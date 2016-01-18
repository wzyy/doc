# 新建项目

登录DomeOS系统，左侧导航栏选择“项目管理”，然后点击左上的“创建新项目”。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject1.jpg)
#关联代码仓库
关联一个代码仓库，以gitlab为例，点击关联新账户，然后输入自己的gitlab账户和密码进行登录，登录后选择一个已有的项目。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject2.jpg)
#持续集成
如果希望项目可以根据代码的更新持续集成，则在自动构建选择或输入需要的分支。

#已有dockerfile
如果项目内有dockerfile，选择使用代码项目内dockerfile。并为项目起一个名字，点击下一步。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject3.jpg)
###运行环境配置
配置dockerfile运行时需要的环境变量
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject4.jpg)

#新配置dockerfile
若项目中未包含dockerfile，我们可以通过DomeOS前端简单的配置，填写配置一个新的dockerfile。
根据需求填写需要的dockerfile的文件编译配置，示例如下：
[](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject5.jpg)
如有必要，可以在高级配置中填写运行时的环境变量：
[](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject6.jpg)
填写完必要的信息后，点击完成创建，我们就实现了新建一个项目。