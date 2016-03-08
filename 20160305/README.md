**TiDB Weekly**

   2016/3/5

欢迎浏览本期 TiDB Weekly。[TiDB](https://github.com/pingcap/tidb) 是一个分布式 SQL 数据库。灵感来自于 Google 的 [F1](http://research.google.com/pubs/pub41344.html) 和 [Spanner](http://research.google.com/archive/spanner.html)，TiDB 支持包括传统 RDBMS 和 NoSQL 的特性。这里是对 TiDB 项目及社区的每周消息汇总。如果要投稿，请关注 Twitter [@](https://twitter.com/ThisWeekInRust)[PingCAP](https://twitter.com/PingCAP) 或者发送邮件到 [weekly@pingcap.com](mailto:weekly@pingcap.com)。[欢迎参与 TiDB 项目](https://github.com/pingcap/tidb/blob/master/CONTRIBUTING.md)以及[《从零开始写分布式数据库》](https://github.com/ngaut/builddatabase)。

# **TiDB 社区动态**

## **新闻 & 文章**

* 完成 SQL Layer 并行查询优化以及 SMP 优化设计草稿
* 3月5日 举办第一次 PingCAP 线下 Meetup，与华为、百度、美团、京东等公司技术人员交流 TiDB 的最新进展

# **TiDB 项目动态**

共 [Merge 23 个 PR](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2016-02-27..2016-03-05+) ：

<table>
  <tr>
    <td>Contributor</td>
    <td>公司</td>
    <td>数量</td>
  </tr>
  <tr>
    <td>赵星宇</td>
    <td>PingCAP</td>
    <td>2</td>
  </tr>
  <tr>
    <td>coocood</td>
    <td>PingCAP</td>
    <td>12</td>
  </tr>
  <tr>
    <td>zimulala</td>
    <td>PingCAP</td>
    <td>3</td>
  </tr>
  <tr>
    <td>shenli</td>
    <td>PingCAP</td>
    <td>5</td>
  </tr>
  <tr>
    <td>c-wind</td>
    <td>京东</td>
    <td>1</td>
  </tr>
</table>


## **重要的特性**

* 引入携带类型信息的 Datum 类，替换类型推导，大幅提高性能。其中类型比较操作提速30倍
* 完成[并行查询优化设计草稿](https://github.com/tidb-cn/docs/pull/5)
* 完成 [SMP 设计草稿](https://github.com/tidb-cn/docs/pull/4)

## **（感谢）新增 Contributor**

* [田光宇](https://github.com/c-wind)

# **近期事件**

* 2016/03/06 100offer 线下大数据交流，[黄东旭](http://weibo.com/c4pt0r?is_all=1)：《分布式关系型数据库架构设计》
* 2016/04/16  Gopher China，[刘奇](http://weibo.com/chuangyiyongpin)：《 Go 在分布式数据库中的应用》
* DTCC 2016 中国数据库大会《使用 Raft 构建分布式 OLTP 之路》议题入选
