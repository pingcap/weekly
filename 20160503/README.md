**TiDB Weekly**

   2016/5/03 第9期

欢迎浏览本期 TiDB Weekly。[TiDB](https://github.com/pingcap/tidb) 是一个分布式 SQL 数据库。灵感来自于 Google 的 [F1](http://research.google.com/pubs/pub41344.html) 和 [Spanner](http://research.google.com/archive/spanner.html)，TiDB 支持包括传统 RDBMS 和 NoSQL 的特性。这里是对 TiDB 项目及社区的每周消息汇总。如果要投稿，请关注 Twitter [@](https://twitter.com/ThisWeekInRust)[PingCAP](https://twitter.com/PingCAP) 或者发送邮件到 [weekly@pingcap.com](mailto:weekly@pingcap.com)。[欢迎参与 TiDB 项目](https://github.com/pingcap/tidb/blob/master/CONTRIBUTING.md)以及[《从零开始写分布式数据库》](https://github.com/ngaut/builddatabase)。

**点击**[此处](http://eepurl.com/bT1FAv)**进行邮件订阅**

# **TiDB 社区动态**

## **新闻 & 文章**

* 4/23 日举办 TiDB 第 6 次线下 Meetup，[周煜行](https://github.com/coocood)分享《TiDB 中如何使用索引》，[黄梦龙](https://github.com/disksing)分享《TiDB/TiKV 如何实现分布式查询》
* PingCAP 与 海尔电商技术人员交流 NewSQL 相关技术，并对 TiDB 的实现细节进行讨论
* 2014/04/23 QCon Beijing，黄东旭：[《基础软件开源与创业在中国》](http://2016.qconbeijing.com/presentation/2808)
* PingCAP Golang 实践经验分享：[《Golang In PingCAP》](http://mp.weixin.qq.com/s?__biz=MjM5OTcxMzE0MQ==&mid=2653369705&idx=1&sn=ec1d9a6bca390059aad77baeebf49934#rd)
* PingCAP 被收入 [Rust 语言成功案例](https://www.rust-lang.org/friends.html)

# **TiDB 项目动态**

共 [Merge 54 个 PR](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2016-04-16..2016-05-03+) 
* 分布式 SQL 支持 Subquery、Limit/Offset 算子、Like/In 表达式，查询性能大幅提升
* TiDB 支持通过本地 unixsocket 方式访问，支持原生的 MySQL Driver
* TiDB 使用 vendor 机制解决依赖

新增Contributor：
* [hanfei](https://github.com/hanfei19910905) 来自 PingCAP
* [zyguan](https://github.com/zyguan) 来自电子科技大学

# **近期事件**

* 2016/05/14 [DTCC 2016](http://dtcc.it168.com/jiabin.html)，[黄东旭](http://weibo.com/c4pt0r?is_all=1)：《使用 Raft 构建分布式 OLTP 之路》
* 2016/06/24 [HKOSCon 2016](http://2016.opensource.hk/)，[刘奇](http://weibo.com/chuangyiyongpin?is_all=1)：《How to build a NewSQL database》

# **技术新闻 & 文章**

* [MemSQL 获得 3600w 美元 C 轮融资](http://techcrunch.com/2016/04/21/memsql-raises-36m-series-c-round-for-its-in-memory-database-platform/)
* [单表 60 亿记录等大数据场景的 MySQL 优化和运维之道](http://gold.xitu.io/entry/5716e28aebcb7d005cac1634)
* [Go best practices](https://peter.bourgon.org/go-best-practices-2016/)

# **加入 PingCAP**

分布式数据库是一个高难度又令人着迷的领域，前方路上还有很多未知的困难和挑战，我们深信只有找到最优秀的人同行，方能走远。盼望各路大牛加入 PingCAP，和我们一起为数据库技术、开源事业做出一些贡献，同时也能实现自身的财务自由。

具体信息参见[职位介绍](http://www.lagou.com/gongsi/j113568.html)，有意者请联系[hire@pingcap.com](mailto:hire@pingcap.com)。
