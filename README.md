## Open Source Promotion Plan - Summer 2020 Tasks

### 开源软件供应链点亮计划-暑期2020背景介绍

“开源软件供应链点亮计划-暑期2020”（以下简称 暑期2020）是由中科院软件所与 openEuler 社区共同举办的一项面向高校学生的暑期活动，旨在鼓励在校学生积极参与开源软件的开发维护，促进国内优秀开源软件社区的蓬勃发展。

该计划将联合各大开源社区，针对重要开源软件的开发与维护提供 mini 项目，并向全国高校学生开放报名。学生可自主选择感兴趣的项目进行申请，并在中选后获得该软件资深维护者（社区导师）亲自指导的机会。根据项目的难易程度和完成情况，参与者还可获取“开源软件供应链点亮计划-暑期2020”活动奖金和奖杯。

**“暑期2020”项目在今年（2020）首次举办，与Google Summer of Code类似，不同点是“暑期2020”只允许中国学生参加，可以看做中国版的GSoC。**

1. 官网：https://isrc.iscas.ac.cn/summer2020
2. 官方新闻：http://www.iscas.ac.cn/xshd2016/xshy2016/202004/t20200426_5563484.html

### 活动的主要参与方有哪些？

活动组织方：中国科学院软件研究所、openEuler 社区主办，中国科学院软件研究所中国科学院软件研究所南京软件技术研究院，华为技术有限公司、中科软科技股份有限公司、深圳华锐金融技术股份有限公司等公司协办，此外，活动组组委会还联合国内公司、科研院所和各大高校共同推广此次活动。

活动参与方主要角色为学生、社区和导师。

1. 学生：学生自由选择项目，与导师沟通实现方案并撰写项目计划书。被选中的学生将在导师指导下，按计划完成开发工作，并将成果贡献给社区。社区评估学生的完成度，主办方根据评估结果发放资助金额给学生。
2. 社区：社区提供项目列表和描述，并安排项目对应的导师，导师与申请者沟通方案、并从申请者中选中一位承接项目。在为期三个月的开发周期中，导师指导学生进行对应项目的开发工作。
3. 导师：社区针对每一个项目指定一个导师，与学生一起制定合适的开发计划和方案，指导学生按计划完成开发。

### 项目的奖金额度是多少？

项目难度分为高、中、低三档，对应税前奖金分别为高（12000 元）、中（9000 元）、低（6000 元）。

## ChubaoFS项目介绍

![ChubaoFS](chubaofs.png)

ChubaoFS是一个开源，开放的云原生存储平台，提供分布式文件系统与对象存储服务，为云原生应用提供计算与存储分离的持久化存储方案。 ChubaoFS提供通用存储引擎，支持多种读写模型，支持多租户，针对小文件处理做了专门的优化，兼容POSIX协议以及S3协议，是可以实现一份数据通过多种接口访问。

ChubaoFS设计相关论文被国际顶级数据库会议SIGMOD2019发表： CFS: A Distributed File System for Large Scale Container Platforms. SIGMOD‘19, June 30-July 5, 2019, Amsterdam, Netherlands. https://dl.acm.org/citation.cfm?doid=3299869.3314046

目前ChubaoFS 已经是国际顶级基金会CNCF（Cloud Native Computing Foundation）的Sandbox项目： https://www.cncf.io/sandbox-projects/ 

更多具体项目信息可以参考ChubaoFS项目官网：https://www.chubao.io/

## 项目列表

### 1. 基于DataFusion和ChubaoFS的存储计算分离

- 项目题目: 基于DataFusion和ChubaoFS的存储计算分离
- 项目描述: 在ChubaoFS创建一个基于DataFusion的compute node, 并提供基于ChubaoFS存储节点的SQL服务,使用户可通过SQL在ChubaoFS中存储的非结构化文件中检索信息。
- 难度: `高`
- 社区项目导师: Dr. Wei Ding
- 导师联系方式: [wei.ding@jd.com](mailto:wei.ding@jd.com)
- 项目产出要求: 完成源码开发并且demo基本的SQL操作
- 项目技术要求：Rust, Go
- 相关仓库地址: 
    - https://github.com/apache/arrow/tree/master/rust/datafusion
    - https://github.com/chubaofs

