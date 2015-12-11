title: linux虚拟网络设备介绍
date: 2015-12-11 10:05:51
tags: network
---
* linux bridge
> 如名字所说，实现数据包的转发  
> 只能够处理接收的包，不能处理发送的包

* vlan device
> 实现数据包的隔离  
> 通常与linux bridge结合使用，来模拟现实世界的802.1q交换机

* tap设备（tun，tap）
> 让用户程序向内核协议栈注入数据的设备  
> tun工作在三层，tap工作在二层

* veth设备
> 总是成对出现  
> 作用是反转通讯数据的方向，间接完成数据注入

*ovs （openflow vswitch）
> 模拟现实的二层交换机的基本功能，并且额外支持openflow协议  
> 性能和linux bridge相当