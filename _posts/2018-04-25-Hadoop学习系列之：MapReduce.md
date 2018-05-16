# MapReduce学习

#### 1. MapReduce定义

MapReduce是**面向大数据并行处理（大于1TB）的计算模型、框架、平台，其资源调度由Yarn完成**

* 基于集群的高性能并行计算平台：cluster infrastructure
* 并行计算与运行软件框架：software framework
* 并行程序设计模型和方法：programming model&methodology

MapReduce不适合**迭代计算、实时计算**，适合**离线计算**

MR特点：

* 易于编程：程序员只需要描述做什么，具体交给系统执行框架处理
* 良好扩展性：可以添加机器扩展集群能力
* 高容错性：通过计算迁移或者数据迁移等策略提高集群的可用性与容错性

#### 2. MapReduce计算流程

##### 2.1 MR计算过程——数据形式

![Screen Shot 2018-05-16 at 11.54.41 PM.png](https://i.loli.net/2018/05/16/5afc54be014e2.png)

#####2.2 MR过程详解

* ResourceManager：根据用户map请求由RM create job。Job提交前先进行split操作。在Map操作开始前，提交job给RM，RM根据NM的情况选择合适的节点调度app master。
* map分为四步：partition、sort、combine、spill/merge
* reduce：suffer/copy、sort/merge、reduce

![Screen Shot 2018-05-16 at 11.55.19 PM.png](https://i.loli.net/2018/05/16/5afc54be04e65.png)

![Screen Shot 2018-05-16 at 11.55.26 PM.png](https://i.loli.net/2018/05/17/5afc56651f966.png)