### 2. 基于DataFusion和ChubaoDB的存储计算分离

- 项目题目: 基于DataFusion和ChubaoDB的存储计算分离
- 项目描述: 在ChubaoFS创建一个基于DataFusion的compute node并提供基于ChubaoDB的SQL服务。
- 难度: `高`
- 社区项目导师: Dr. Wei Ding
- 导师联系方式: [wei.ding@jd.com](mailto:wei.ding@jd.com)
- 项目产出要求: 完成源码开发并且demo基本的SQL操作
- 项目技术要求: 
    - Rust
    - Go
- 相关仓库地址:
    - https://github.com/chubaofs/chubaodb     
    - https://github.com/apache/arrow/tree/master/rust/datafusion

### 3. 分布式文件系统ChubaoFS测试框架

- 项目标题: 分布式文件系统ChubaoFS测试框架
- 项目描述: ChubaoFS是云原生的分布式文件系统及对象存储，提供高可用可扩展的分布式存储服务。如何对分布式系统进行有效的自动化测试至关重要，是项目稳定性重要保证，可缩短发布周期和及时发现低概率问题。
- 项目难度: `中`
- 项目社区导师: Zhengyi Zhu
- 导师联系方式: [zhengyi.zhu.hust@gmail.com](mailto:zhengyi.zhu.hust@gmail.com)
- 项目产出要求:
   - 基于docker环境搭建的分布式测试框架
   - 基于ChubaoFS的有针对性的测试用例
- 项目技术要求:
   - 熟练使用docker命令
   - 对一致性复制协议有一定了解，主从复制协议，raft
   - 具备一种脚本语言，如 Python、Bash script 等
- 相关的开源软件仓库列表:
   - github.com/chubaofs/chubaofs


### 4. 基于Raft和Rocksdb实现一个简单的分布式Key-Value数据库   

- 项目题目: 基于Raft和Rocksdb实现一个简单的分布式Key-Value数据库
- 项目描述: 利用已有的Raft和Rocksdb，组合实现最终一致的分布式Key-Value数据库软件。效果类似etcd或者是zookper。
- 项目难度: `中`
- 项目设计导师: Jian Sun
- 导师联系方式: [ansj-sun@163.com](mailto:ansj-sun@163.com)
- 项目产出要求: 
    - 完成源码开发及相关测试用例
    - 实现CRUD的基本功能。 
- 项目技术要求:
    - 熟练使用Rust语言
    - 熟悉Raft算法
- 相关仓库地址: 
    - https://github.com/chubaofs/chubaodb
    - https://github.com/tiglabs/raft

### 5. ChubaoFS项目文档重构

- 项目题目: ChubaoFS项目文档重构
- 项目描述: 对当前项目的中英文文档的结构进行重新组织，优化文档结构并补充缺少的的内容。包括项目的设计文档、管理员手册、用户文档、FAQ等主题。
- 难度: `中`
- 项目社区导师: Mofei Zhang
- 导师联系方式: [mofei2816@gmail.com](mailto:mofei2816@gmail.com)
- 项目产出要求： 
   1. 完成英文文档结构梳理并优化文档结构。
   2. 完成中文文档结构梳理并优化文档结构。
- 项目技术要求：
   - Markdown
   - Restructured text (rst)
- 相关仓库地址: 
   - https://github.com/chubaofs/chubaofs
   - https://github.com/chubaofs/docs-zh

### 6. 分布式文件系统ChubaoFS命令行管理工具

- 项目标题: 分布式文件系统ChubaoFS命令行管理工具
- 项目描述: ChubaoFS是云原生的分布式文件系统及对象存储，基于http协议提供了丰富的资源管理接口。将这些接口整合和封装到基于Linux操作系统的命令行客户端，对于ChubaoFS分布式文件系统易用性提升、推广和普及具有十分重要的意义。
- 项目难度：`中`
- 项目社区导师：Xihao Xu
- 导师联系方式: [xxscott@163.com](mailto:xxscott@163.com)
- 项目产出要求:
    - 命令行客户端基本覆盖ChubaoFS官方文档提供的接口
    - 命令行客户端在Linux终端的显示风格一致、易读性高
