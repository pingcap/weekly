---
title: Weekly update (November 11 ~ November 17, 2019)
date: 2019-11-18
summary: Last week, we landed 122 PRs in the TiDB repository, 12 PRs in the TiSpark repository, 53 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog post

As TiDB-Wasm allows you to easily write TiDB SQL statements, to test the compatibility, and to understand the difference between TiDB and MySQL right in your browser, this Golang database also opens a door to an entirely new world for both Golang and Wasm.

Last week, we published a post that dives deep into how and why we built an in-browser database. By the end of the article, you’ll know how to reproduce it yourself, create your own projects, and get inspired.

The full article is here:

[How We Compiled a Golang Database in the Browser Using WebAssembly](https://pingcap.com/blog/how-we-compiled-a-golang-database-in-the-browser-using-webassembly/)

## Community

### New contributors

tidb:

* [silver--bullet](https://github.com/silver--bullet)
* [CCChieh](https://github.com/CCChieh)
* [Zhuchengyu04](https://github.com/Zhuchengyu04)
* [lwxwx](https://github.com/lwxwx)
* [hejiayua](https://github.com/hejiayua)
* [LynneLiu-LYJ](https://github.com/LynneLiu-LYJ)

tikv:

* [cireu](https://github.com/cireu)
* [gauss1314](https://github.com/gauss1314)

tidb-operator:

* [mantuliu](https://github.com/mantuliu)

tidb-binlog:

* [wty4427300](https://github.com/wty4427300)

## Call for participation

* [Vectorized Expression Working Group](https://github.com/pingcap/community/blob/master/working-groups/wg-vec-expr.md)
    * [`Date` or `Time` built-in functions (30/65)](https://github.com/pingcap/tidb/issues/12101)
    * [`Decimal` built-in functions (20/31)](https://github.com/pingcap/tidb/issues/12102)
    * [`Int` built-in functions (155/187)](https://github.com/pingcap/tidb/issues/12103)
    * [`JSON` built-in functions (22/27)](https://github.com/pingcap/tidb/issues/12104)
    * [`Real` built-in functions (46/49)](https://github.com/pingcap/tidb/issues/12105)
    * [`String` built-in functions (89/133)](https://github.com/pingcap/tidb/issues/12106)
    * [`Duration` built-in functions (17/45)](https://github.com/pingcap/tidb/issues/12176)
    * Last week, 50 PRs were landed in the expression component.

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

Last week, we landed [122 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-11-11..2019-11-17) in the TiDB repository, [12 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-11-11..2019-11-17) in the TiSpark repository, and [53 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-11-11..2019-11-17&type=Issues) in the TiKV and PD repositories.

### Critical PRs

TiDB:

* [Fix a `BatchGetExec` bug inside a transaction](https://github.com/pingcap/tidb/pull/13473)
* [Fix the data race for the partition table's hash code](https://github.com/pingcap/tidb/pull/13421)
* [Support `PointGet` by `_tidb_rowid`](https://github.com/pingcap/tidb/pull/13360)
* [Handle the unique key when estimating equal conditions for indices and the primary key](https://github.com/pingcap/tidb/pull/13354)
* [Check the length of the table name when renaming a table](https://github.com/pingcap/tidb/pull/13339)
* [Add the implementation rule for `TopN` in the cascades planner](https://github.com/pingcap/tidb/pull/13323)
* [Support `Hint` for `IndexHashJoin` and `IndexMergeJoin`](https://github.com/pingcap/tidb/pull/13238)
* [Support adding or dropping the primary key by configuring `enable-pk-is-handle`](https://github.com/pingcap/tidb/pull/13229)
* [Add the store limit to restrain the bad stores which occupy too much token limit](https://github.com/pingcap/tidb/pull/12779)
* [Implement the execution part of the outer hash join](https://github.com/pingcap/tidb/pull/12882)
* [Perform the vectorized calculation of the key for the `GROUP BY` items in the hash aggregation](https://github.com/pingcap/tidb/pull/12729)

TiSpark:

* [Fix the task retry when TiKV is down](https://github.com/pingcap/tispark/pull/1207)

TiKV and PD:

* [Generate the flame graph at runtime](https://github.com/tikv/tikv/pull/5697)
* [Fix a replica read bug which causes the panic](https://github.com/tikv/tikv/pull/5887)
* [Fix a Region merge bug which causes the panic](https://github.com/tikv/tikv/pull/5868)
* [Fix the panic that occurs when getting TS from followers](https://github.com/pingcap/pd/pull/1930)
* [Check the timestamp decrease and return an error when the decrease occurs](https://github.com/pingcap/pd/pull/1921)
* [Add the collection of thread information and the calculation of store scores](https://github.com/pingcap/pd/pull/1903)
