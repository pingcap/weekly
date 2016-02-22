**TiDB Weekly**

   2016/2/19

欢迎浏览本期 TiDB Weekly。[TiDB](https://github.com/pingcap/tidb) 是一个分布式 SQL 数据库。灵感来自于 Google 的 [F1](http://research.google.com/pubs/pub41344.html) 和 [Spanner](http://research.google.com/archive/spanner.html)，TiDB 支持包括传统 RDBMS 和 NoSQL 的特性。这里是对 TiDB 项目及社区的每周消息汇总。如果要投稿，请关注 Twitter [@](https://twitter.com/ThisWeekInRust)[PingCAP](https://twitter.com/PingCAP) 或者发送邮件到 [weekly@pingcap.com](mailto:weekly@pingcap.com)。[欢迎参与 TiDB 项目](https://github.com/pingcap/tidb/blob/master/CONTRIBUTING.md)以及[《从零开始写分布式数据库》](https://github.com/ngaut/builddatabase)。

# **TiDB 社区动态**

## 新闻 & 文章

* PingCAP CEO 宣布将于 2016/04/01 开源完全自主研发的大型分布式 Key-Value 系统 TiKV。TiKV 使用 Rust 语言编写，可以作为 TiDB 的存储引擎来替换 HBase 引擎。目前正在做开源前的各项准备工作，该系统的特性包括：
    * 强一致性：使用 Raft 协议来复制数据
    * 分布式事务
    * 强大的动态 Scale 能力
    * 支持 Coprocessor 机制
* [《源码角度看 TiDB 的异步 schema 变更实现》](https://github.com/ngaut/builddatabase/blob/master/f1/schema-change-implement.md)

# TiDB 项目动态

共 [Merge 27个 PR](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2016-01-30..2016-02-19) ：

<table>
  <tr>
    <td>Contributor</td>
    <td>公司</td>
    <td>数量</td>
  </tr>
  <tr>
    <td>Steffen Butzer</td>
    <td></td>
    <td>2</td>
  </tr>
  <tr>
    <td>聂愿愿</td>
    <td>华为</td>
    <td>3</td>
  </tr>
  <tr>
    <td>coocood</td>
    <td>PingCAP</td>
    <td>12</td>
  </tr>
  <tr>
    <td>zimulala</td>
    <td>PingCAP</td>
    <td>2</td>
  </tr>
  <tr>
    <td>shenli</td>
    <td>PingCAP</td>
    <td>8</td>
  </tr>
</table>


## 重要的特性

* Performance Schema： 实现建表与查询
* 优化 Truncate 语句执行计划，使用后台任务删除数据
* 优化 Update/Delete 语句执行计划
* [SMP 架构设计](https://github.com/tidb-cn/docs/pull/3/files) (来自华为 [roger-lijian](https://github.com/roger-lijian))

## **（感谢）新增 Contributor**

* [Steffen Butzer](https://github.com/steffengy)（德国）

# **近期事件**

* 2016/04/16  第二届 Gopher China (Beijing) 演讲（[刘奇](http://weibo.com/chuangyiyongpin)）
* 2016/02/18 联通云计算交流
* 2016/02/18 万达技术交流
