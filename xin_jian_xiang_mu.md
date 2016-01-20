# 新建项目
---
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
如果您的代码项目包含Dockerfile，则在新建部署的时候开启“使用代码内Dockerfile”。之后您需要选择创建者身份（关于创建者身份的意义和用途，详见[项目成员](https://wzyy.gitbooks.io/domeos/content/xiang_mu_cheng_yuan.html)）并填写项目名称。完成所有操作后点击“下一步”。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject1.jpg)

您需要继续进行构建和运行相关的配置。其中运行过程环境变量是在项目中声明并给出默认值和描述，用于提示部署运维人员在部署和升级等操作时配置。完成所有配置后，点击“完成创建”，就成功创建了一个项目。您可以在项目列表中查看所有项目。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject1.jpg)

###3.2 配置Dockerfile
如果您的代码项目不包含Dockerfile，或代码中的Dockerfile已经不适用了，那么您可以在新建项目时通过简单的几项配置，生成一个Dockerfile，用于构建您的项目。

在新建项目第一步，关闭“使用代码内Dockerfile”，选择创建者身份并填写项目名称。完成所有操作后点击“下一步”。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject1.jpg)

接下来您需要进行Dockerfile的配置，您可以选择手动配置，也可以点击“复制已有项目”来复制一个项目的Dockerfile配置。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject5.jpg)

您可以在“高级设置”中指定配置文件模板，上传文件（如配置文件）以及运行相关的其他配置。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject6.jpg)

完成所有配置后，点击“完成创建”，成功创建一个新项目。