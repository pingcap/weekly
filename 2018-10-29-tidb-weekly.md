---
title: Weekly update (October 22 ~ October 28, 2018)
date: 2018-10-29
summary: Last week, we landed 52 PRs in the TiDB repository and 31 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [52 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-10-22..2018-10-28+) in the TiDB repository.

## Added

* [Support `ShowStats` for the partitioned tables](https://github.com/pingcap/tidb/pull/8023)
* [Support `:=` in the `set` syntax](https://github.com/pingcap/tidb/pull/8018)
* [Enable range typed table partition](https://github.com/pingcap/tidb/pull/8011)
* [Add the proposal for the column pool](https://github.com/pingcap/tidb/pull/7988)
* [Add the log for the binary executed statement](https://github.com/pingcap/tidb/pull/7987)
* [Add the slow log for the `commit` statement](https://github.com/pingcap/tidb/pull/7983)
* [Add the proposal of maintaining histograms in the plan](https://github.com/pingcap/tidb/pull/7605)

## Improved

* [Use the Pump client to write binlogs](https://github.com/pingcap/tidb/pull/8070)
* [Export the function `init()` to `Init()` in the `planner` package](https://github.com/pingcap/tidb/pull/8060)
* [Support `_tidb_rowid` for table scan range](https://github.com/pingcap/tidb/pull/8047)
* [Move the `parser` package to a separate repository](https://github.com/pingcap/tidb/pull/8036)
* [Update the error rate for the partitioned tables in statistics](https://github.com/pingcap/tidb/pull/8022)
* [Refine the built-in function `truncate` to support the `uint` argument](https://github.com/pingcap/tidb/pull/8000)
* [Split unit tests to the corresponding files in the `executor`/`aggfuncs` package](https://github.com/pingcap/tidb/pull/7993)
* [Add the unit test for the `executor`/`aggfuncs` package](https://github.com/pingcap/tidb/pull/7966)
* [Use the local feedback for the partitioned tables in statistics](https://github.com/pingcap/tidb/pull/7963)
* [Support GC for partition table statistics](https://github.com/pingcap/tidb/pull/7962)
* [Make `INFORMATION_SCHEMA` the first one in `show databases`](https://github.com/pingcap/tidb/pull/7938)
* [Improve the `Insert` and `Update` performance for wide tables](https://github.com/pingcap/tidb/pull/7935)
* [Use `rowDecoder` to decode data and evaluate the generated column for `AdminCheck`](https://github.com/pingcap/tidb/pull/7862)

## Fixed

* [Disable the plan cache for queries containing `SubqueryExpr`](https://github.com/pingcap/tidb/pull/8064)
* [Fix the issue of executing DDL after executing the SQL failure in a transaction](https://github.com/pingcap/tidb/pull/8044)
* [Fix the wrong result when the `index join` operation is performed on union scan](https://github.com/pingcap/tidb/pull/8031)
* [Fix a panic of the prepared statement with `IndexScan` when using the prepared plan cache](https://github.com/pingcap/tidb/pull/8017)
* [Fix estimation for the out of range point queries in statistics](https://github.com/pingcap/tidb/pull/8015)
* [Clone the schema of `projection` for different children in the `buildProj4Union` function](https://github.com/pingcap/tidb/pull/7999)
* [Correct the schema after the execution of operations is cancelled halfway](https://github.com/pingcap/tidb/pull/7997)
* [Fix the bug that the reassigned partition ID in `truncate table` does not take effect](https://github.com/pingcap/tidb/pull/7919)

# Weekly update in TiKV and PD

Last week, we landed [31 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-10-22..2018-10-28&type=Issues) in the TiKV and PD repositories.

## Added

- Support more functions in Coprocessor:
    
    - [`Trim`](https://github.com/tikv/tikv/pull/3698)
    - [`Conv`](https://github.com/tikv/tikv/pull/3691)

- [Support producing an Alpine Linux image](https://github.com/tikv/tikv/pull/3697)

## Fixed

- [Avoid unsafe mutation for `scan_mode`](https://github.com/tikv/tikv/pull/3696)
- [Fix data race in PD `RaftCluster`](https://github.com/pingcap/pd/pull/1272)

## Improved

- [Add `on_stall_conditions_changed` to `EventListener` in TiKV](https://github.com/tikv/tikv/pull/3712)
- [Support adding more schedulers by pd-ctl](https://github.com/pingcap/pd/pull/1288)
- [Add `tikv_raftstore_event_duration` to metrics](https://github.com/tikv/tikv/pull/3700)
- [Support more server configuration parameters in the PD simulator](https://github.com/pingcap/pd/pull/1281)
- [Support more Region key formats in the pd-ctl detach mode](https://github.com/pingcap/pd/pull/1298)
- [Use the same initial cluster configuration to restart the joined member](https://github.com/pingcap/pd/pull/1279)
- [Support the day format in `ReadableDuration`](https://github.com/tikv/tikv/pull/3687)

# New contributors (Thanks!)

tikv:

- [killme2008](https://github.com/killme2008)

tidb:

- [HaraldNordgren](https://github.com/HaraldNordgren)
- [parastorli](https://github.com/parastorli)
- [yu34po](https://github.com/yu34po)

tidb-operator:

- [liufuyang](https://github.com/liufuyang)