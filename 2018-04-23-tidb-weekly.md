---
title: Weekly update (April 16 ~ April 22, 2018)
date: 2018-04-23
summary: Last week, we landed 36 PRs in the TiDB repositories, 8 PRs in the TiSpark repositories, and 29 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [36 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-04-16..2018-04-22) in the TiDB repositories.

## Added

- [Add TiDB HTTP API to query the DDL history information](https://github.com/pingcap/tidb/pull/6245/files)
- [Add the session variable `tidb_optimizer_selectivity_level` to control the selectivity estimation level](https://github.com/pingcap/tidb/pull/6289)
- [Add table partition information in `SHOW CREATE TABLE`](https://github.com/pingcap/tidb/pull/6292)
- [Analyze the table automatically when the modified row count of a table is too large](https://github.com/pingcap/tidb/pull/6294)

## Fixed

- [Check if the column name already exists before renaming a column](https://github.com/pingcap/tidb/pull/6284)
- [Fix a problem when parallel executing `CREATE TABLE IF NOT EXISTS`](https://github.com/pingcap/tidb/pull/6286)
- [Fix pseudo selectivity estimation for the primary key](https://github.com/pingcap/tidb/pull/6302)
- [Eliminate `Projection` when the schema length is `0`](https://github.com/pingcap/tidb/pull/6318)
- [Set the hash join concurrency in `NewSessionVars`](https://github.com/pingcap/tidb/pull/6295)

## Improved

- [Refactor `scalarFuncToPBExpr`](https://github.com/pingcap/tidb/pull/6290)
- [Improve the cost estimation for physical aggregate operators](https://github.com/pingcap/tidb/pull/6307)
- [Improve the execution performance of the `UnionScanExec` operator](https://github.com/pingcap/tidb/pull/6312)
- [Cache global variables](https://github.com/pingcap/tidb/pull/6315)

# Weekly update in TiSpark

Last week, we landed [8 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-04-16..2018-04-22) in the TiSpark repositories.

## Fixed

- [Fix the binary test and delete redundant issue tests](https://github.com/pingcap/tispark/pull/317)
- [Fix `Protobuf` definition according to TiKV changes](https://github.com/pingcap/tispark/pull/318)

# Weekly update in TiKV and PD

Last week, we landed [29 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-04-16..2018-04-22&type=) in the TiKV and PD repositories.

## Added

- [Support specifying `ColumnFamily` in the `rawkv` APIs](https://github.com/pingcap/tikv/pull/2852)
- [Add a new Region score function for balance that considers the free space of TiKV](https://github.com/pingcap/pd/pull/1014)
- [Support `ScatterRegion`](https://github.com/pingcap/pd/pull/1028)

## Fixed

- [Fix the issue of reloading without persisted schedulers](https://github.com/pingcap/pd/pull/1021)
- [Fix wrongly collected Coprocessor statistics](https://github.com/pingcap/tikv/pull/2951)
- [Bump the recursion limit to 200](https://github.com/pingcap/tikv/pull/2958)

## Improved

- [Upgrade the Rust and Clippy versions](https://github.com/pingcap/tikv/pull/2922)
- [Add metrics to `FuturePool`](https://github.com/pingcap/tikv/pull/2932)
- [Reduce the lock contention in `WORKER`](https://github.com/pingcap/tikv/pull/2933)