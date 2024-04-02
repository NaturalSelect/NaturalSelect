> # 存储工程师简历
>
> ## 基础信息
>
> * 姓名：黄志斌
> * 性别：男
> * 年龄：20
> * Github ID：NaturalSelect
> * 邮箱：2145973003@qq.com
> * 手机号： +86 15915145280
>
> ## 基本技能
>
> * 熟悉C++/C#/GO，了解Java/Python。
> * 熟悉Posix API、Windows API。
> * 熟悉分布式存储系统(CubeFS、Ceph、Curve)。
> * 熟悉Raft和MultiRaft算法。
> * 熟悉Percolator风格分布式事务。
> * 了解常用复制方式（Primary-backup Replication、Chain Replication、Quorum Replication）。
> * 了解分布式系统原理。
>
> ## 教育经历
>
> ### 成都信息工程大学
>
> 本科 | 区块链工程
>
> 2021.9 - 2025.6
>
> ## 实习经历
>
> ### Sohu
>
> **部门：** 大数据中心-基础架构团队
>
> **时间：** 2023 年 10 月 - 12月
>
> **岗位：** SRE工程师（Ceph集群）
>
> **职责：** 运维Ceph存储集群
>
> **内容：**
>   * DevOps集群：
>       * 调优CephFS 配置，提高元数据效率。
>       * 调整CephFS 用法，避免DevOps编译后，回收垃圾数据过慢的瓶颈。
>   * OpenStack集群：
>       * 调整 RBD 配置，提高IO效率。
>   * 部署Ceph监控。
>
> ### OPPO
>
> **部门：** 互联网服务系统/云数服务中心/云存储部/存储技术组
>
> **时间：** 2024 年 1 月 - 至今
>
> **岗位：** 后端工程师（分布式存储）
>
> **职责：** 分布式存储系统CubeFS的开发迭代
>
> **内容：**
>   * 3.3.2版本:
>       * Master组件：
>           * Raft 快照流程重构以及BUG修复。
>           * DataPartition follower read相关bugfix。
>           * 磁盘损坏自动化迁移。
>       * MetaNode组件：
>           * 修复极端情况下，审计日志回收不及时的BUG。
>           * Inode删除审计日志滚动支持。
>           * Data Partition丢失时，调过extent回收，避免回收列表堆积。
>           * 文件截断流程支持批量删除extents。
>       * DataNode组件：
>           * 重启和升级场景的启动加速。
>       * Client组件：
>           * 大压力下流控的bugfix
>   * MetaNode组件 Rocksdb持久化的开发:
>       * MetaNode支持指定多个Rocksdb目录，每个目录代表一个磁盘，MetaPartition创建时选择磁盘放置数据。
>       * 每个磁盘一个Rocksdb实例，复用BlockCache。
>       * 重构文件删除（unlink）和截断（truncate）流程，保持Rocksdb落盘原子性。
>       * 封装原有内存流程和Rocksdb流程为一套接口。
>
>
> ## 项目经历
>
> ### CubeFS
>
>
> **项目简介：** CubeFS是新一代云原生存储产品由云原生计算基金会（CNCF）托管的孵化项目， 兼容S3、POSIX、HDFS等多种访问协议，支持多副本与纠删码两种存储引擎，为用户提供多租户、 多AZ部署以及跨区域复制等多种特性，广泛应用于大数据、AI、容器平台、数据库、中间件存算分离、数据共享以及数据保护等场景。
>
> **社区角色：** Committer
>
> **项目日期：** 2023/5 - 至今
>
> **主要贡献与职责:**
>
> CubeFS是一个代码量高达 280k + Lines的超大型系统，内部分为Master、DataNode、MetaNode、Blobstore等模块。
> 我在社区中负责Master和MetaNode模块相关功能的开发，累计提交了 60+ 的PR。
>
>
> 具体的工作如下：
>
> * 对Master模块进行优化，加速快照应用和Client Id分配。
> * 添加查询DataNode和MetaNode的负载的功能，减轻运维负担。
> * 重构副本放置算法，并加入多种新算法（CarryWeight、Ticket、RoundRobin、AvaliableSpaceFirst、Straw2），提供更为丰富的功能以应对复杂的场景。
> * 添加主动禁止卷写入的功能，与卷迁移功能对接。
> * 添加设置DataNode数据分区限制的功能，支持运维根据具体情况做出调整。
> * 添加后端审计日志并支持通过Master进行卷级别配置。
> * 优化MetaNode更新VolumeView逻辑，合并多个RPC减少Master负载。
> * 优化Panic处理，确保在程序崩溃之前Log能够Flush到磁盘上。
> * 修复相关模块的多个BUG并完善相关模块的单测。
>
> ## Curve
>
>
> **项目简介：** Curve 是网易主导自研的现代化存储系统, 目前支持文件存储(CurveFS)和块存储(CurveBS)。现作为沙箱项目托管于CNCF。
>
> **社区角色：** Contributor
>
> **项目日期：** 2023/8 - 至今
>
> **主要贡献:**
>
> * 修复了不能在GCC 11上编译的BUG。
> * 支持元数据服务进行异步的 Raft Snapshot。
> * 修复Google log打印到`docker logs`的BUG（这个BUG导致日志双写）。
>
> ### Rkv
>
> **项目简介：** 使用C++编写的基于MultiRaft的简单键值存储系统，面向大量小键设计，提供基于范围的自动分区。
>
> **项目日期：** 2022/4 - 2022/6
>
> **项目角色：** 开发者
>
>## 自我评价
>
> 本人具有良好的团队协作意识和学习自驱力，对于开源事业有着持续的投入，对于分布式存储技术有浓厚的兴趣。本人对于代码有效率优化意识，平时在分布式文件系统领域较为投入，算法和数据结构知识良好，有责任心和担当意识。