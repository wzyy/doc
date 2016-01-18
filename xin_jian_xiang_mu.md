# 新建项目



登录DomeOS系统，左侧导航栏选择“项目管理”，然后点击左上的“创建新项目”。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject1.jpg)
##1. 关联代码仓库
DomeOS支持关联私有Gitlab账户。您需要点击“关联新账户”并输入自己的Gitlab帐户名和密码，将您Gitlab上的代码同步到DomeOS上。您可以选择您自己的一个代码项目作为本次新建项目的代码源。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject2.jpg)
##2. 持续集成
在“自动构建”中指定代码项目的分支或tag，当代码仓库发生push操作的时候，您的项目会自动触发一次构建，保证项目镜像和代码源同步更新，实现持续集成。
![](http://)
##3. Dockerfile和构建运行相关配置
项目需要有Dockerfile才能构建成可运行的镜像文件。您可以选择使用代码内的Dockerfile或在页面上配置一个Dockerfile。
###3.1 使用代码内Dockerfile
如果代码项目内有Dockerfile，选择使用代码项目内dockerfile。并为项目起一个名字，点击下一步。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject3.jpg)
###运行环境配置
配置dockerfile运行时需要的环境变量
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject4.jpg)

#新配置dockerfile
若项目中未包含dockerfile，我们可以通过DomeOS前端简单的配置，填写配置一个新的dockerfile。
根据需求填写需要的dockerfile的文件编译配置，示例如下：
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject5.jpg)

如有必要，可以在高级配置中填写运行时的环境变量：
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject6.jpg)

填写完必要的信息后，点击完成创建，我们就实现了新建一个项目。