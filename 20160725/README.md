**TiDB Weekly**

   2016/07/25 第 10 期

欢迎浏览本期 TiDB Weekly。[TiDB](https://github.com/pingcap/tidb) 是一个分布式 SQL 数据库。灵感来自于 Google 的 [F1](http://research.google.com/pubs/pub41344.html) 和 [Spanner](http://research.google.com/archive/spanner.html)，TiDB 支持包括传统 RDBMS 和 NoSQL 的特性。这里是对 TiDB 项目及社区的每周消息汇总。如果要投稿，请关注 Twitter [@](https://twitter.com/ThisWeekInRust)[PingCAP](https://twitter.com/PingCAP) 或者发送邮件到 [weekly@pingcap.com](mailto:weekly@pingcap.com)。[欢迎参与 TiDB 项目](https://github.com/pingcap/tidb/blob/master/CONTRIBUTING.md)以及[《从零开始写分布式数据库》](https://github.com/ngaut/builddatabase)。

**点击**[此处](http://eepurl.com/bT1FAv)**进行邮件订阅**

# **TiDB 社区动态**

## **新闻 & 文章**

* 7/13 日，CTO [黄东旭](http://weibo.com/c4pt0r?refer_flag=1001030103_)受邀与 InfoQ 网友分享：[《基于 Raft 构建弹性伸缩的存储系统的一些实践》](http://mp.weixin.qq.com/s?timestamp=1469178831&src=3&ver=1&signature=BPww-x2-tVgeWbZykaSLA7Pqe-d7zJq-ULSdwNn6r108qU4X7iKMJGipnerRneB1Vk5Jz-417NzyJGKBxHJUOZDkQFKGxrM26QVYZdlGbTnDJ9binlDqscWgHTnqEvWbqFsPFJbDGUI40SmFM1mC28-K2O-liH0nu3fFmKklgDQ=)
* 7/14 日，Founder [崔秋](http://weibo.com/u/2032093082?topnav=1&wvr=6&topsug=1)做客 InfoQ 线上分享群，分享《云时代数据库的核心特点》
* 7/16 日举办第 16 次 NewSQL Meetup，来自京东的田琪分享的《Cool Extensions of Raft for NewSQL》，以及来自百度的孟圣智分享的《基于 Ceph 构建文件共享服务的实践》
* 7/17 日，"细说云计算"专访 CTO 黄东旭：[《黄东旭：还是写代码舒服|视频+文字》](https://mp.weixin.qq.com/s?__biz=MzI4MjE3MTcwNA==&mid=2664334662&idx=1&sn=7277349ce87986c9393fc654a885223f&scene=0&key=77421cf58af4a6533193a66d5ae245b30e56501d5daf2a234ae85448974fcf547bafb776b1386655556d82c46689228e&ascene=7&uin=MTI4NzU2NDA4Mw%3D%3D&devicetype=iPhone+OS9.3.2&version=16031610&nettype=WIFI&fontScale=100&pass_ticket=IV3CCL%2Bj%2FZa897jsPA1RrPTxxbFNpw3u0AIPPmwu5z4HnjlhAU6KghaAzvpWYK8S)
* 7/23 日举办第 17 次 NewSQL Meetup，崔秋分享[《How does TiKV auto-balance work?》](./how_does_TiKV_auto-balance_work.pdf)，张阳分享《Kubernetes in PingCAP》

# **TiDB 项目动态**

共 [Merge 22 个 PR](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-07-17..2016-07-22%20)

* 查询优化器全面重构，针对 Join、SubQuery 效率提升
* 分布式 SQL 支持聚合函数
* 提升 TiDB 服务稳定性
* 重构 Decimal 类型相关代码，提高对 MySQL 兼容性
* 针对 [Zabbix](http://www.zabbix.com/) 应用场景优化 TiDB 兼容性和性能
* 优化性能，Sysbench 结果提升 50%

**新增 Contributor：**

* [hzmangel](https://github.com/hzmangel)

# **近期事件**

* 2016/07/28 QingCloud Insight 2016，刘奇：《How we built TiDB》

# **技术新闻 & 文章**

* [PostgreSQL索引优化案例分析](http://tech.it168.com/a2016/0712/2783/000002783727.shtml)
* [Slides and Links to slides for 2016 talks](https://github.com/gophercon/2016-talks)
* [Go 1.6.3 and 1.7rc2 are released](https://groups.google.com/forum/?utm_source=golangweekly&utm_medium=email#!msg/golang-nuts/kfzBGiAcxME/3sDd4A-3CQAJ)
* [BuntDB: Embeddable, In-Memory Key/Value Database for Go](https://github.com/tidwall/buntdb)

# **加入 PingCAP**

分布式数据库是一个高难度又令人着迷的领域，前方路上还有很多未知的困难和挑战，我们深信只有找到最优秀的人同行，方能走远。盼望各路大牛加入 PingCAP，和我们一起为数据库技术、开源事业做出一些贡献，同时也能实现自身的财务自由。

具体信息参见[职位介绍](http://www.lagou.com/gongsi/j113568.html)，有意者请联系[hire@pingcap.com](mailto:hire@pingcap.com)。
