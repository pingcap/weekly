---
title: Weekly update (December 02 ~ December 08, 2019)
date: 2019-12-09
summary: Last week, we landed 100 PRs in the TiDB repository, 19 PRs in the TiSpark repository, and 49 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog posts

The TiDB user community has played an important role in product polishing and upgrading. However, it was obscured in the old community structure. In addition, the responsibilities for the roles in the developer community and the relationship between roles are relatively simple. Therefore, we decided to include the TiDB user community in the new community structure while providing the TiDB developer community with clearly defined roles, rights, and responsibilities. At the same time, some new roles and new organizations have been introduced.

Let's take a closer look:

[New Structure, New Roles - TiDB Community Upgrade!](https://pingcap.com/blog/tidb-community-upgrade/)

NetEase Games, affiliated with NetEase, Inc., is a leading provider of self‐developed PC‐client and mobile games to worldwide users. As their business boomed, the soaring data size became a nightmare. Last week, we published a post written by Wenjie Li, the senior database administrator at NetEase Games Billing Team and the TiDB User Group Ambassador, that dives deep into why NetEase Games chose TiDB, an open-source MySQL-compatible distributed Hybrid Transactional/Analytical Processing (HTAP) database, over some other MySQL-based and NewSQL storage solutions. Li describes how they tested TiDB against its competitors, why TiDB won, and how they are using it now.

The full article is here:

[NetEase Games: Why We Chose a Distributed SQL Database Alongside MySQL to Break down Data Silos](https://pingcap.com/success-stories/why-we-chose-a-distributed-sql-database-alongside-mysql-to-break-down-data-silos/)

## Community

### New contributors

tidb:

* [ylht](https://github.com/ylht)
* [eggeek](https://github.com/eggeek)
* [t0350](https://github.com/t0350)
* [tongxing2019](https://github.com/tongxing2019)

pd:

* [ekalinin](https://github.com/ekalinin)

dm:

* [SE-Bin](https://github.com/SE-Bin)

## Call for participation

* [Vectorized Expression Working Group](https://github.com/pingcap/community/blob/master/working-groups/wg-vec-expr.md)
    * [`Date` or `Time` built-in functions (35/38)](https://github.com/pingcap/tidb/issues/12101)
    * [`Decimal` built-in functions (26/31)](https://github.com/pingcap/tidb/issues/12102)
    * [`Int` built-in functions (174/187)](https://github.com/pingcap/tidb/issues/12103)
    * [`JSON` built-in functions (24/27)](https://github.com/pingcap/tidb/issues/12104)
    * [`Real` built-in functions (47/49)](https://github.com/pingcap/tidb/issues/12105)
    * [`String` built-in functions (100/108)](https://github.com/pingcap/tidb/issues/12106)
    * [`Duration` built-in functions (26/34)](https://github.com/pingcap/tidb/issues/12176)
    * Last week, [19 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+sort%3Aupdated-desc+merged%3A2019-12-02..2019-12-08+label%3Acomponent%2Fexpression+) were landed in the expression component.

* Coprocessor SIG:
    * [Improve the performance of Chunk Encoder](https://github.com/tikv/tikv/issues/5729)
    * [Implement more UDFs](https://github.com/tikv/tikv/issues/5727)
    * [Implement the new row format](https://github.com/tikv/tikv/issues/5726)
    * [Port `BinaryJSON`](https://github.com/tikv/tikv/issues/5715)
    * [Tracing](https://github.com/tikv/tikv/issues/5714)
    * [The maximum execution time of Per-request](https://github.com/tikv/tikv/issues/5712)

* Planner SIG:
    * [Add rules for the cascades planner](https://github.com/pingcap/tidb/issues/13709)

* [More issues to solve for TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)
* [More issues to solve for TiKV](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

Last week, we landed [100 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-12-02..2019-12-08+) in the TiDB repository, [19 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-12-02..2019-12-08+) in the TiSpark repository, and [49 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-12-02..2019-12-08&type=Issues) in the TiKV and PD repositories.

### Critical PRs

TiDB:

* [Change `waitStart` of the pessimistic lock for one statement](https://github.com/pingcap/tidb/pull/13922)
* [Add the `tidb_enable_parallel_commit` global variable](https://github.com/pingcap/tidb/pull/13920)
* [Add the `ProjectionElimination` transformation rule for the cascades planner](https://github.com/pingcap/tidb/pull/13895)
* [Fix the SQL `bind` when SQL has a symbol list](https://github.com/pingcap/tidb/pull/13889)
* [Apply `vecGroupChecker` in the `window` executor](https://github.com/pingcap/tidb/pull/13852)
* [Show operators' disk consumption in the results of `EXPLAIN ANALYZE`](https://github.com/pingcap/tidb/pull/13764)
* [Support the framework of the reverse evaluation for the expression](https://github.com/pingcap/tidb/pull/13738)
* [Support reading the memory table of the TiDB cluster](https://github.com/pingcap/tidb/pull/13065)

TiSpark:

* [Support getting JSON when using the `TypeChunk coedc` format](https://github.com/pingcap/tispark/pull/1283)
* [Fix the issue that TiSpark distributes TiFlash tasks in the way of TiKV](https://github.com/pingcap/tispark/pull/1289)
* [Add the timezone check](https://github.com/pingcap/tispark/pull/1275)

TiKV and PD:

* [Update gRPC to fix a potential memory leak issue](https://github.com/tikv/tikv/pull/6128)
* [Fix a bug that causes the deadlock detector leader to step down](https://github.com/tikv/tikv/pull/6125)
* [Optimize the scheduler latches to avoid `latch-wait`](https://github.com/tikv/tikv/pull/6094)
* [Fix the non-pessimistic lock conflict](https://github.com/tikv/tikv/pull/6066)
* [Add the pending influence to the scheduler](https://github.com/pingcap/pd/pull/1982)
* [Improve the performance of the HTTP API for getting all Regions](https://github.com/pingcap/pd/pull/1970)
* [Introduce the operator builder](https://github.com/pingcap/pd/pull/1958)

## Upcoming TiDB event

[Paper reading (in Chinese) on Dec 9](https://github.com/pingcap/presentations/blob/master/paper-reading.md)
