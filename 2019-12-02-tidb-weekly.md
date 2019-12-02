---
title: Weekly update (November 25 ~ December 01, 2019)
date: 2019-12-02
summary: Last week, we landed 74 PRs in the TiDB repository, 21 PRs in the TiSpark repository, and 87 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog posts

The query execution engine plays an important role in database system performance. Inspired by the paper *MonetDB/X100: Hyper-Pipelining Query Execution*, we began to employ vectorized execution in TiDB to improve query performance. Last week, we published an article that deep dives into why we need vectorized execution, how we implement it, how we managed to vectorize more than 360 functions along with community contributors, and our thoughts about the future.

The full article is here:

[10x Performance Improvement for Expression Evaluation Made Possible by Vectorized Execution and the Community](https://pingcap.com/blog/10x-performance-improvement-for-expression-evaluation-made-possible-by-vectorized-execution/)

## Community

### New contributors

tidb:

* [Rustin-Liu](https://github.com/Rustin-Liu)
* [dengsigua](https://github.com/dengsigua)

tikv:

* [ty666](https://github.com/ty666)
* [waynexia](https://github.com/waynexia)
* [tw666](https://github.com/tw666)

tispark:

* [wfnuser](https://github.com/wfnuser)

tidb-ansible:

* [n0vad3v](https://github.com/n0vad3v)

## Call for participation

* [Vectorized Expression Working Group](https://github.com/pingcap/community/blob/master/working-groups/wg-vec-expr.md)
    * [`Date` or `Time` built-in functions (35/38)](https://github.com/pingcap/tidb/issues/12101)
    * [`Decimal` built-in functions (26/31)](https://github.com/pingcap/tidb/issues/12102)
    * [`Int` built-in functions (174/187)](https://github.com/pingcap/tidb/issues/12103)
    * [`JSON` built-in functions (24/27)](https://github.com/pingcap/tidb/issues/12104)
    * [`Real` built-in functions (47/49)](https://github.com/pingcap/tidb/issues/12105)
    * [`String` built-in functions (100/108)](https://github.com/pingcap/tidb/issues/12106)
    * [`Duration` built-in functions (26/34)](https://github.com/pingcap/tidb/issues/12176)
    * Last week, [13 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+sort%3Aupdated-desc+merged%3A2019-11-25..2019-12-01+label%3Acomponent%2Fexpression+) were landed in the expression component.

* Coprocessor SIG:
    * [Improve the performance of Chunk Encoder](https://github.com/tikv/tikv/issues/5729)
    * [Implement more UDFs](https://github.com/tikv/tikv/issues/5727)
    * [Implement the new row format](https://github.com/tikv/tikv/issues/5726)
    * [Port `BinaryJSON`](https://github.com/tikv/tikv/issues/5715)
    * [Tracing](https://github.com/tikv/tikv/issues/5714)
    * [The maximum execution time of Per-request](https://github.com/tikv/tikv/issues/5712)

* Planner SIG: [Add rules for the cascades planner](https://github.com/pingcap/tidb/issues/13709)

* [More issues to solve for TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)
* [More issues to solve for TiKV](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

Last week, we landed [74 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-11-25..2019-12-01) in the TiDB repository, [21 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-11-25..2019-12-01) in the TiSpark repository, and [87 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-11-25..2019-12-01&type=Issues) in the TiKV and PD repositories.

### Critical PRs

TiDB:

* [Refactor `GetClusterServerInfo` to avoid executing the internal SQL statement to obtain the cluster topology](https://github.com/pingcap/tidb/pull/13765)
* [Get `GoVersion` from the runtime variable instead of from the shell](https://github.com/pingcap/tidb/pull/13763)
* [Raise the `No database selected` error for the `GRANT` statement](https://github.com/pingcap/tidb/pull/13745)
* [Support retrieving the CPU/memory/mutex/block/allocs profile from PD via SQL statements](https://github.com/pingcap/tidb/pull/13717)
* [Add the RPC server to get the information of other TiDB servers for diagnostics](https://github.com/pingcap/tidb/pull/13693)
* [Show `max-proc-keys` and `p95-proc-keys` in the results of `explain analyze`](https://github.com/pingcap/tidb/pull/13692)
* [Implement the non-block reading for `Get` and `BatchGet` under the large transaction protocol](https://github.com/pingcap/tidb/pull/13599)
* [Unify the endian for the `Chunk` encode format](https://github.com/pingcap/tidb/pull/13349)
* [Support a hint to force using an `IndexMerge` path](https://github.com/pingcap/tidb/pull/12843)

TiSpark:

* [Support the data format and the columnar execution of the TiDB `Chunk` in Spark](https://github.com/pingcap/tispark/pull/1220)
* [Register `UDF` for every `sparkSession`](https://github.com/pingcap/tispark/pull/1258)
* [Fix a bug of `encodeKey` for the decimal type](https://github.com/pingcap/tispark/pull/1254)
* [Disable pushing down the set, enum, and bit types](https://github.com/pingcap/tispark/pull/1242)

TiKV and PD:

* Improve TiKV performance: [#5756](https://github.com/tikv/tikv/pull/5756) [#5846](https://github.com/tikv/tikv/pull/5846) [#6010](https://github.com/tikv/tikv/pull/6010) [#6000](https://github.com/tikv/tikv/pull/6000) [#6047](https://github.com/tikv/tikv/pull/6047)
* [Fix a Region merge bug](https://github.com/tikv/tikv/pull/5871)
* [Provide the diagnostics gRPC interface](https://github.com/tikv/tikv/pull/5980)
* [Support the Coprocessor cache protocol](https://github.com/tikv/tikv/pull/6076)
* [Support printing the SST files in Region properties for tikv-ctl](https://github.com/tikv/tikv/pull/5987)
* [Fix an unexpected error in PD when setting the configuration item to the same value](https://github.com/pingcap/pd/pull/1960)
* [Add the profiling API to PD](https://github.com/pingcap/pd/pull/1965)

## Upcoming TiDB event

[Infra Meetup No.120 (in Chinese)](https://pingcap.com/meetup/)

Date: December 7th, 2019

Location: Beike Building, Nanshan District, Guangdong Province
