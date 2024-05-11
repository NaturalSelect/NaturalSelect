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
 - 求职意向：分布式存储工程师
 - CNCF 孵化项目 CubeFS Committer
 - CNCF 沙盒项目 Curve Contributor
 <!-- - 工作经验：0 年（校招可不填） -->
 <!-- - 期望薪资：0k（校招可不填） -->

## <img src="assets/graduation-cap-solid.svg" width="30px"> 教育经历

<!-- - 硕士，XXXX大学，计算机科学与技术专业，2016.9~2019.7 -->
- 学士，成都信息工程大学，区块链工程专业，2021.9~2025.7
<!-- - 绩点：***，年级前 100% -->
- 通过了 CET4 英语等级考试

## <img src="assets/briefcase-solid.svg" width="30px"> 工作经历

- **OPPO，互联网服务系统/云数能力中心/云计算部/存储技术组，后端工程师，2024.1~至今**

   开发和迭代分布式文件系统 CubeFS

- **搜狐，大数据中心/基础架构团队，SRE工程师，2023.10-2023.12**

   负责调优和维护Ceph存储集群

## <img src="assets/project-diagram-solid.svg" width="30px"> 项目经历

- **CubeFS** <sub><a href="https://cubefs.io/zh">cubefs.io</a></sub>

  CubeFS是一种新一代云原生存储系统, **主要使用golang编写** ，支持S3、HDFS和POSIX等访问协议， **被OPPO、京东、网易等厂商广泛使用，现作为孵化项目托管于CNCF。** 它广泛适用于各种场景，如大数据、AI/LLMs、容器平台、数据库和中间件的存储与计算分离、数据共享和保护等。

  贡献：
  * 负责开发 **MetaNode的Rocksdb持久化功能（on 3.6.0 ROADMAP）** 。
  * 参与CubeFS 多个版本的研发及BUG修复：
    * 3.4.0 节点选择算法，提供更多算法适配多个场景。
    * 3.4.0 Extent删除流程优化。
    * 3.4.0 磁盘放置算法优化， **避免大量Data Partition无视磁盘可用空间放置**。
    * 3.4.0 坏盘自动化迁移功能（与mentor一起开发）。
    * 3.3.2 卷冻结功能。
    * 3.3.2 DataNode启动加速， **从3分钟缩短到20秒** 。
    * 3.3.2 Inode删除审计日志滚动。
    * 3.3.1 MetaNode 审计日志。
    * 3.3.0 DataNode 限制最大 DataPartition 数量。

  <!-- 使用一两句话描述项目的主要功能，然后介绍自己在项目中的角色，解决了什么问题，使用什么方式解决，比别人的方法相比有什么优势（尽量用数据来说明）。 -->

- **Curve** <sub><a href="https://opencurve.io/Curve/HOME">opencurve.io</a> </sub>

  Curve 是网易主导的自研的 **主要使用C++编写** 的现代化存储系统, 目前支持文件存储(CurveFS)和块存储(CurveBS)。 **Curve在网易内部广泛使用，现作为沙箱项目托管于CNCF。**

  贡献：
  * 负责开发 CurveFS Metaserver 的异步Raft Snapshot功能。
  * 修复容器部署场景下docker logs的日志双写问题。


## <img src="assets/tools-solid.svg" width="30px"> 技能清单

- 熟练使用C++、go。
- 熟悉常见数据结构与算法。
- 熟悉分布式存储系统： CubeFS、Curve、Ceph。
- 熟悉Raft算法。
- 熟悉分布式事务。
- 熟练使用Linux系统。