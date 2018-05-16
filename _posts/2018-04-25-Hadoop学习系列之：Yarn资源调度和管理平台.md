# Yarn系统架构及功能

####1. Yarn定义

Yarn：Yet another resource negotiation——资源调度和管理平台

yarn为主从结构：

* 主节点：ResourceManager，可以有两个（主备关系）

  负责集群资源的分配和调度MapReduce、Storm、Spark等应用，必须实现**ApplicationMaster**接口才能被RM管理

* 从节点：NodeManager，可以有很多个

  负责**单节点资源的管理**

Yarn支持管理的资源：CPU、内存

#### 2. Yarn组件架构

![Screen Shot 2018-05-17 at 12.12.13 AM.png](https://i.loli.net/2018/05/17/5afc58854982b.png)

Resource Request：出现一个JOb会激活一个APP MASTER，app master会预算所需要的资源并向RM提出申请，RM分配container

app master会通知NodeManager启动任务

Node status：RM调查NodeManager情况

App master也是一个container，其所负责的container会向app master汇报

