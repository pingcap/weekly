---
title: Weekly update (April 22 ~ April 28, 2019)
date: 2019-04-29
summary: Last week, we landed 59 PRs in the TiDB repository, 14 PRs in the TiSpark repository, and 25 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [59 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-04-22..2019-04-28+) in the TiDB repository.

## Added

- [Support `drop session binding`](https://github.com/pingcap/tidb/pull/10287)
- [Support `show session bindings`](https://github.com/pingcap/tidb/pull/10285)
- [Support `add session binding`](https://github.com/pingcap/tidb/pull/10247)
- [Support `show analyze status`](https://github.com/pingcap/tidb/pull/10172)
- [Support building `CMSketch` with Top-N](https://github.com/pingcap/tidb/pull/10163)
- [Support incremental `Analyze` for indexes without feedback updates](https://github.com/pingcap/tidb/pull/10102)

## Improved

- [Add cop-tasks and memory information into the `slow_query` table](https://github.com/pingcap/tidb/pull/10264)
- [Support building statistics on samples from fast `Analyze`](https://github.com/pingcap/tidb/pull/10258)
- [Add memory tables to store TiKV status](https://github.com/pingcap/tidb/pull/10248)
- [Check inconsistent indexes in `IndexLookupExecutor`](https://github.com/pingcap/tidb/pull/10237)
- [Remove some unused gRPC metrics in the TiKV client](https://github.com/pingcap/tidb/pull/10233)
- [Predefine metrics labels in the `conn/session` package to improve the performance](https://github.com/pingcap/tidb/pull/10232)
- [Predefine metrics labels in the `plan/executor` package to improve the performance](https://github.com/pingcap/tidb/pull/10231)
- [Predefine metrics labels in the `store` package to improve the performance](https://github.com/pingcap/tidb/pull/10229)
- [Reduce `alloc` and `lock-hold-time` caused by counting errors and warnings](https://github.com/pingcap/tidb/pull/10223)
- [Make `SHOW COLLATIONS` show supported collations only](https://github.com/pingcap/tidb/pull/10186)
- [Lazily evaluate `explainID` and the memory tracker label to improve the performance](https://github.com/pingcap/tidb/pull/10139)
- [Add `pre_split_regions` when creating a table with `shard_row_id_bits`](https://github.com/pingcap/tidb/pull/10138)
- [Take more prefix columns into account when building ranges](https://github.com/pingcap/tidb/pull/10053)
- [Support the column collate syntax `create table t(col type collate...)`](https://github.com/pingcap/tidb/pull/9947)
- [Improve the row count estimation by using column order correlation](https://github.com/pingcap/tidb/pull/9839)
- [Make Join reorder by dynamic programming work](https://github.com/pingcap/tidb/pull/8816)

## Fixed

- [Fix the panic when moving `Analyze` jobs to `history`](https://github.com/pingcap/tidb/pull/10286)
- [Fix wrong `PointGet` judgement conditions in some cases](https://github.com/pingcap/tidb/pull/10278)
- [Fix the issue that the slow log parser parses logs wrongly when a slow log includes `#`](https://github.com/pingcap/tidb/pull/10271)
- [Fix the issue that `distinct` on multiple strings returns wrong results in some cases](https://github.com/pingcap/tidb/pull/10225)
- [Fix the wrong behavior of `group_concat(distinct)` in some cases](https://github.com/pingcap/tidb/pull/10108)

# Weekly update in TiSpark

Last week, we landed [14 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-04-22..2019-04-28+) in the TiSpark repository.

## Added

- [Support `Spark 2.4.x` with the maven profile](https://github.com/pingcap/tispark/pull/665)

## Fixed

- [Fix the retry method in `Scan` when encountering locks](https://github.com/pingcap/tispark/pull/666)
- [Fix the `next()` implementation in the point key](https://github.com/pingcap/tispark/pull/667)
- [Fix inconsistent timestamps of different tables in the same plan](https://github.com/pingcap/tispark/pull/676)
- [Fix the issue that the supported Spark version is not updated in the maven profile](https://github.com/pingcap/tispark/pull/679)
- [Fix the issue that the `desc formatted table` command for hive tables might lead to `ArrayIndexOutOfBoundException`](https://github.com/pingcap/tispark/pull/686)

# Weekly update in TiKV and PD

Last week, we landed [25 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-04-22..2019-04-28&type=Issues) in the TiKV and PD repositories.

## Added

* [Add a speed limit for `tikv-importer`](https://github.com/tikv/tikv/pull/4412)
* [Implement the `period_add` and `period_diff` Coprocessor functions](https://github.com/tikv/tikv/pull/4428)
* [Add the check command for `operators`](https://github.com/pingcap/pd/pull/1512)
* [Add the `GetOperator` service](https://github.com/pingcap/pd/pull/1514)
* [Add `BatchSelectionExecutor`](https://github.com/tikv/tikv/pull/4562)
* [Add the `COUNT` batch aggregate function](https://github.com/tikv/tikv/pull/4569)

## Improvement

* [Disable unused features of dependencies](https://github.com/tikv/tikv/pull/4453)
* [Add `storeID` to metrics back](https://github.com/pingcap/pd/pull/1506)
* [Utilize the `iter_batched_ref` new feature of Criterion](https://github.com/tikv/tikv/pull/4539)
* [Add a timeout for the HTTP client](https://github.com/pingcap/pd/pull/1515)
* [Improve some logs](https://github.com/pingcap/pd/pull/1516)
* [Add `jq` and cache dependencies for the `docker` image](https://github.com/pingcap/pd/pull/1519)
* [Use the memory to cache split `SST` instead of disk files](https://github.com/tikv/tikv/pull/4566)
* [Upgrade the Rust compiler version to `2019-04-25`](https://github.com/tikv/tikv/pull/4568)

## Fixed

* [Fix the problem of not considering the learner in the merge process](https://github.com/tikv/tikv/pull/4559)
* [Fix the sending error failure in `heartbeat stream`](https://github.com/pingcap/pd/pull/1521)

# New contributors (Thanks!)

tikv:

- [Seact](https://github.com/Seact)
- [jswh](https://github.com/jswh)
- [psinghal20](https://github.com/psinghal20)