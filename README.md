## 数据库复习总结      一单元

* 数据是经过数字化后由计算机进行处理的符号记录

* 数据库是长期存储在计算机内的、有组织的、可共享的大量数据的集合

* 数据处理是指对数据的收集、组织、存储、加工和传播等一系列操作。它是从已有数据出发，经过加工处理得到所需数据的过程

* 数据管理是指对数据的分类、组织、编码、存储、检索和维护工作
 
* 数据管理是数据处理的核心和基础

* 数据库管理系统(DBMS)是完成数据库建立、使用、管理和维护任务的系统软件。它建立在操作系统上，对数据进行管理的软件

* 手工管理阶段:
    - 数据不保留
    - 应用程序管理数据
    - 数据不共享
    - 数据没有独立性

* 文件系统阶段:
    - 数据可长期保存
    - 用文件系统管理数据
    - 数据可共享，但共享性较差
    - 数据与应用程序之间有了一点的独立性

* 数据库系统阶段：
    - 数据结构化
    - 数据共享性高
    - 数据独立性高
    - 统一的数据管理与控制:
        + 数据的完整性
        + 数据的安全性
        + 并发控制
    - 方便的用户接口

* 关系模型
    - 由一组关系组成
    - 每个关系的数据结构是一张规范的二维表
    - 表中的一行称为一个元组
    - 表中的一列称为属性
    - 唯一确定一个元组的属性组称为码
    - 主要操作包括查询与更新
    - 满足关系完整性约束条件
        + 实体完整性
        + 参照完整性
        + 用户定义的完整性
    - 优点
        + 建立在严格的数学基础上的
        + 数据结构简单、清晰、容易理解
        + 实体与实体之间的联系、操作的对象、操作的结果都是关系
        + 存取路径对用户透明，数据独立性和安全保密性更好，易于用户使用
    - 主要缺点是查询效率低，因此数据库管理系统要对查询优化

* 数据库系统(DBS)
    - 包含数据库的计算机系统
    - 一般由以下组成
        + 数据库
        + 数据库管理系统(及其开发工具)
        + 应用系统
        + 开发和使用数据库系统的人员
    - 主要由以下组成
        + 数据库
        + 硬件系统
        + 人员组成
    - 其整体结构(由上至下)
        + 人员
            * 用户、DBA(数据库管理员)、开发人员
        + 软件系统
            * 数据库应用软件
            * 应用开发工具
            * 数据库管理系统
            * 操作系统
        + 数据库
    - 软件系统
        + 数据库管理系统
        + 操作系统
        + 高级语言及其编译系统
        + 应用开发工具
        + 数据库应用软件

* 数据库管理系统(DBMS):
    - 数据(用户数据)
    - 元数据(系统数据、数据字典)
    - 存储管理器
        + 从数据存储器中获得或修改数据
        + 缓冲管理器(内存的管理、通过文件管理器获得数据块、选择存储的内存位置)
        + 文件管理器(跟踪磁盘上文件的位置、根据内存管理器的请求获得数据块)
    - 查询处理器
        + 预编译器(解析嵌入在宿主语言中的查询语句)
        + 编译器(对查询和更新语句优化，并转为底层命令)
        + 解释器(编译或解释模式更新，并将其记录在元数据中)
    - 事务管理器
        + 负责系统的完整性工作，确保事务的ACID特性，以及确保在出现故障时仍然保持一致
    - 结构示意图(由上至下)
        + 应用程序、查询、数据库模式
        + 查询处理器
        + 存储管理器、事务管理器
        + 数据与元数据
    - 工作模式
        + DBMS接受应用程序的数据请求和处理请求
        + 将该请求(高级指令模式)转换为机器码(底层指令)，并完成数据库的操作
        + 接收对数据库操作的结果，并对操作结果进行处理
        + 将处理结果返回给应用系统
    - 主要功能
        + 数据定义
        + 数据组织、存储和管理
        + 数据操作
        + 事务管理和运行管理
        + 数据库的维护

* 三级模式结构
    - 模式
        + 概念模式或逻辑模式，数据库中全体数据的逻辑结果和特征的描述
    - 内模式
        + 子模式或用户模式，用户所看到和使用的局部数据的逻辑结构和特征的描述
        + 一个数据库只有一个内模式，内模式由数据库管理系统提供的内模式描述语言定义
    - 外模式
        + 存储模式，数据物理结构和存储方式的描述，是数据库内部的表示方法，包括存储记录的物理表示、数据项的描述方法、数据存储的文件结构、索引、散列等存取方式和路径
        + 可以有多个外模式
    - 模式之间的格式的转化过程称为映像
    - 两级映像
        + 外模式/模式映像(局部逻辑结构与全局逻辑结构之间的对应关系)
        + 模式/内模式映像(全局逻辑结构与存储结构之间的对应关系)
    - 示意图(由上至下)
        + 用户
        + 外模式
        + 外模式/模式映像
        + 模式
        + 模式/内模式映像
        + 内模式
        + 文件
    - 数据库独立性
        + 应用程序与数据库的数据逻辑组织以及存储结构间的相互独立，数据的逻辑组织或存储结构发生变化不影响应用程序
        + 逻辑数据独立性是指外模式不会随着模式的改变而改变
        + 物理数据独立性是指模式不会随着内模式的改变而改变

* 