# 简历

## 基础信息

>姓名：
>
>性别：男
>
>年龄：20
>
>Github ID：NaturalSelect
>
>邮箱：2145973003@qq.com

## 基本技能

* 熟悉C++/C#/GO，了解Java/Python。
* 熟悉Posix API、Windows API。
* 了解云原生文件系统。
* 对Raft算法有一定的理解，了解MultiRaft。
* 对分布式事务有一定的理解，了解Percolator风格分布式事务。
* 了解Primary-backup Replication、Chain Replication、Quorum Replication。
* 了解分布式系统原理。
* 了解关系式数据库原理。

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

## 开源经历

### CubeFS

CubeFS是新一代云原生存储产品， 兼容S3、POSIX、HDFS等多种访问协议，支持多副本与纠删码两种存储引擎，为用户提供多租户、 多AZ部署以及跨区域复制等多种特性，广泛应用于大数据、AI、容器平台、数据库、中间件存算分离、数据共享以及数据保护等场景。

为CubeFS编写了10+ Pull Requests:
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
|[Feature]: Limit the number of threads for blobnode and datanode to read and write disk|#1974|限制datanode和blobnode的磁盘读写线程数量，防止线程数量过多造成panic并提高性能。|Review|
|[Feature]: DataNode receiving processing supports speed limit|#2182|支持primary-backup 复制的接收限速，并提供operate阶段的负载监控，以便动态对限速做出调整。|Review|
|[Feature]: Support for multiple selection strategies when selecting nodes and nodesets|#2226|在选择node和nodeset时支持多个策略（`RoundRobin`、`CarryWeight`、`AvailableSpaceFirst`）并支持CLI/HTTP API进行查询和切换。|Review|
|test(ci): show more information in CI to help debug|#2278|在CI中显示node信息以帮助debug|Review|
|[Fix]: fix cli format bug|#2284|修复CLI中的格式化输出函数误用|Review|

