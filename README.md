directConfig
===

现在都搞得太复杂，太折腾了，索性我自己收集整理，如其名字 'directconfig' 所说一样，就是基于本地能访问来设置的，即本地白名单机制。

### 概述

因为是白名单机制，所以默认都走代理网络（proxy），direct.list 是主文件。

### 规则原理

GEOIP(cn/private) - 本地网络

direct.list - 在某国能直接访问的或者要求只能本地访问的，走本地网络

google.list - Google 专线

apple.list -  Apple 专线

special.list -  指定网络

兜底策略是 proxy
