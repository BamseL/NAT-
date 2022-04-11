# NAT-

将Linux系统配置成NAT网关，具备NAT、DHCP、DNS功能,利用地址池实现内网访问外网的通信、实现外网对内网特定主机的访问以及域名解析的功能。搭建实验测试网络。




大致思路：
1、使用linux虚拟机。
1）、安装VMware 14.1.1虚拟机
2）、安装Ubuntu-20.04.1系统
2、按要求配置
要求（1）：将Linux系统配置成NAT网关，有NAT、DHCP、DNS功能。
在Linux系统上用iptable配置NAT网关。
知道用iptable 配置NAT网关，知道了SSH，SSHD的简单含义，知道了状态监测的四种状态：NEW,ESTABLISED,RELATED,INVALID
20201223 22:06 下一步：IPtable 的语法问题，SNAT和DNAT的实现
Iptables 语法中表：filter用于过滤外网主机（即实现外网对内网特定主机的访问），nat用于实现网络地址转换（NAT）

Xshell 连接Linux系统，（1）安装ssh。（2）安装net工具。（3）安装ufw。（4）关闭ufw。（5）开放端口22

Iptables 的配置需要获得管理员权限root,具体方法见
https://blog.csdn.net/jxaucm/article/details/80194372
Authentation failure

Linux系统被配置成了一个NAT网关（防火墙），不是一台计算机了。
已经完成：
20201224 22:20 下一步：什么是ppp0？Eth0和eth1的问题将Linux配置成网关，DHCP、DNS问题。
20201225 17:34 下一步isc-dhcp-server使用方法
20201225 22:25 下一步/etc/network/interface ??  看ubuntu 官方文件
要求（2）：利用地址池实现内网访问外网的通信。
自己定义内网地址池，逐个测试内网访问外网
安装两个虚拟机？将两个虚拟机作为内网，而自己的计算机作为外网？
要求（3）：实现外网对内网特定主机的访问以及域名解析的功能。
外网访问内网的特定主机应该是建立隧道？
答：不需要建立隧道，配置网关时，利用IPtables 应该可以将外网主机设为白名单。
如何实现域名解析？
