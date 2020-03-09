---
title: Weekly update (March 02 ~ March 08, 2020)
date: 2020-03-09
summary: Last week, we landed 90 PRs in the TiDB repository and 46 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog posts

Not long after we celebrated our 300th contributor milestone in September 2019, a new record, [400th contributor](https://github.com/pingcap/tidb/graphs/contributors), is just created in our TiDB repository! Last week, we published a post written by our CTO Edward Huang to celebrate 400 contributors in our TiDB repository.

The full post is here:

[TiDB Celebrates 400 Contributors](https://pingcap.com/blog/tidb-celebrates-400-contributors/)

As the TiDB community expands and the TiDB project evolves, we're inspired to see contributors joining us and demonstrating their passion and pursuit of the open-source spirit. To get more people involved and included, we launched the TiDB Challenge Program, a series community program to bring TiDB to a new level in terms of stability, performance, and usability. With some amazing improvements in performance in season 1 last year, we published a post last week to announce that season 2 is ready for you.

The full post is here:

[TiDB Usability Challenge - Dare to Dream Bigger](https://pingcap.com/blog/tidb-usability-challenge-dare-to-dream-bigger/)

## Community

### New contributors

tidb:

* [dasinlsb](https://github.com/dasinlsb)
* [psinghal20](https://github.com/psinghal20)
* [peterepsteen](https://github.com/peterepsteen)

pd:

* [loxp](https://github.com/loxp)
* [Poytr1](https://github.com/Poytr1)

docs-cn:

* [hjk0205](https://github.com/hjk0205)

tidb-operator:

* [tirsen](https://github.com/tirsen)

parser:

* [gauss1314](https://github.com/gauss1314)

chaos-mesh:

* [tfulcrand](https://github.com/tfulcrand)

## Call for participation

* [Issues to solve for TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)
* [Issues to solve for TiKV](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

Last week, we landed [90 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2020-03-02..2020-03-08+) in the TiDB repository and [46 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2020-03-02..2020-03-08) in the TiKV and PD repositories.

### Critical PRs

TiDB:

* [Enable the dynamic configuration by default](https://github.com/pingcap/tidb/pull/15172)
* [Support `SELECT FOR UPDATE` for `BatchPointGet`](https://github.com/pingcap/tidb/pull/15129)
* [Push the collation information down to TiKV and MockTiKV](https://github.com/pingcap/tidb/pull/15125)
* [Do not generate the partial aggregation when the cop-task has root conditions](https://github.com/pingcap/tidb/pull/15112)
* [Add the DDL and DML privilege check for system tables](https://github.com/pingcap/tidb/pull/15095)
* [Support `BatchCommands` for the RPC server to fix the panic in the batch connection heartbeat](https://github.com/pingcap/tidb/pull/15055)
* [Refactor the TSO future in the RC isolation](https://github.com/pingcap/tidb/pull/14966)
* [Add the implementation for `SetCollationExpr` in the planner](https://github.com/pingcap/tidb/pull/14959)
* [Fix the issue that the `CREATE TABLE LIKE` statement does not split Regions on TiKV](https://github.com/pingcap/tidb/pull/14904)
* [Support caching the prepare plan for the query on hash partitioned tables](https://github.com/pingcap/tidb/pull/14473)
* [Add a channel to limit multiple DDL jobs being written at the same time](https://github.com/pingcap/tidb/pull/14342)

TiKV and PD:

* [Enable the dynamic configuration by default](https://github.com/tikv/tikv/pull/7015)
* [Make sure that check keys do not exist](https://github.com/tikv/tikv/pull/6715)
* [Support `CollationAware` in `compare_in`](https://github.com/tikv/tikv/pull/6713)
* [Move `WriteBatch` from `engine` to `engine_traits` and `rocks`](https://github.com/tikv/tikv/pull/6697)
* [Add a Raftstore option to keep the data integration when half of peers fail](https://github.com/tikv/tikv/pull/6578)

## On-going TiDB event

[TiDB Usability Challenge Program](https://pingcap.com/community/tidb-usability-challenge/)
