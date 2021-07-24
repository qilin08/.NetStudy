# .NetStudy(个人.Net学习记录)

借鉴大佬路线（https://www.processon.com/view/link/6050be8d1e0853179f62352b?pw=dotnetv5#outline）

- ### .NET技术栈

  1. #### .NET基础

     ##### - 类型语法+内存管理

     ###### 				值类型与引用类型、装箱与拆箱、浅拷贝与深拷贝

     ###### 				堆与栈的差异、GC垃圾回收机制、内存泄漏

     ##### - 字符串+集合+流

     ###### 		StringBuilder的作用、字符串驻留池、泛型的约束、序列化与反序列化

     ##### - 委托+事件+反射+特性

     ###### 				委托的基本原理、链式委托（多播委托）、事件的基本原理

     ###### 				反射的原理和基石、声明式编程、特性的使用范围

     ##### - 多线程开发

     ###### 				.NET中的线程池、线程的独享数据存储、同步块与同步索引、lock关键字、Mutex、Monitor、Semaphore

     ###### 				Task、async+await语法糖

     ##### - ADO.NET+WebService

     ###### 				数据库连接池基本原理、如何提高数据库连接池内的连接效率

     ###### 				SOAP、REST、XML、JSON

  2. #### ASP.NET

      ##### - ASP.NET WebForm

      ###### 				aspx、ashx、AutoPostback

      ###### 				Viewstate、Updatepanel、XmlHttpRequest

      ###### 				页面生命周期、HttpApplication、HttpModule、HttpHandler

      ##### - ASP.NET MVC

      ###### 				MVC的解读、HtmlHelper、Razor、Routing路由

      ###### 				Filter过滤器、Area区域、母版页

      ###### 				WebAPI与WCF的联系、MVC源码机制

      ##### - ASP.NET Core

      ###### 				ASP.NET Core Pipeline = Server + HttpHandler (Middlewares)

      ###### 				五大过滤器（Filters）

     1. Authorization Filter:授权过滤器，优先级最高，可实现 权限角色验证、登录授权 等操作
     2. Resource Filter:资源过滤器，可实现 资源缓存、防盗链 等操作
     3. Exception Filter:异常过滤器，可实现全局的 异常日志收集 等操作
     4. Action Filter:Action过滤器，可实现 执行操作日志、参数验证、权限控制 等一系列操作
     5. Result Filter:结果过滤器，可实现 格式化、大小写转换 等一系列操作

      ###### 				依赖注入（DI）

     1. IServiceCollection 负责注册

        Transient:每一次GetService都会创建一个新实例

        Scoped:在同一个Scope内只初始化一个实例

        Singleton:整个应用程序声明周期以内只创建一个实例

     2.  IServiceProvider 负责提供实例

      ###### 				推荐订阅：《.NET Core开发实战》

  3. #### ORM
     ##### - EF Core

     ###### 	性能优化实践

     1. AsNoTracking、EF.Functions.Like、自定义标量函数
     2. 显示编译查询（缓存查询直接复用）、上下文实例池（DbContextPool）

     ###### 	事务和并发冲突

     1. DbContextTransaction、DbTransaction
     2. 乐观锁（RowVersion）

     ###### 	读写分离

     1. 单个Context多连接字符串方案（主or从）

     ###### 	即时分析

     1. 为EF Core增加Logging扩展即时输出SQL语句

     ##### - 轻量级

     ###### 	Dapper:高性能、灵活可控

     ###### 	FreeSql:功能强大、扩展方便

  4. #### 单元测试

  5. #### 性能调优

- ### 常用中间件

- ### 常用数据库

  1. #### MySQL

  2. #### MSSQL

     ##### - 参考资料：《MSSQL技术内幕：T-SQL语言基础》、《MSSQL技术内幕：T-SQL查询》

     ##### - 体系结构、架构和对象

     ##### - T-SQL

     ###### 	查询、表表达式、集合运算

     ###### 	透视、逆透视、分组

     ###### 	数据修改、可编程对象

     ###### 	逻辑查询

     ##### - 事务与并发

     ###### 	事务的概念、ACID特性

     ###### 	锁定和阻塞

     1. 排它锁与共享锁

     ###### 	事务隔离级别

     1. READ UNCOMMITED（未提交读）、READ COMMITED（已提交读，默认隔离级别）
     2. REPEATABLE READ（可重复读）、SERIALIZEABLE（可序列化）
     3. SNAPSHOT（快照）和READ COMMITED SNAPSHOT（已经提交读隔离）

     ###### 	死锁

     1. 默认MSSQL选择选择终止做过的操作最少的事务进行回滚
     2. 手动设置优先级：会话选项DEADLOCK_PRIORITY设置为范围（-10到10）
     3. 如何避免死锁：改变访问资源的顺序、良好的索引设计	

  3. #### NoSQL

- ### 软件设计

