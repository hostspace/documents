增加IP分组功能设置－－设计

目的：
对业务IP和管理IP进行分组，使其管理IP只能使用同组的业务IP。

设计思想:
1.创建一个分组表，存机房的分组。
2.管理IP实体增加一个所属分组字段。
3.业务IP实体增加一个所属分组字段。
4.在增加管理IP和业务IP时选择它们所属的分组。
5.修改与IP分配有关的代码(我想到的有两个地方)。
  5.1.订单自动分配管理IP和业务IP需要修改。
  5.2.工单里面的分配，要通过分配的管理IP来确定可分配的业务IP(需要李家东来完成)。
    *5.2.1 需要唐提供一个接口(根据管理IP获取可用的业务IP)
  5.3.服务器上柜只能搜索本机房的管理IP。
    *5.3.1 本机房可能存在多个分组，需考虑加入分组

请求设计：
admin/ip/group: 分组列表
admin/ip/group/add: 增加分组
admin/ip/group/{group}: 编辑分组

表设计：
 分组表(ip_group)：
   gid: 主键
   name: 分组名
   rid: 所属机房
   created: 创建时间
   uid: 用户ID
   changed: 更改时间

  管理IP实体增加一个"group_id", "rid"字段。
  业务IP审核申请表增加一个"group_id"字段。
  业务IP实体增加一个"group_id"字段。

  **所属分组一但被使用就不能改变其所属机房**

优化功能：
  优化管理Ip列表的查询，可以按照分组进行查询。
  优化业务IP列表的查询，可以按照分组进行查询。