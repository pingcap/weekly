---
title: Weekly update (November 04 ~ November 10, 2019)
date: 2019-11-11
summary: Last week, we landed 151 PRs in the TiDB repository, 13 PRs in the TiSpark repository, 58 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog posts

TiDB is an HTAP database that targets both OLTP and OLAP scenarios. TiFlash is its extended analytical engine. Last week, we published a post that introduces how TiFlash fuels TiDB to become a true HTAP database that lets users perform real-time analytics.

The full article is here:

[Delivering Real-time Analytics and True HTAP by Combining Columnstore and Rowstore](https://pingcap.com/blog/delivering-real-time-analytics-and-true-htap-by-combining-columnstore-and-rowstore/)

Is there an easier way to write TiDB SQL statements, to test the compatibility, and to easily understand the difference between TiDB and MySQL? Yes. Now, you can run TiDB directly in a web browser.

Last week, we published another posts that introduces how you can run TiDB directly in a web browser, how it is possible, and what the limitations are.

The full article is here:

[TiDB in the Browser: Running a Golang Database on WebAssembly](https://pingcap.com/blog/tidb-in-the-browser-running-a-golang-database-on-webassembly/)

## Community

### New contributors

tidb:

* [chenlx0](https://github.com/chenlx0)
* [CSFresh](https://github.com/CSFresh)
* [KuangBo](https://github.com/KuangBo)
* [zhongshanhao](https://github.com/zhongshanhao)
* [soobun](https://github.com/soobun)

tikv:

* [iswade](https://github.com/iswade)

tidb-operator:

* [silentred](https://github.com/silentred)

## Call for participation

* [Vectorized Expression Working Group](https://github.com/pingcap/community/blob/master/working-groups/wg-vec-expr.md)
    * [`Date` or `Time` built-in functions (25/65)](https://github.com/pingcap/tidb/issues/12101)
    * [`Decimal` built-in functions (19/31)](https://github.com/pingcap/tidb/issues/12102)
    * [`Int` built-in functions (150/187)](https://github.com/pingcap/tidb/issues/12103)
    * [`JSON` built-in functions (19/27)](https://github.com/pingcap/tidb/issues/12104)
    * [`Real` built-in functions (46/49)](https://github.com/pingcap/tidb/issues/12105)
    * [`String` built-in functions (80/133)](https://github.com/pingcap/tidb/issues/12106)
    * [`Duration` built-in functions (17/45)](https://github.com/pingcap/tidb/issues/12176)
    * Last week, [54 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+sort%3Aupdated-desc+merged%3A2019-11-04..2019-11-10+label%3Acomponent%2Fexpression+) were landed in the expression component.

* Coprocessor SIG:
    * [Improve the performance of Chunk Encoder](https://github.com/tikv/tikv/issues/5729)
    * [Implement more UDFs](https://github.com/tikv/tikv/issues/5727)
    * [Implement the new row format](https://github.com/tikv/tikv/issues/5726)
    * [Port `BinaryJSON`](https://github.com/tikv/tikv/issues/5715)
    * [Tracing](https://github.com/tikv/tikv/issues/5714)
    * [The maximum execution time of Per-request](https://github.com/tikv/tikv/issues/5712)

* [More issues to solve for TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)
* [More issues to solve for TiKV](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

Last week, we landed [151 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-11-04..2019-11-10) in the TiDB repository, [13 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-11-04..2019-11-10+) in the TiSpark repository, and [58 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-11-04..2019-11-10&type=Issues) in the TiKV and PD repositories.

### Critical PRs

TiDB:

* [Add the `table_tiflash_replica` table to check the status of `tableTiFlashReplica`](https://github.com/pingcap/tidb/pull/13205)
* [Handle the deprecated configuration items in `config-check`](https://github.com/pingcap/tidb/pull/13142)
* [Support using multiple bindings in the planner](https://github.com/pingcap/tidb/pull/13047)
* [Add the `PushSelDownAggregation` transformation rule in the cascades planner](https://github.com/pingcap/tidb/pull/13106)
* [Support `innodb_lock_wait_timeout` for the pessimistic transaction](https://github.com/pingcap/tidb/pull/13103)
* [Push `json_length` to TiKV](https://github.com/pingcap/tidb/pull/13078)
* [Add the `tidb_cluster_config` virtual table to retrieve all instance configurations](https://github.com/pingcap/tidb/pull/13063)
* [Add `binlog_status` for the HTTP API and the `TIDB_SERVERS_INFO` table](https://github.com/pingcap/tidb/pull/13025)
* [Limit the length of the index name when executing the `CREATE TABLE` statement](https://github.com/pingcap/tidb/pull/13016)
* [Vectorize the hash calculation during probing](https://github.com/pingcap/tidb/pull/12669)
* [Support the required rows for the arrow decode format](https://github.com/pingcap/tidb/pull/12613)

TiSpark:

* [Fix the Stack Overflow error when reading from the partition table](https://github.com/pingcap/tispark/pull/1179)
* [Fix `OrderProjectLimitPushdown`](https://github.com/pingcap/tispark/pull/1185)

TiKV and PD:

* [Support the lock wait timeout](https://github.com/tikv/tikv/pull/5680)
* [Refactor `DateTime`](https://github.com/tikv/tikv/pull/5473)
* [Fix the issue that the value type is incorrect when parsing a number to JSON](https://github.com/tikv/tikv/pull/5842)
* [Refactor the storage module](https://github.com/tikv/tikv/pull/5822)
* [Fix the wrong Region size](https://github.com/pingcap/pd/pull/1886)
* [Use the store flow byte rate to make schedule decisions](https://github.com/pingcap/pd/pull/1870)
* [Fix the stale operator when scattering Regions](https://github.com/pingcap/pd/pull/1891)
* [Support the key range for schedulers](https://github.com/pingcap/pd/pull/1791)
