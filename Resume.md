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
 - 21岁，男
 - 求职意向：分布式存储工程师
 - 工作经验：1 年
 <!-- - 期望薪资：0k（校招可不填） -->

## <img src="assets/graduation-cap-solid.svg" width="30px"> 教育经历

<!-- - 硕士，XXXX大学，计算机科学与技术专业，2016.9~2019.7 -->
- 学士，成都信息工程大学，区块链工程专业，2021.9~2025.7

## <img src="assets/tools-solid.svg" width="30px"> 个人优势

- CNCF 毕业项目 CubeFS Committer **(4.7k stars，贡献 70+ PR)**，CNCF 沙盒项目 Curve Contributor **(2.3k stars)**。
- 熟练使用 C++、Go，了解 Rust，参与过大规模分布式系统的研发。
- 熟悉常见数据结构与算法，了解常见异步 I/O 技术：libaio、io_uring。
- 熟悉 CubeFS、Curve、Ceph 等分布式存储系统，熟悉 Raft 算法和分布式事务（2PC）。

## <img src="assets/briefcase-solid.svg" width="30px"> 工作经历

- **小米 分布式存储工程师 2025.5 - 至今**<br/>
    负责 JuiceFS 小米版元数据引擎的核心功能研发：
        * 研发自动均衡与 AppDomain 功能，突破单集群扩展瓶颈，**支撑单集群文件数提升至 3000 亿**。
        * 研发 Raft Learner 模块，重构 Region 迁移流程，显著提升元数据层容灾能力，**实现故障自动检测与自愈, 90%的下线流程不再需要人工介入**。
        * 研发跨 Region 分布式事务 Rename， 使用Spanner风格2PC，**保障文件系统重命名操作的原子性与一致性, 避免目录树成环**。

## <img src="assets/briefcase-solid.svg" width="30px"> 实习经历

- **OPPO 后端工程师 2024.1 - 2024.6**<br/>
    负责分布式文件系统 CubeFS 的核心功能研发：
        * 提升 HDD 环境下 DataNode 的启动速度，**将启动时间从 3 分钟缩短到 20 秒**。
        * 优化 DataNode 选盘算法，**兼顾磁盘剩余容量的同时尽可能打散 DataPartition**。
        * 研发 MetaNode 元数据 RocksDB 持久化功能，**降低元数据存储成本**。
        * 研发 DataNode 坏盘自动迁移功能并修复多个线上问题，**减少运维人工投入，实现自动化迁移**。

- **搜狐 SRE 工程师 2023.10 - 2023.12**<br/>
    负责调优和维护 Ceph 存储集群：
        * 优化 RBD Cache 配置，充分利用机器空闲内存，**将虚拟机磁盘性能提升 3 倍**。
        * 针对 CephFS 大目录删除缓慢问题提出优化方案，**以 mv 替代 rm + 后台异步回收，提升内部 DevOps 工具性能**。
        * 配置生产集群 Ceph 报警规则。

## <img src="assets/project-diagram-solid.svg" width="30px"> 项目经历

- **CubeFS**<br/>
  CubeFS是一种新一代云原生存储系统, **主要使用golang编写** ，支持S3、HDFS和POSIX等访问协议， **被OPPO、京东、网易等厂商广泛使用，现作为毕业项目托管于CNCF。** <br/>
  项目网址： http://github.com/cubefs/cubefs

- **Curve**<br/>
  Curve 是网易主导的自研的 **主要使用C++编写** 的现代化存储系统, 目前支持文件存储(CurveFS)和块存储(CurveBS)。 **Curve在网易内部广泛使用，现作为沙箱项目托管于CNCF。**<br/>
  主要贡献：<br/>
    负责开发 CurveFS Metaserver 的异步Raft Snapshot功能。<br/>
  项目网址：https://github.com/opencurve/curve
<!-- 
- **基于 Raft 的键值存储**<br/>
  使用 **C++开发** 的键值存储系统 。阅读了Raft论文，基于 Raft 算法实现高可用的分布式键值存储系统，支持数据分片以提高扩展性与性能，经过了强杀测试和SIGSTOP/SIGCONT测试。<br/>
  采用领导选举和日志复制确保数据一致性，使用rpc实现高效通信。存储层采用仿制Leveldv的LSM Tree存储数据，底层采用io_uring和协程。<br/>
  项目网址：https://github.com/NaturalSelect/Rkv -->