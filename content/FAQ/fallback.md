---
date: "2020-12-23T00:00:00.000Z"
description: Project X 的文档.
title: 回落相关问题
weight: 5
---

{{% panel theme="warning" header="**Q: 回落是个啥?好吃吗?** " %}}

Fallback 是 Xray 的最强大功能之一, 可有效防止主动探测, 自由配置常用端口多服务共享

点此查看详情 [回落](../../config/fallback)
{{% /panel %}}

{{% panel theme="warning" header="**Q: 为什么我回落以后nginx日志的IP是 127.0.0.1?** " %}}

需要开启 proxy protocol. 参见[fallbacks配置](../../config/fallback)的xver参数

{{% /panel %}}

{{% panel theme="warning" header="**Q: 我还是上一题的提问者, 那么我如何使用proxy protocol,达到所有日志都有源IP的目的呢?** " %}}

~~等待好心人写一篇小小白白话文~~

{{% /panel %}}

{{% panel theme="warning" header="**Q: Wordpress 是 Mixed Content, 回落到配置的Wordpress看起来怪怪的, 怎么办?** " %}}

<img src="https://avatars2.githubusercontent.com/u/8460881?s=60" width="32px" height="32px" alt="a"/>[@Ardentwheel](https://github.com/Ardentwheel) :

需要在nginx的配置中加入以下内容，才可以修复
```
add_header Content-Security-Policy "upgrade-insecure-requests";
```

{{% /panel %}}
