---
title: "集群故障诊断FAQ"
date: 2019-03-11T12:50:54+08:00
draft: false
weight: 1320
description: 当试用 Rainbond 遇到问题时，请先参考本篇文档。如果问题未解决，请按要求收集必要的信息通过社区反馈给Rainbond开发者。
hidden: true
---

当试用 Rainbond 遇到问题时，请先参考本篇文档快速索引部分。如果问题未解决，请按要求收集必要的信息通过[社区(用户帮助)](https://t.goodrain.com/) 提供给Rainbond开发者。

#### 如何给Rainbond开发者报告错误

当使用 Rainbond 遇到问题并且通过后面所列信息无法解决时，请收集以下信息并创建新 Issue:

- 具体的出错信息以及正在执行/历史执行的操作(正在执行的操作或者之前的操作导致集群故障)
- 当前集群所有组件的状态(dps/node/docker/kubelet)
- dmesg中关于Rainbond或者docker的相关信息

#### 必要信息

```yaml

Rainbond版本:
操作系统:
内核版本:
环境:(云服务商,实体机,虚拟机等，是否为全新环境，如果不是，部署了其他什么服务)
节点配置(CPU核数,内存大小,硬盘类型(SSD/机械硬盘),网络类型,网络拓扑):
安装类型:
如何复现:
尝试解决: 
相关截图:


1. 集群是否正常（grctl node list）
2. 应用是否正常  (grctl service get <应用概览url>)
3. 应用监听端口是否正确，是否开启了健康检测，持久化目录是否设置正确
4. 集群状态
5. 操作流程，能否复现
6. 是否尝试过更新部分组件的镜像，是否有效
7. 当前正在进行什么操作
8. 最近一段时间的网络/IO监控数据是否有异常

```

#### 快速索引

- [重置企业管理员密码](/user-operations/op-guide/reset_enterprise_password/)