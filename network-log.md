# Network Logs

## NetMon

1. 下载Net Monitor安装包,确认选取目标机器对应平台的安装包
    - https://www.microsoft.com/en-us/download/4865
2. 在需要抓取网络包的机器上安装Network Monitor(使用默认选项即可).
3. 以管理员身份运行Network Monitor. 请注意尽量关闭与问题无关的软件以及不进行不相关操作以防数据包过大.
4. 检查左下角Select Networks中对应的网络是否被勾选,确保正在被使用的IP对应的网卡被选中.
5. 点击 "New Capture", 然后点击start(或者F5)开始抓取数据.
6. 重现问题,并记录时间点, URL等相关信息
7. 在Network Monitor上点击"Capture"->stop”(或者F7) ,点击"File"->"Save as"，保存为Cap包.

## Trace Router

1. 以管理员权限运行CMD
2. 执行以下命令跟踪路由并告知结果:
    - `ping -4 -n 20 <FQDN of your site>`
    - `tracert <FQDN of your site>`
