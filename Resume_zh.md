# 简历

## 基础信息

* 姓名：黄志斌
* 性别：男
* 年龄：20
* Github ID：NaturalSelect
* 邮箱：2145973003@qq.com
* 手机号： +86 15915145280

## 基本技能

* 熟悉C++/C#/GO，了解Java/Python。
* 熟悉Posix API、Windows API。
* 了解云原生文件系统。
* 对Raft算法有一定的理解，了解MultiRaft。
* 对分布式事务有一定的理解，了解Percolator风格分布式事务。
* 了解Primary-backup Replication、Chain Replication、Quorum Replication。
* 了解常见磁盘数据结构（B+Tree、LSM Tree）。
* 了解分布式系统原理、关系式数据库原理、操作系统原理。

## 教育经历

### 成都信息工程大学

本科 | 区块链工程

2021.9 - 2025.6

## 项目经历

### CubeFS

* **项目简介：** CubeFS是新一代云原生存储产品由云原生计算基金会（CNCF）托管的孵化项目， 兼容S3、POSIX、HDFS等多种访问协议，支持多副本与纠删码两种存储引擎，为用户提供多租户、 多AZ部署以及跨区域复制等多种特性，广泛应用于大数据、AI、容器平台、数据库、中间件存算分离、数据共享以及数据保护等场景。
* **社区角色：** Commiter
* **项目日期：** 2023/5 - 至今

**相关证书：**

|Commiter|Contributor|
|-|-|
|![Commiter](./CubeFS%20Commiter.jpg)|![Contributor](./CubeFS%20Contributor.jpg)|

**主要贡献:**

* 添加和修复多个模块的单元测试，提高测试覆盖率。
* 对Master模块进行优化，加速快照应用和Client Id分配。
* 添加查询DataNode和MetaNode的负载的功能，减轻运维负担。
* 重构副本放置算法，并加入多种策略，提供更为丰富的功能。
* 添加主动禁止卷写入的功能，与卷迁移功能对接。
* 添加设置DataNode数据分区限制的功能，以便运维根据具体情况做出调整。

### Curve

* **项目简介：** Curve 是网易主导自研的现代化存储系统, 目前支持文件存储(CurveFS)和块存储(CurveBS)。现作为沙箱项目托管于CNCF。
* **社区角色：** Contributor
* **项目日期：** 2023/8 - 至今

**主要贡献:**

* 修复了不能在GCC 11上编译的BUG。
* 支持元数据服务进行异步的raft 快照。

### Rkv

* **项目简介：** 使用C++编写的基于MultiRaft的简单键值存储系统，面向大量小键设计，提供基于范围的自动分区。
* **项目日期：** 2022/4 - 2022/6
* **项目角色：** 开发者