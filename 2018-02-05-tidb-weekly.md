---
title: Weekly update (January 29 ~ February 04, 2018)
date: 2018-02-05
summary: Last week, we landed 35 PRs in the TiDB repositories, 6 PRs in the TiSpark repositories, and 22 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [35 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is:pr+is:merged+merged:2018-01-29..2018-02-04) in the TiDB repositories.

## Added

* [Support the `load stats` command](https://github.com/pingcap/tidb/pull/5724)

## Removed

* [Remove `iota` in DDL package to make the constant clearer](https://github.com/pingcap/tidb/pull/5753)

## Fixed

* [`limit` and `offset` can be parameter markers in the prepared statement](https://github.com/pingcap/tidb/pull/2364)
* [`IndexOption` can be a list in creating a table](https://github.com/pingcap/tidb/pull/2366)
* [Fix the bug of some field length missing in creating a table](https://github.com/pingcap/tidb/pull/2382)
* [Fix the bug of parsing `Datetime` overflow](https://github.com/pingcap/tidb/pull/2401)
* [Trim leading zeros before parsing integer `literal`](https://github.com/pingcap/tidb/pull/2404)
* [Fix the float truncate bug](https://github.com/pingcap/tidb/pull/2405)

## Improved

* [Importer tools support `loadStats` by path](https://github.com/pingcap/tidb/pull/5768/files)
* [Support mock table info for importer tools](https://github.com/pingcap/tidb/pull/5759/files)
* [Let `DO` statement be a read only statement](https://github.com/pingcap/tidb/pull/5752)
* [Improve an error handling in `ddl`](https://github.com/pingcap/tidb/pull/5748/files)
* [Reduce memory allocation in `buildDataSource`](https://github.com/pingcap/tidb/pull/5747)
* [Make `Explain` clearer](https://github.com/pingcap/tidb/pull/5742)
* [Add the metrics package and recover `Panic` of `Worker`](https://github.com/pingcap/tidb/pull/5733)
* [Refine the `joinResult` generator to return `maxChunkSize` chunk](https://github.com/pingcap/tidb/pull/5715)
* [Limit `lock` count for `ScanLock` request](https://github.com/pingcap/tidb/pull/5606)
* [Enhance the `IndexRange` calculation](https://github.com/pingcap/tidb/pull/5611)
* Refine metrics in TiDB:
    - [Refine `DistSQL` metrics](https://github.com/pingcap/tidb/pull/5774)
    - [Add metrics for the meta package](https://github.com/pingcap/tidb/pull/5770)
    - [Move and refine the server metrics](https://github.com/pingcap/tidb/pull/5766)
    - [Add metrics for DDL syncer](https://github.com/pingcap/tidb/pull/5765)
    - [Update metrics for `session`](https://github.com/pingcap/tidb/pull/5762)

# Weekly update in TiSpark

Last week, we landed [6 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-01-29..2018-02-04) in the TiSpark repositories.

## Improved

* [Switch integration test to `scalatest` framework](https://github.com/pingcap/tispark/pull/127)

## Fixed

* [Fix `Average` on BIGINT overflow](https://github.com/pingcap/tispark/pull/231)
* [Fix `scala` version for some libraries](https://github.com/pingcap/tispark/pull/228)

# Weekly update in TiKV and PD

Last week, we landed [22 PRs](https://github.com/search?q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-01-29..2018-02-04) in the TiKV and PD repositories.

## Added

* [PD: implement `GetAllStores` API](https://github.com/pingcap/pd/pull/937)
* [TiKV: implement `GetAllStores` API](https://github.com/pingcap/tikv/pull/2722)
* [Add PD health API](https://github.com/pingcap/pd/pull/941)
* [Support setting `leader` priority to etcd members](https://github.com/pingcap/pd/pull/942)
* [Sync the PD leader with the etcd leader](https://github.com/pingcap/pd/pull/945)
* [Add the `future` pool](https://github.com/pingcap/tikv/pull/2725)

## Fixed

* [Fix hot Region `DistinctScoreFilter`](https://github.com/pingcap/pd/pull/934)
* [Fix and update Region size](https://github.com/pingcap/tikv/pull/2715)
* [Fix `cleanup` for raw KV](https://github.com/pingcap/tikv/pull/2724)

## Improved

* [Check Range for DAG and analysis](https://github.com/pingcap/tikv/pull/2698)
* [Sync the snapshots](https://github.com/pingcap/tikv/pull/2719)
* [Remove the sync snapshot file](https://github.com/pingcap/tikv/pull/2723)
* [Add operator duration metrics](https://github.com/pingcap/pd/pull/935)
* [Support simple command line args](https://github.com/pingcap/tikv/pull/2637)
* [Add Region statistics](https://github.com/pingcap/pd/pull/936)
* [Clear stale data using `DeleteFilesInRanges`](https://github.com/pingcap/tikv/pull/2731)

# New contributor (Thanks!)

* TiDB: [Boik](https://www.github.com/qazbnm456)
