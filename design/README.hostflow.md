===目的:===
- 整合网站后台流程步骤

===系统变量:===
* SOP系统工单状态
$sop_status = array(
 '新工单',
 '运维处理',
 '业务处理',
 '已交付',
 '完成',

 '运维转接工单',
 '运维已交付',

 '核实业务信息',
 '业务转接',
 '运维返工',
);

$sop_buttons = array(
  '交付客户', //业务权限
  '转交运维部',
  '质量异常',
  '提取计费信息',
  '业务已核实',
  '完成',
  '接受工单', //技术权限
  '审核异常',
  '交他人处理',
  '异常接受工单',
  '交付业务部',
  '直接交付客户',
  '建立工单', //技术业务可见
  '修改/保存',
  '提取交付信息',
  '修正工单/保存工单',
  '撤消返工', //特殊权限
  '撤消工单', //工单建立人
);

$question_type = array(
 I3,P1,P2,P3,P4,P5,P6,E类
);