# 新建项目

您可以在DomeOS上关联您的代码源，并通过简单的配置创建一个项目，项目可以被构建成可交付的镜像文件。

进入DomeOS控制台，点击左侧导航栏的“项目管理”，再点击“新建项目”，进入新建项目页面。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject1.jpg)

##1. 关联代码仓库
DomeOS支持关联私有Gitlab，您可以在新建项目第一步选择Gitlab仓库，并点击“关联新账户”。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject1.jpg)

输入您的Gitlab用户名和密码。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject1.jpg)

您会看到自己Gitlab上的代码项目已经同步到了DomeOS。您可以选择一个代码项目作为此项目的代码源。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject1.jpg)

##2. 持续集成
项目只有被构建成镜像文件才能交付和部署。针对代码项目快速迭代的特点，DomeOS开发了智能化的持续集成功能。在关联代码仓库后，您可以在“自动构建”处指定代码项目的branch和tag，当您的代码源发生push操作时，会自动触发一次构建，保证您的项目镜像和代码源同步。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject1.jpg)

##3. Dockfile和运行相关配置
项目的构建需要Dockfile才能进行，您可以使用代码项目内的Dockerfile，也可以在DomeOS页面上配置一个新Dockerfile。
###3.1 使用代码内Dockerfile
如果您的代码项目包含Dockerfile，则在新建部署的时候开启“使用代码内Dockerfile”。之后您需要选择创建项目的身份（关于创建身份的用途，详见[项目成员](https://wzyy.gitbooks.io/domeos/content/xiang_mu_cheng_yuan.html)）并填写项目名称。完成所有操作后点击“下一步”。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject1.jpg)