- 项目技术要求：
    - 熟悉docker命令
    - 熟悉Linux操作系统常用命令
    - 熟练使用golang编程语言
    - 有cobra命令行框架开发经验者优先
- 相关仓库地址: github.com/chubaofs/chubaofs

### 7. ChubaoFS的高级检索引擎ChubaoDB集群调度

- 项目题目: ChubaoFS的高级检索引擎ChubaoDB集群调度
- 项目描述： ChubaoDB是ChubaoFS的高级数据检索引擎，是基于ChubaoFS的检索服务。对ChubaoDB的集群调度进行设计和开发，平衡集群资源的负载。
- 难度：高
- 项目社区导师: Jian Sun
- 导师联系方式: [ansj-sun@163.com](mailto:ansj-sun@163.com)
- 项目产出要求: 搭建调度环境，模拟各种情况，产出规则算法
- 项目技术要求: Rust
- 相关仓库地址: https://github.com/chubaofs/chubaodb

### 8. 基于Rook在Kubernetes集群中部署ChubaoFS Console

- 项目题目: 基于Rook在Kubernetes集群中部署ChubaoFS Console
- 项目描述: 服务容器化已成为部署服务的主流方式，Kubernetes作为管理容器化的工作负载和服务最流行的平台，拥有庞大且快速成长的生态系统。一个Kubernetes集群中能够部署多少应用，除了受限于CPU和内存外，还会受限与磁盘空间，尤其是需要大量数据存储需求的应用。本项目希望基于Rook实现在Kubernetes集群中更加简单高效的部署和运维ChubaoFS Console。
- 难度: `高`
- 项目社区导师: Chengyu Liu
- 导师联系方式: [liuchengyu@jd.com](mailto:liuchengyu@jd.com)
- 项目产出要求:
   1. 完成Rook ChubaoFS Console的开发，实现ChubaoFS Console基于Rook的方式进行安装
   2. 实现ChubaoFS Console基于Rook的方式进行升级
   3. 实现ChubaoFS Console基于Rook的方式进行卸载
- 项目技术要求：
   1. Golang
   2. Kubernetes
   3. Docker
   4. Shell
- 相关仓库地址: 
   - https://github.com/chubaofs/chubaofs
   - https://github.com/kubernetes/kubernetes
   - https://github.com/kubernetes/client-go
   - https://github.com/rook/rook

### 9. 基于Rook在Kubernetes集群中部署ChubaoFS CSI 

- 项目题目: 基于Rook在Kubernetes集群中部署ChubaoFS CSI
- 项目描述: 服务容器化已成为部署服务的主流方式，Kubernetes作为管理容器化的工作负载和服务最流行的平台，拥有庞大且快速成长的生态系统。一个Kubernetes集群中能够部署多少应用，除了受限于CPU和内存外，还会受限与磁盘空间，尤其是需要大量数据存储需求的应用。本项目希望基于Rook实现在Kubernetes集群中更加简单高效的部署和运维ChubaoFS-CSI。
- 难度: `高`
- 项目社区导师：Xihao Xu
- 导师联系方式: [xxscott@163.com](mailto:xxscott@163.com)
- 项目产出要求: 
   1. 完成Rook ChubaoFS CSI的开发，实现ChubaoFS CSI基于Rook的方式进行安装
   2. 实现ChubaoFS CSI基于Rook的方式进行升级
   3. 实现ChubaoFS CSI基于Rook的方式进行卸载
   4. 实现Kubernetes应用正常使用ChubaoFS CSI创建的PVC
- 项目技术要求：
   1. Golang
   2. Kubernetes
   3. Docker
   4. Shell
- 相关仓库地址: 
   - https://github.com/chubaofs/chubaofs
   - https://github.com/kubernetes/kubernetes
   - https://github.com/kubernetes/client-go
   - https://github.com/rook/rook

### 10. 基于Rook在Kubernetes集群中部署ChubaoFS

