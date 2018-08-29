**关键字**
- ViewModel 视图模型
- DomainModel 领域模型
- DAL 数据访问层
- DAO 数据访问对象
- DataModel 数据模型
- field 字段
- property 属性

**学习线路**

1.基础编程->2.编程进阶->3.类库使用->4.框架使用->5.领域建模->6.设计模式->7.架构设计->8.平台设计

**技术网站**
- 入门培训：http://imooc.com, http://w3school.com.cn
- 进阶与社区：http://cnblogs.com, http://csdn.net
- 架构设计：http://www.infoq.com/cn/
- 开源与工具：http://oschina.net
- 项目管理：http://gitee.com

**DDD结构**
- 概念中的DDD
http://www.cnblogs.com/lori/archive/2013/02/05/2892605.html
- 经典三层：表现层、业务层、数据层
- DDD：表现层、应用层、领域层、基础设施层
- DDD~microsoft NLayerApp项目中的层次结构图
http://www.cnblogs.com/lori/archive/2013/02/21/2920641.html
http://kb.cnblogs.com/page/103962/

**架构、框架、模式和平台**
- 意义：设计模式、框架 的意义在于，代码复用，规范化。
- 设计模式(Design pattern)是一套被反复使用、多数人知晓的、经过分类编目的、代码设计经验的总结。使用设计模式是为了可重用代码、让代码更容易被他人理解、保证代码可靠性。 毫无疑问，设计模式于己于他人于系统都是多赢的，设计模式使代码编制真正工程化，设计模式是软件工程的基石，如同大厦的一块块砖石一样。http://baike.so.com/doc/4379170-4585358.html
- 区分什么是架构、框架、模式和平台
http://www.cnblogs.com/chehaoj/archive/2010/12/09/1901049.html
- 框架和类库的区别
http://www.cnblogs.com/wbqsln/archive/2012/07/02/2573713.html

**实践案例**
- EntityFramework之领域驱动设计实践 （一）
http://www.cnblogs.com/daxnet/archive/2010/07/07/1772581.html
- Unit Of Work（工作单元）模式探索
http://www.cnblogs.com/OceanEyes/archive/2012/10/29/UnitOfWork--ByEyes.html
- 企业模式之Unit Of Work模式
http://www.cnblogs.com/zxj159/p/3505457.html
- UnitOfWork模式 主要解决 数据持久化执行的 事务化 处理，保持数据完整。例如，多次持久化不同记录，要保持数据完整性，出错回滚。
场景1：转账功能，2个人相互转账，一个记录执行减法后持久化，另一个记录执行加法后持久化，这个时候必须2个记录执行都没有问题才能算完成执行。如果中间出现错误，就要回滚，所以要用到事务处理。当然不用模式的化，也可以在 数据提交之前做一个事务处理。设计模式的意义在于，代码复用，规范化。


.

