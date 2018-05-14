---
title: Weekly update (May 07 ~ May 13, 2018)
date: 2018-05-14
summary: Last week, we landed 55 PRs in the TiDB repositories and 24 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [55 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-05-07..2018-05-13+) in the TiDB repositories.

## Added

- [Support renaming a table as its original name](https://github.com/pingcap/tidb/pull/6391)
- [Allow correlated columns to be pushed down to TiKV](https://github.com/pingcap/tidb/pull/6403)
- [Support local latches for the transactions in TiDB](https://github.com/pingcap/tidb/pull/6418)
- [Add an option to stop writing Binlog when TiDB meets some Binlog errors](https://github.com/pingcap/tidb/pull/6503)
- [Add an HTTP API to enable or disable the general log of TiDB](https://github.com/pingcap/tidb/pull/6513)
- [Update the `logrus` package to a new version](https://github.com/pingcap/tidb/pull/6536)

## Fixed

- [Set `lastInsertID` in the duplicated update statement](https://github.com/pingcap/tidb/pull/6345)
- [Fix several bugs of statistics feedback](https://github.com/pingcap/tidb/pull/6444)
- [Fix a bug occurred when values are inserted into a time column](https://github.com/pingcap/tidb/pull/6451)
- [Fix a bug when creating a table and renaming a table run concurrently](https://github.com/pingcap/tidb/pull/6462)
- [Rollback all keys when `Prewrite` fails](https://github.com/pingcap/tidb/pull/6472)
- [Fix a bug when adding index meets `handle = MaxInt64`](https://github.com/pingcap/tidb/pull/6481)
- [Fix a bug when the `limit` offset is a multiple of `MaxChunkSize`](https://github.com/pingcap/tidb/pull/6498)
- [Fix a bug when a complex subquery exists in the `Update` statement](https://github.com/pingcap/tidb/pull/6540)

## Improved

- [Refine the error message about `Out of range value for column`](https://github.com/pingcap/tidb/pull/6334)
- [Set `gc_worker` and `loadDeleteRangeSQL` to a much higher priority](https://github.com/pingcap/tidb/pull/6450)
- [Make `tidb_opt_insubquery_unfold` a global variable](https://github.com/pingcap/tidb/pull/6482)
- [Uniform the calculation method of pseudo statistics](https://github.com/pingcap/tidb/pull/6483)
- [Improve the CPU usage when `opentracing` is not enabled](https://github.com/pingcap/tidb/pull/6494)

# Weekly update in TiKV and PD

Last week, we landed [24 PRs](https://github.com/search?p=1&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-05-07..2018-05-13&type=Issues&utf8=%E2%9C%93) in the TiKV and PD repositories.

## Added

- [Support `reverse_scan`](https://github.com/pingcap/tikv/pull/3033)

## Fixed

- [Check learner regardless of whether learner is enabled or not](https://github.com/pingcap/pd/pull/1053)
- [Use `AtomicU64` instead of `RwLock` to track the snapshot size](https://github.com/pingcap/tikv/pull/3020)

## Improved

- [Migrate CircleCI 1.0 to 2.0](https://github.com/pingcap/tikv/pull/2993)
- [Ignore `Lock` when lock's type is `Lock`](https://github.com/pingcap/tikv/pull/3011)
- [Decode the number by accessing `slice` directly](https://github.com/pingcap/tikv/pull/3028)