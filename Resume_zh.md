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

## 开源经历

### CubeFS

* **项目简介：** CubeFS是新一代云原生存储产品由云原生计算基金会（CNCF）托管的孵化项目， 兼容S3、POSIX、HDFS等多种访问协议，支持多副本与纠删码两种存储引擎，为用户提供多租户、 多AZ部署以及跨区域复制等多种特性，广泛应用于大数据、AI、容器平台、数据库、中间件存算分离、数据共享以及数据保护等场景。
* **社区角色：** Commiter

**相关证书：**

|Commiter|Contributor|
|-|-|
|![Commiter](./CubeFS%20Commiter.jpg)|![Contributor](./CubeFS%20Contributor.jpg)|

**提交的Pull Request列表：**

|标题|PR|主要内容|状态|
|-|-|-|-|
|[Feature]: Master does snapshot optimization|#2124|加速Master的快照apply。|Merged|
|[Feature]: Master qosClientId allocation optimization|#2112|使用batch进行id分配。|Merged|
|[Feature]: Master supports the reporting interface of io and cpu load|#2097|为datanode、metanode添加上报负载信息的功能，并支持在master查询|Merged|
|[Feature]: The cfs-cli supports setting the maximum number of dp on datanode|#1946|去除`dp limit`全局变量，实现limit可被动态调整。|Merged|
|test(datanode): fix limit_test.go unit test|#2035|修复错误的单元测试代码。|Merged|
|fix(master): fix #2084|#2086|修复#2084。|Merged|
|fix(master): fix `api_service_test.go`|#2123|修复`api_service_test.go`中的所有错误。|Merged|
|test(master): add IDAllocator test and fix TestBalanceMetaPartition test|#2215|修复master单元测试中的其他错误（以便在CI中包含master）并添加`IDAllocator`单元测试。|Merged|
|[Feature]: Limit the number of threads for blobnode and datanode to read and write disk|#1974|限制datanode和blobnode的磁盘读写线程数量，防止线程数量过多造成panic并提高性能。|Merged|
|[Feature]: Support for multiple selection strategies when selecting nodes and nodesets|#2353|在选择node和nodeset时支持多个策略（`RoundRobin`、`CarryWeight`、`AvailableSpaceFirst`、`Ticket`）并支持CLI/HTTP API进行多维度的策略查询和切换。|Merged|
|[Feature]: Master/DataNode/MetaNode start log optimization|#2350|在启动时打印log内容到output以便于分析启动失败的原因|Merged|
|[Feature]: Use parallel compile to speed up pre_build|#2344|使用`-j`选项加速依赖的编译|Merged|
|[Feature]: Supports write disable option|#2537|支持主动禁止卷的写入|Merged|

### Curve

* **项目简介：** Curve 是网易主导自研的现代化存储系统, 目前支持文件存储(CurveFS)和块存储(CurveBS)。现作为沙箱项目托管于CNCF。
* **社区角色：** Contributor

提交的Pull Request列表：

|标题|PR|主要内容|状态|
|-|-|-|-|
|[Build]: Support build on GCC 11+|#2642|修改了一些bug并支持curve在高版本GCC构建|Merged|
|[Feature]: curvefs metaserver support asynchronous snapshot|#2691|curvefs支持metaserver异步raft snapshot|Review|

## 个人项目

### Sharpen

基于协程的C++网络库，封装了Iocp（Windows）、Epoll（Linux）和io_uring(Linux)，并提供一个不完整的Raft实现。

主要功能：
* 提供Tcp Socket的封装。
* 提供File Stream的封装。
* 提供Pipe 的封装。
* 提供Posix Signal的封装。
* 提供基于模板元的半自动序列化和反序列化。

项目亮点：
* 提供基于协程的I/O操作。
* 不依赖除`Boost.Context`以外的其他开源库。

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

## 教育经历

### 成都信息工程大学

本科 | 区块链工程

2021.9 - 2025.6