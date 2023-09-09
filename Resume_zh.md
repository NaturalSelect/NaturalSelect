# 简历

## 基础信息

* 姓名：黄志斌
* 性别：男
* 年龄：20
* Github ID：NaturalSelect
* 邮箱：2145973003@qq.com

## 基本技能

* 熟悉C++/C#/GO，了解Java/Python。
* 熟悉Posix API、Windows API。
* 了解云原生文件系统。
* 对Raft算法有一定的理解，了解MultiRaft。
* 对分布式事务有一定的理解，了解Percolator风格分布式事务。
* 了解Primary-backup Replication、Chain Replication、Quorum Replication。
* 了解常见磁盘数据结构（B+Tree、LSM Tree）。
* 了解分布式系统原理。
* 了解关系式数据库原理。
* 了解操作系统原理。

## 教育经历

### 成都信息工程大学

本科 | 区块链工程

2021.9 - 2025.6

## 项目经历

### CubeFS

* **项目简介：** CubeFS是新一代云原生存储产品由云原生计算基金会（CNCF）托管的孵化项目， 兼容S3、POSIX、HDFS等多种访问协议，支持多副本与纠删码两种存储引擎，为用户提供多租户、 多AZ部署以及跨区域复制等多种特性，广泛应用于大数据、AI、容器平台、数据库、中间件存算分离、数据共享以及数据保护等场景。
* **社区角色：** Commiter

**相关证书：**

|Commiter|Contributor|
|-|-|
|![Commiter](./CubeFS%20Commiter.jpg)|![Contributor](./CubeFS%20Contributor.jpg)|

### Curve

* **项目简介：** Curve 是网易主导自研的现代化存储系统, 目前支持文件存储(CurveFS)和块存储(CurveBS)。现作为沙箱项目托管于CNCF。
* **社区角色：** Contributor

### Rkv

使用C++编写的基于MultiRaft的键值存储系统。

主要功能：
* 提供基础的`GET/PUT/DELETE`接口。
* 基于MultiRaft，单个集群可以负载大量的Raft状态机。
* 基于key范围的数据分区。
* 动态自动分区。

项目亮点：
* 通过Raft实现数据一致。
* 基于键数量的动态重新分区，当单一分区键数量到达阈值时分裂成两个分区。
* 不依赖除`Boost.Context`以外的其他开源库。