- 项目题目: 基于Rook在Kubernetes集群中部署ChubaoFS
- 项目描述: 服务容器化已成为部署服务的主流方式，Kubernetes作为管理容器化的工作负载和服务最流行的平台，拥有庞大且快速成长的生态系统。一个Kubernetes集群中能够部署多少应用，除了受限于CPU和内存外，还会受限与磁盘空间，尤其是需要大量数据存储需求的应用。本项目希望基于Rook实现在Kubernetes集群中更加简单高效的部署和运维ChubaoFS。
- 难度: `高`
- 项目社区导师: Chengyu Liu
- 导师联系方式: [liuchengyu@jd.com](mailto:liuchengyu@jd.com)
- 项目产出要求： 
   1. 完成Rook ChubaoFS的开发，实现ChubaoFS基于Rook的方式进行安装
   2. 实现ChubaoFS基于Rook的方式进行升级
   3. 实现ChubaoFS基于Rook的方式进行卸载
- 项目技术要求：
   1. Golang
   2. Kubernetes
   3. Docker
   4. Shell
- 相关仓库地址: 
   - https://github.com/chubaofs/chubaofs
   - https://github.com/kubernetes/kubernetes
   - https://github.com/kubernetes/client-go
   - https://github.com/rook/rook

### 11. 基于Rook在Kubernetes集群中部署ChubaoFS Monitor

- 项目题目: 基于Rook在Kubernetes集群中部署ChubaoFS Monitor
- 项目描述: 服务容器化已成为部署服务的主流方式，Kubernetes作为管理容器化的工作负载和服务最流行的平台，拥有庞大且快速成长的生态系统。一个Kubernetes集群中能够部署多少应用，除了受限于CPU和内存外，还会受限与磁盘空间，尤其是需要大量数据存储需求的应用。本项目希望基于Rook实现在Kubernetes集群中更加简单高效的部署和运维ChubaoFS Monitor。
- 难度: `高`
- 项目社区导师: Chengyu Liu
- 导师联系方式: [liuchengyu@jd.com](mailto:liuchengyu@jd.com)
- 项目产出要求： 
   1. 完成Rook ChubaoFS Monitor的开发，实现ChubaoFS Monitor基于Rook的方式进行安装
   2. 实现ChubaoFS Monitor基于Rook的方式进行升级
   3. 实现ChubaoFS Monitor基于Rook的方式进行卸载
- 项目技术要求：
   1. Golang
   2. Kubernetes
   3. Docker
   4. Shell
- 相关仓库地址: 
   - https://github.com/chubaofs/chubaofs
   - https://github.com/kubernetes/kubernetes
   - https://github.com/kubernetes/client-go
   - https://github.com/rook/rook


## 候选人要求

### 工作职责：

- 每周与项目导师进行线上讨论，完成项目规定的开发任务。项目导师由开源项目创始人或其他核心成员担任；
- 积极参与开源社区的建设，参与代码提交、解决Issue、审核PR等日常工作；
- 配合完成官方要求的材料提交等事项，包括项目申请书撰写、社区反馈任务完成度追踪等。

### 职位要求：

- 本科、硕士或博士在读（已毕业、工作的无法参加）；
- 对开源软件、开源社区感兴趣；
- 熟悉一种或多种编程语言，有较强的工程能力，代码格式清晰规范，善于团队协作；
- 有一定英文读写能力，能够熟练运用英语在GitHub进行开发、协作；
- 较强的沟通能力和逻辑表达能力。

### 具有以下条件者优先：

- 熟悉Go, Rust等语言、分布式系统、存储系统，有相关项目开发经验；
- 熟悉计算机网络，有相关开发经验；
- 熟悉Kubernetes、Docker，有相关项目开发经验；
- 熟悉Raft算法，有相关项目开发经验;
- 熟悉SQL及其语法解析，有相关项目开发经验；
- 熟悉POSIX标准，有相关存储类项目开发经验；
- 在GitHub较为活跃，有自己的开源项目，或参与过知名开源项目；
- 可以在项目结束后继续长期参与开源社区的开发、建设或维护。

## 投递要求

申请学生需要同时完成以下“联系社区”和“官网投递”两个环节：

### 1. 联系社区（2020年5月15日至6月20日）
进入**Summer 2020 - ChubaoFS**微信群与社区导师沟通<br>
<img src="wechat.jpeg" alt="Summer 2020 - ChubaoFS" width="250">

### 2. 官网投递（2020年6月1日至6月20日）

详见：https://isrc.iscas.ac.cn/summer2020/help/student.html#学生如何报名
