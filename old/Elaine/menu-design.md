*menu-design*menu(功能菜单)

说明
	1.对前台菜单进行展示，编辑
	2.对后台菜单进行展示，编辑

问题
需求问题
	1.前台问题
		a)前台菜单展示(名称。自定义链接,显示顺序)
		b)展示页面可直接对父次菜单进行修改(名称，链接)，删除
		c)菜单信息编辑(名称，所属父级，自定义链接)
		d)菜单删除
		e)一级菜单添加(名称。自定义链接)
		f)二级菜单添加(名称，所属父级，自定义链接)
2.后台
		a)后台菜单展示(名称。自定义链接,显示顺序)
		b)展示页面可直接对父级菜单进行修改(名称，链接，显示顺序)，删除
		c)菜单删除
		d)父级菜单添加(名称。自定义链接,显示顺序)
		e)子级菜单添加,编辑(名称。自定义链接,显示顺序，所属父级)

一、 系统变量 ~

二、 请求设计 ~ 

三、 权限设计 ~

四、 对象设计 ~

五、 数据库设计 ~
menu(菜单)
	mid:菜单编号(主键)	int
	name:菜单名称		varchar(20)
	parent_mid:菜单父ID	int
	url:自定义链接		varchar(255)
	quality:优先级(排列顺序)	int



六、 APIs设计 ~