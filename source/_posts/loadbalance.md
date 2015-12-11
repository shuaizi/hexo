title: loadbalance
date: 2015-12-11 09:59:11
tags: network
---

## 负载均衡
* 硬件：贵
* 软件：LVS



## 负载均衡类型
* LVS-DR  
* LVS-NAT  
* LVS-TUN  
* Full-NAT  

#### DR Direct Routing
* 直接路由，性能最好
* 在loopback上绑定VIP

#### NAT
* 外网和内网地址的映射
* 请求时，修改DNAT为目的RS的IP，回应时，修改SNAT为VIP


#### Full-NAT
* 外网和内网地址的映射
* 请求时，修改源IP为LVS内网IP，目的IP为目的RS的IP，回应时，修改源IP为LVS的VIP，目的IP为客户端的IP