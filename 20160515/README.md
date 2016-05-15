**TiDB Weekly**

   2016/5/15 第 10 期

欢迎浏览本期 TiDB Weekly。[TiDB](https://github.com/pingcap/tidb) 是一个分布式 SQL 数据库。灵感来自于 Google 的 [F1](http://research.google.com/pubs/pub41344.html) 和 [Spanner](http://research.google.com/archive/spanner.html)，TiDB 支持包括传统 RDBMS 和 NoSQL 的特性。这里是对 TiDB 项目及社区的每周消息汇总。如果要投稿，请关注 Twitter [@](https://twitter.com/ThisWeekInRust)[PingCAP](https://twitter.com/PingCAP) 或者发送邮件到 [weekly@pingcap.com](mailto:weekly@pingcap.com)。[欢迎参与 TiDB 项目](https://github.com/pingcap/tidb/blob/master/CONTRIBUTING.md)以及[《从零开始写分布式数据库》](https://github.com/ngaut/builddatabase)。

**点击[此处](http://eepurl.com/bT1FAv)进行邮件订阅**

# **TiDB 社区动态**

## **新闻 & 文章**

* 5/7 日举办第 7 次 NewSQL Meetup，[黄东旭](http://weibo.com/c4pt0r?is_all=1)分享[《CalvinDB 解析: Modern Distributed Transaction Scheduler》](Calvin_Slides.pptx)，[韩飞](https://github.com/hanfei19910905)分享[《TiDB 新版查询优化器设计》](tidb_optimization.pdf)
* 5/14 日举办第 8 次 NewSQL Meetup，张帅分享[《两阶段提交优化》](2pc.pdf)，刘奇分享《分布式数据库开发中遇到的那些坑》
* 5/14  [DTCC 2016](http://dtcc.it168.com/jiabin.html)，[黄东旭](http://weibo.com/c4pt0r?is_all=1)：[《使用 Raft 构建分布式 OLTP 之路》](https://mp.weixin.qq.com/s?__biz=MzI3NDIxNTQyOQ==&mid=2247483687&idx=1&sn=62d344b14e2501a34f5785f8f3f3dfb7&scene=1&srcid=0514SXYXkMKE6i6Ew3lhiux5&key=b28b03434249256b4fa64da661479af3c487e85bff08378b031296edd1e446f6eda857c66002a5b1ed6a24ba2a7301be&ascene=0&uin=MjMwNjY5NzY2MA%3D%3D&devicetype=iMac+MacBookPro11%2C1+OSX+OSX+10.11.4+build(15E65)&version=11020201&pass_ticket=1OO6mfQH4DrAqcfSs3QZ4hzqCW8s96rS8%2B%2F7TZ6SlmCXtYEaz98iH4rdtYDGxgFd)

# **TiDB 项目动态**

共 [Merge 33 个 PR](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2016-05-04..2016-05-15+) 

* 分布式 SQL 支持 Limit、逆序扫索引，提高计算并行度，性能大幅提升
* 修复 Bug，提高对 MySQL 协议/语法的兼容性

**新增Contributor：**
* [Ivan.Yang](https://github.com/hanfei19910905) 来自上海交通大学

# **近期事件**

* 2016/06/24 [HKOSCon 2016](http://2016.opensource.hk/)，[刘奇](http://weibo.com/chuangyiyongpin?is_all=1)：《How to build a NewSQL database》

# **技术新闻 & 文章**

* [SQL vs. NoSQL Databases: What’s the Difference?](https://www.upwork.com/hiring/data/sql-vs-nosql-databases-whats-the-difference/)
* [Understanding Go's `nil` value](http://www.gmarik.info/blog/2016/understanding-golang-nil-value/)
* [Using, Abusing and Scaling MySQL at Flickr](http://code.flickr.net/2010/02/08/using-abusing-and-scaling-mysql-at-flickr/)
* [史上最全的"大数据"学习资源](https://yq.aliyun.com/articles/37308)

# **加入 PingCAP**

分布式数据库是一个高难度又令人着迷的领域，前方路上还有很多未知的困难和挑战，我们深信只有找到最优秀的人同行，方能走远。盼望各路大牛加入 PingCAP，和我们一起为数据库技术、开源事业做出一些贡献，同时也能实现自身的财务自由。

具体信息参见[职位介绍](http://www.lagou.com/gongsi/j113568.html)，有意者请联系[hire@pingcap.com](mailto:hire@pingcap.com)。