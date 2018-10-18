---
title: Weekly update (January 08 ~ January 14, 2018)
date: 2018-01-15
summary: Last week, we landed 43 PRs in the TiDB repositories and 25 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [43 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is:pr+is:merged+merged:2018-01-08..2018-01-14) in the TiDB repositories.

## Added

* [Support the ODBC syntax of `time/date/timestamp` literal](https://github.com/pingcap/tidb/pull/5634)
* [Add `MaxProcs` and make the `runtime.GOMAXPROCS` parameter configurable](https://github.com/pingcap/tidb/pull/5612)

## Fixed

* [Fix a bug about index join](https://github.com/pingcap/tidb/pull/5623)
* [Close `HashJoin` goroutines as soon as possible to avoid unexpected errors](https://github.com/pingcap/tidb/pull/5620)
* [`fetchShowTableStatus` should append an integer to the third column instead of a string](https://github.com/pingcap/tidb/pull/5608)
* [Correct the behavior when `RunWorker` is false](https://github.com/pingcap/tidb/pull/5598)
* [Refine the `typeInfer` of `group_concat`](https://github.com/pingcap/tidb/pull/5573)

## Improved

* [Avoid the Children type assertion](https://github.com/pingcap/tidb/pull/5616)
* [Merge `IntColumnRange` with `NewRange`](https://github.com/pingcap/tidb/pull/5591)
* [Upgrade the username length limit to 32 to be compatible with MySQL 5.7](https://github.com/pingcap/tidb/pull/5588)
* [Garbage collects useless stats info](https://github.com/pingcap/tidb/pull/558)
* [`InsertExec` eliminates unnecessary `CastValue` operations](https://github.com/pingcap/tidb/pull/5581)
* [Speed up row count estimation](https://github.com/pingcap/tidb/pull/5579)
* [Support encoding a `Chunk` row](https://github.com/pingcap/tidb/pull/5578)
* [Use `dep` instead of `glide`](https://github.com/pingcap/tidb/pull/5558)
* [Optimize the `insert ignore` statement](https://github.com/pingcap/tidb/pull/5508)
* Support `Chunk` in:
    - [`HashJoinExec`](https://github.com/pingcap/tidb/pull/5439)
    - [`ExecuteExec`](https://github.com/pingcap/tidb/pull/5410)

# Weekly update in TiKV and PD

Last week, we landed [25 PRs](https://github.com/search?q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-01-08..2018-01-14) in the TiKV and PD repositories.

## Added

* [Add the node case](https://github.com/pingcap/pd/pull/901)
* [Support Region split](https://github.com/pingcap/pd/pull/905)
* [Support query regions by read/write flow](https://github.com/pingcap/pd/pull/897)

## Fixed

* [Change the version](https://github.com/pingcap/tikv/pull/2658)
* [Fix a RocksDB task name error](https://github.com/pingcap/tikv/pull/2663)
* [Cancel `call` when refreshing client](https://github.com/pingcap/tikv/pull/2669)

## Improved

* [Use `dep` instead of `glide`](https://github.com/pingcap/pd/pull/904)
* [Optimize write type parsing for MVCC properties collector](https://github.com/pingcap/tikv/pull/2654)
* [Update README and upgrade Dockerfile golang:1.9.2](https://github.com/pingcap/pd/pull/908)
* [Specify gRPC event engine](https://github.com/pingcap/tikv/pull/2656)
* [Add the debug log](https://github.com/pingcap/pd/pull/907)
* [Fix some `ineffassign` to improve the GoReport Result](https://github.com/pingcap/pd/pull/911)
* [Rename `AggregationExecutor` to `HashAggExecutor`](https://github.com/pingcap/tikv/pull/2673)
* [Improve the GoReport Result](https://github.com/pingcap/pd/pull/912)
* [Dump the `ConfChange` type Raft log entry](https://github.com/pingcap/tikv/pull/2661)
* [Make meta key return array](https://github.com/pingcap/tikv/pull/2677)

# New contributor (Thanks!)

* PD: [maiyang](https://github.com/yangwenmai)