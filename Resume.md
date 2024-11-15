 <center>
     <h1>黄志斌</h1>
     <div>
         <span>
             <img src="assets/phone-solid.svg" width="18px">
             15915145280
         </span>
         ·
         <span>
             <img src="assets/envelope-solid.svg" width="18px">
             2145973003@qq.com
         </span>
         ·
         <span>
             <img src="assets/github-brands.svg" width="18px">
             <a href="https://github.com/NaturalSelect">NaturalSelect</a>
         </span>
         <!--
         之后考虑启用
         ·
         <span>
             <img src="assets/rss-solid.svg" width="18px">
             <a href="#">My Blog</a>
         </span> -->
     </div>
 </center>

 ## <img src="assets/info-circle-solid.svg" width="30px"> 个人信息

 - 男，2003 年出生
 - 求职意向：后端工程师、运维工程师、测试工程师
 - CNCF 孵化项目 CubeFS Committer
 - CNCF 沙盒项目 Curve Contributor
 <!-- - 工作经验：0 年（校招可不填） -->
 <!-- - 期望薪资：0k（校招可不填） -->

## <img src="assets/graduation-cap-solid.svg" width="30px"> 教育经历

<!-- - 硕士，XXXX大学，计算机科学与技术专业，2016.9~2019.7 -->
- 学士，成都信息工程大学，区块链工程专业，2021.9~2025.7
- 绩点：3.0，年级前 30%
- 通过了 CET4 英语等级考试

## <img src="assets/tools-solid.svg" width="30px"> 技能清单

- 熟练使用C++、go、了解Java、Python。
- 熟悉常见数据结构与算法。
- 熟悉分布式存储系统： CubeFS、Curve、Ceph。
- 熟悉Raft算法和分布式事务。
- 了解常见I/O技术： libaio、io_uring。

## <img src="assets/briefcase-solid.svg" width="30px"> 工作经历

- **OPPO，互联网服务系统/云数能力中心/云计算部/存储技术组，后端工程师，2024.1～2024.6**

   开发和迭代分布式文件系统 CubeFS，参与3.3.2 3.4.0等版本的功能开发和缺陷修复。

   产出：
    - 优化DataNode在HDD环境下的启动速度， **使用镜像文件的方式将启动时间从3分钟缩短到20秒** 。
    - 优化DataNode的DataPartition放置算法， **兼顾磁盘剩余容量的同时尽可能打散负载** 。
    - 合并 MetaNode 获取卷信息的RPC以减少Master负载。

- **搜狐，大数据中心/基础架构团队，SRE工程师，2023.10～2023.12**

   调优和维护Ceph存储集群。

   产出：
     - 优化RBD Cache配置充分使用机器未使用的空闲内存，**将虚拟机磁盘性能提升3倍。**
     - 针对CephFS大目录删除缓慢问题提出优化方案，**使用mv代替rm + 后台异步回收的方式，提升内部DevOps工具性能。**
     - 配置生产集群Ceph报警规则。

<br/>

## <img src="assets/project-diagram-solid.svg" width="30px"> 项目经历

- **CubeFS** <sub><a href="https://cubefs.io/zh">cubefs.io</a></sub>

  CubeFS是一种新一代云原生存储系统, **主要使用golang编写** ，支持S3、HDFS和POSIX等访问协议， **被OPPO、京东、网易等厂商广泛使用，现作为孵化项目托管于CNCF。** 它广泛适用于各种场景，如大数据、AI/LLMs、容器平台、数据库和中间件的存储与计算分离、数据共享和保护等。

  贡献：
  * 负责开发 **MetaNode的 [Rocksdb持久化](https://github.com/cubefs/cubefs/tree/develop-v3.5.0-metanode_rocksdb) 功能（on 3.5.0 ROADMAP）**。
  * 参与CubeFS [3.3.0](https://github.com/cubefs/cubefs/releases/tag/v3.3.0)的研发：
    * DataNode 限制最大 DataPartition 数量。 [#1946](https://github.com/cubefs/cubefs/pull/1946)
  * 参与CubeFS [3.3.1](https://github.com/cubefs/cubefs/releases/tag/v3.3.1)的研发：
    * MetaNode 审计日志。 [#2642](https://github.com/cubefs/cubefs/pull/2642) [#2789](https://github.com/cubefs/cubefs/pull/2789) [#2837](https://github.com/cubefs/cubefs/pull/2837) [#3179](https://github.com/cubefs/cubefs/pull/3179)
    * 合并MetaNode 获取卷信息的RPC以减少Master负载。 [#2775](https://github.com/cubefs/cubefs/pull/2775)
  * 参与CubeFS [3.3.2](https://github.com/cubefs/cubefs/releases/tag/v3.3.2)的研发以及BUG修复：
    * 卷冻结功能。 [#2537](https://github.com/cubefs/cubefs/pull/2537) [#2584](https://github.com/cubefs/cubefs/pull/2584)
    * DataNode启动加速， **使用镜像文件的方式将启动时间从3分钟缩短到20秒** 。[#3341](https://github.com/cubefs/cubefs/pull/3341)
    * Inode删除审计日志滚动。[#3206](https://github.com/cubefs/cubefs/pull/3206)
    * Master Raft Snapshot优化。 [#2124](https://github.com/cubefs/cubefs/pull/2124) [#3146](https://github.com/cubefs/cubefs/pull/3146)
  * 参与CubeFS 3.4.0的研发以及BUF修复：
    * qosClientId 分配优化。 [#2112](https://github.com/cubefs/cubefs/pull/2112)
    * 采集DataNode和MetaNode的负载并展示。 [#2097](https://github.com/cubefs/cubefs/pull/2097)
    * 重构节点选择算法，提供更多算法适配多个场景。 [#2353](https://github.com/cubefs/cubefs/pull/2353) [#2569](https://github.com/cubefs/cubefs/pull/2569) [#2829](https://github.com/cubefs/cubefs/pull/2829)
    * Extent删除流程优化。 [#3170](https://github.com/cubefs/cubefs/pull/3170)
    * 磁盘放置 DataPartition 算法优化， **兼顾磁盘剩余容量的同时尽可能打散负载**。
    * 与mentor一起开发坏盘自动化迁移功能。

  <!-- 使用一两句话描述项目的主要功能，然后介绍自己在项目中的角色，解决了什么问题，使用什么方式解决，比别人的方法相比有什么优势（尽量用数据来说明）。 -->

- **Curve** <sub><a href="https://opencurve.io/Curve/HOME">opencurve.io</a> </sub>

  Curve 是网易主导的自研的 **主要使用C++编写** 的现代化存储系统, 目前支持文件存储(CurveFS)和块存储(CurveBS)。 **Curve在网易内部广泛使用，现作为沙箱项目托管于CNCF。**

  贡献：
  * 负责开发 CurveFS Metaserver 的异步Raft Snapshot功能。 [#2691](https://github.com/opencurve/curve/pull/2691)
  * 修复容器部署场景下docker logs的日志双写问题。 [#2869](https://github.com/opencurve/curve/pull/2869)

- **基于Raft的键值存储** <sub><a href="https://github.com/NaturalSelect/Rkv">github.com/NaturalSelect/Rkv</a></sub>
  * 使用 **C++开发** 的键值存储系统 。
  * 本项目基于 Raft 算法实现高可用的分布式键值存储系统，支持数据分片以提高扩展性与性能。
  * 采用领导选举和日志复制确保数据一致性，使用rpc实现高效通信。
  * 存储层采用LSM Tree存储数据。
