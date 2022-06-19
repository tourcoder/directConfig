directConfig
===

现在都搞得太复杂，太折腾了，索性我自己收集整理，做了一个简单的列表，下面是两个方案

### 方案一

本地白名单机制，即不在本名单里面的都视为无法被正常访问的，都走指定网络。

规则原理：

GEOIP(cn/private) - 本地网络

cndirect.list - 在 cn 本地能够访问的，走本地网络

google.list - Google 专线

special.list -  指定网络

兜底策略是 proxy

### 方案二

本地黑名单机制，即默认走本地网络，其他的走指定的网络

规则原理

blocked-in-cn.list - 在 cn 本地无法访问的，走自己选择的指定网络

google.list - Google 专线

special.list -  指定网络

兜底策略是 direct
