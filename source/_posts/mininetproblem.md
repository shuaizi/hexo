title: mininetproblem
date: 2015-12-11 10:08:55
tags: network
---

*关于mininet在非正常退出时，不会清理掉ovs-switchd相关进程的解决：  
*删除并重新创建ovsdb-server的数据库conf.db    
操作命令（具体目录可能有变）:    
>	rm /etc/openvswitch/conf.db     (最好备份，以防后面创建失败)  
>	service openvswitch-switch stop  
>	ovsdb-tool create /etc/openvswitch/conf.db /usr/share/openvswitch/vswitch.ovsschema  
>	service openvswitch-switch start  
