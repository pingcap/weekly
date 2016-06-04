**TiDB Weekly**

   2016/6/04 第 11 期

欢迎浏览本期 TiDB Weekly。[TiDB](https://github.com/pingcap/tidb) 是一个分布式 SQL 数据库。灵感来自于 Google 的 [F1](http://research.google.com/pubs/pub41344.html) 和 [Spanner](http://research.google.com/archive/spanner.html)，TiDB 支持包括传统 RDBMS 和 NoSQL 的特性。这里是对 TiDB 项目及社区的每周消息汇总。如果要投稿，请关注 Twitter [@](https://twitter.com/ThisWeekInRust)[PingCAP](https://twitter.com/PingCAP) 或者发送邮件到 [weekly@pingcap.com](mailto:weekly@pingcap.com)。[欢迎参与 TiDB 项目](https://github.com/pingcap/tidb/blob/master/CONTRIBUTING.md)以及[《从零开始写分布式数据库》](https://github.com/ngaut/builddatabase)。

**点击**[此处](http://eepurl.com/bT1FAv)**进行邮件订阅**

# **TiDB 社区动态**

## **新闻 & 文章**

* 5/21 日举办第 9 次 NewSQL Meetup，[刘奇](http://weibo.com/chuangyiyongpin?is_all=1)分享[《 TiKV MVCC 和 GC 实现》](MVCC_GC.pptx)，[韩飞](https://github.com/hanfei19910905)分享[《 SQL 子查询优化》](QueryOptimization.pptx)
* 5/28 日举办第 10 次 NewSQL Meetup，[刘奇](http://weibo.com/chuangyiyongpin?is_all=1)分享《 TiKV 的网络模拟测试》，[周昱行](https://github.com/coocood)分享《 TiDB 的条件下推优化》
* 5/29 日 36Kr 对 PingCAP 项目进行新闻报道：[《去IOE的又一利器，PingCAP打算创造一款更适合云计算的分布式数据库》](http://36kr.com/p/5047514.html#rd)
* 6/2 日开源中国对 CTO 黄东旭进行了个人专访，在"OSC 大咖说"栏目发表文章：[《写代码、玩开源，体会造物的成就感》](http://www.oschina.net/question/2652078_2182038#rd)
* 6/4 日举办第 11 次 NewSQL Meetup，[黄梦龙](https://github.com/disksing)分享[《 TiKV 的结构化存储模型优化》](TiKV的结构化存储模型优化.pptx)，张金鹏分享[《深入解析 LevelDB 》](leveldb.pdf)

# **TiDB 项目动态**

共 [Merge 44 个 PR](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2016-05-16..2016-06-04+) 
* 支持 HashJoin，在通用场景下，性能提升 10 倍以上
* 优化分布式 SQL，支持读写混合场景下的分布式 SQL
* 完善对 TiKV 的支持
* 优化存储模型，不需存储 Null 值，节省存储空间
* 修复 Bug，提高对 MySQL 协议/语法的兼容性

**新增Contributor：**

* [Zhang Yang](https://github.com/v01dstar) 来自南加州大学

# **近期事件**

* 2016/06/24 [HKOSCon 2016](http://2016.opensource.hk/)，[刘奇](http://weibo.com/chuangyiyongpin?is_all=1)：《How to build a NewSQL database》

# **技术新闻 & 文章**

* [Scaling to 100M: MySQL is a Better NoSQL](http://blog.wix.engineering/2015/12/10/scaling-to-100m-mysql-is-a-better-nosql/)
* [Go 1.7 Beta 1 is released](https://groups.google.com/forum/#!msg/golang-nuts/zndSPkE2DVE/bcOu35-OBwAJ)
* [PostgreSQL 9.6 并行度的源码分析](https://yq.aliyun.com/articles/44655#)

# **加入 PingCAP**

分布式数据库是一个高难度又令人着迷的领域，前方路上还有很多未知的困难和挑战，我们深信只有找到最优秀的人同行，方能走远。盼望各路大牛加入 PingCAP，和我们一起为数据库技术、开源事业做出一些贡献，同时也能实现自身的财务自由。

具体信息参见[职位介绍](http://www.lagou.com/gongsi/j113568.html)，有意者请联系[hire@pingcap.com](mailto:hire@pingcap.com)。
