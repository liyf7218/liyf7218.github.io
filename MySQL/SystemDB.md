# MySQL 系统数据库介绍

自带的4个系统数据库：information_schema、mysql、performance_schema、sys；

- information_schema
    这个数据库保存了mysql服务器所有数据库的信息。比如数据库的名、数据库的表、访问权限、数据库表的数据类型，数据库索引的信息等等。
- performance_schema
    主要用于收集数据库服务器性能参数，可用于监控服务器在一个较低级别的运行过程中的资源消耗、资源等待等情况。
    链接：[performance_schema全方位介绍](http://blog.woqutech.com/2018/04/03/%E5%88%9D%E7%9B%B8%E8%AF%86%EF%BD%9Cperformance_schema%E5%85%A8%E6%96%B9%E4%BD%8D%E4%BB%8B%E7%BB%8D/)
- sys
    库中所有的数据源来自：performance_schema。目标是把performance_schema的把复杂度降低，让DBA能更好的阅读这个库里的内容。让DBA更快的了解DB的运行情况。
    链接： [MYSQL的SYS数据库](https://blog.csdn.net/jayewu/article/details/80183274)
- mysql
    mysql的核心数据库，类似于sql server中的master表，主要负责存储数据库的用户、权限设置、关键字等mysql自己需要使用的控制和管理信息。
