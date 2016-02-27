**TiDB Weekly**

   2016/2/26

欢迎浏览本期 TiDB Weekly。[TiDB](https://github.com/pingcap/tidb) 是一个分布式 SQL 数据库。灵感来自于 Google 的 [F1](http://research.google.com/pubs/pub41344.html) 和 [Spanner](http://research.google.com/archive/spanner.html)，TiDB 支持包括传统 RDBMS 和 NoSQL 的特性。这里是对 TiDB 项目及社区的每周消息汇总。如果要投稿，请关注 Twitter [@](https://twitter.com/ThisWeekInRust)[PingCAP](https://twitter.com/PingCAP) 或者发送邮件到 [weekly@pingcap.com](mailto:weekly@pingcap.com)。[欢迎参与 TiDB 项目](https://github.com/pingcap/tidb/blob/master/CONTRIBUTING.md)以及[《从零开始写分布式数据库》](https://github.com/ngaut/builddatabase)。

# **TiDB 社区动态**

## **新闻 & 文章**

* 完成查询计划相关代码重构，SQL Optimizer 全面升级，更强大、灵活
* 开始并行查询设计

# **TiDB 项目动态**

共 [Merge 9 个 PR](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2016-02-20..2016-02-26+) ：

<table>
  <tr>
    <td>Contributor</td>
    <td>公司</td>
    <td>数量</td>
  </tr>
  <tr>
    <td>聂愿愿</td>
    <td>华为</td>
    <td>1</td>
  </tr>
  <tr>
    <td>coocood</td>
    <td>PingCAP</td>
    <td>4</td>
  </tr>
  <tr>
    <td>zimulala</td>
    <td>PingCAP</td>
    <td>2</td>
  </tr>
  <tr>
    <td>shenli</td>
    <td>PingCAP</td>
    <td>1</td>
  </tr>
  <tr>
    <td>ngaut</td>
    <td>PingCAP</td>
    <td>1</td>
  </tr>
</table>


## **重要的特性**

* 增加内存引擎，用于存储 InformationSchema 和 PerformanceSchema
* PerformanceSchema 接入 SQL 查询流程中，用于记录语句执行性能
* 支持 Explain 语句

## **（感谢）新增 Contributor**

* 实习生[赵星宇](https://github.com/zxylvlp)入职 PingCAP

# **近期事件**

* 2016/04/16  Gopher China，[刘奇](http://weibo.com/chuangyiyongpin)：《 Go 在分布式数据库中的应用》
* 2016/02/24 联想云计算交流
* DTCC 2016 中国数据库大会《使用 Raft 构建分布式 OLTP 之路》议题入选
* 100offer 线下大数据交流《分布式关系型数据库架构设计》
