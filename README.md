directConfig
===

现在都搞得太复杂，太折腾了，索性我自己收集整理，如其名字 'directconfig' 所说一样，就是基于本地能访问来设置的，即本地白名单机制。

### 概述

因为是白名单机制，所以默认都走代理网络（proxy），direct.list 是主文件。

### 主规则

这三套规则基本覆盖了常规内容，能无缝访问网络

GEOIP(cn/private) - 本地网络

direct.list - 能被直接访问的或者要求只能本地访问的，走本地网络

兜底策略是 proxy

### 扩展规则（选项）

有时候自己需要一些特殊的设置，所以将一些常规的独立出来了

google.list - Google 专线

apple.list -  Apple 专线

bing.list - Bing 专线

github.list - GitHub 专线

telegram.list - Telegram 专线

special.list -  指定网络
