# 组管理
---
通常，公司内一个项目的开发、一个部署的运维和一个集群的管理都是由相应职能部门的某个小组完成的。DomeOS提供组管理的功能，让负责同样资源的用户能够统一管理和协作。当创建一个资源时（该资源可能是项目、部署或集群），可以选择以组的身份创建。资源创建后，创建组的成员直接获得和组内权限对应的资源权限，方便组成员管理和维护资源。

##1. 新建组

在组管理页面点击“创建组”，进入创建组的配置页面。您需要填写组名称，可以给组添加描述和成员。完成设置后，点击“完成创建”。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject63.jpg)

##2. 管理组成员
在组列表中点击一个组的名字，进入组的成员页面。如果您的组内权限是master，您可以点击“编辑”按钮，添加新用户、修改已有用户的权限、或删除用户。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject64.jpg)


##3. 角色权限
组内各角色权限划分如下：

| 角色 |权限 |
| -- | -- |
| master | 组内最高权限，可以查看组，删除组，管理组成员 |
| developer | 可以查看组|
| reporter | 可以查看组|
