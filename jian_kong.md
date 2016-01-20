# 监控
---
DomeOS提供容器和主机级别的多维度监控。您可以在监控页面查看部署或主机的运行状态。

点击控制台左侧导航栏的“监控”，进入监控页。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject6.jpg)

在监控对象栏选择监控类型。监控类型有“主机”和“容器”。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject6.jpg)

##1. 主机监控
监控类型选择“主机”，并选择希望查看的集群，监控对象栏最下方会出现该集群的主机列表。您可以通过选择主机标签和搜索关键字来筛选出希望查看的主机。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject6.jpg)

选中希望查看的主机，点击“刷新监控指标列表”，即可在右侧“监控指标”栏看到所有的监控指标。各项监控指标意义如下：

| 监控指标 | 意义 | 说明 |
| -- | -- | -- |
| agent.alive | 主机上agent存活情况 | “1”表示存活，“0”表示死亡。只有主机上agent正常运行，才能获取该主机的监控数据 |
| cpu.busy| cpu使用率 | 反映了主机所用cpu占主机总cpu的百分比，不会超过100% |
| mem.memtotal| 内存总量 | 主机的内存总量|
| mem.memused | 内存使用量 | 主机的内存使用量 |
| disk.io.read_bytes/device=xx | 磁盘读总量 | 单位KB/s，device为设备名 |
| disk.io.write_bytes/device=xx | 磁盘写总量 | 单位KB/s，device为设备名|
| df.bytes.used/fstype=xx,mount=xx | 磁盘使用量 | fstype为分区类型，mount为分区挂载点 |
| df.bytes.total/fstype=xx,mount=xx| 磁盘总量 | fstype为分区类型，mount为分区挂载点 |
| net.if.in.bytes/iface=xx | 网络接收带宽 | 单位KB/s，iface为网卡 |
| net.if.out.bytes/iface=xx | 网络发送带宽 | 单位KB/s，iface为网卡 |

选中希望查看的监控指标，点击“看图”，选择一种视角，即可在新页面查看监控。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject6.jpg)

##2. 容器监控
监控类型选择“容器”，并选择希望查看的集群和容器所在部署。监控对象栏最下方会出现该部署的实例列表。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject6.jpg)

选中希望查看的实例，此时您可以直接点击“刷新监控指标列表”，查看监控。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject6.jpg)

如果您希望查看实例内部的容器监控，请在选中实例后点击“查看容器”，进入所选实例的容器列表。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject6.jpg)

选中希望查看的容器，并点击“刷新监控指标列表”，在监控指标栏选中希望查看的指标，点击“看图”并选择视角，即可查看监控。
![](http://881471b33d4f9.cdn.sohucs.com/q_mini/newproject6.jpg)


实例和容器的各项监控指标意义如下：

| 监控指标 | 意义 | 说明 |
| -- | -- | -- |
| container.cpu.usage.total/id=xx |cpu使用率| xx为container id，该项为实例或容器占所在主机的cpu百分比 |
| container.memory.usage/id=xx |内存使用量 | 实例或容器的内存使用量|
| container.memory.limit/id=xx | 内存限额 | 实例或容器所分配的内存限额 |
| container.network.rxbytes | 网络接收带宽 | 单位为KB/s|
| container.network.txbytes | 网络发送带宽 | 单位为KB/s |


