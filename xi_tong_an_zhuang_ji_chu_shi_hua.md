# 系统安装及初始化

1. 如果您的私有仓库通过http访问，在第1步用Docker Hub官方镜象启动私有仓库，该私有仓库在您的Kubernetes集群外部。如果您的私有仓库通过https访问，需要在第4步安装Kubernetes时，通过Kubernetes启动私有仓库。

2. 安装并启动etcd集群。详细步骤见etcd官方网站。

3. 给集群内的主机安装Docker。主机的hostname需要符合dns命名规则。每台主机需要配置私有仓库地址

4. 安装带flannel网络的Kubernetes集群：

   配置flannel时，需要给出etcd地址并配置etcd-prefix。
   
   启动flannel时，主机上的Docker必须停止。
   
   启动flannel后，需要重新启动Docker。
   
   Kubernetes集群在启动服务端时，需要按顺序启动以下三个组件：api server、kube-controller-manager、kube-scheduler。在api server完全启动后，再启动后两个组件。      
   
   启动主机时，需要启动两个组件：kubelet和kube-proxy                            
   
   更详细的安装步骤详见Kubernetes官方网站。

4. 配置skyDNS，kube2sky。DomeOS的公开镜像仓库中提供了两者的镜像。DomeOS提供安装两者的YAML文件，Kubectl可以根据YAML文件创建两者。

5. 启动MySQL，建议通过传统方式启动而非镜像启动。

6. 启动监控需要的四个组件：transfer、graph、query、dashboard。DomeOS公开镜像仓库提供镜像。 transfer和query中配置的graph信息需要保持一致。

   需要在每台主机上安装agent，每个agent需要配置一个transfer地址。agent镜像在DomeOS公开镜像仓库中提供。
   
   agent和监控四个组件的工作逻辑：
   agent上报信息给transfer；transfer将信息传递给graph存储；query从graph里查询信息；dashboard把从query里查询的信息做图形化展示。
   
   更多详细步骤见小米Open-Falcon官方文档

7. 在每个主机上启动一个镜像，用于容器的ssh登录。镜像由DomeOS公开镜像仓库提供。

8. 启动DomeOS server 。镜像由DomeOS公开镜像仓库提供。