---
title: Weekly update (October 15 ~ October 21, 2018)
date: 2018-10-22
summary: Last week, we landed 60 PRs in the TiDB repository, 2 PRs in the TiSpark repository, and 16 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [60 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-10-15..2018-10-21+) in the TiDB repository.

## Added

* [Add the slow log for the `Commit` statement](https://github.com/pingcap/tidb/pull/7964)
* [Support cross-domain requests in the HTTP API](https://github.com/pingcap/tidb/pull/7939)
* [Add the `PreAlloc4Row` and `Insert` functions for `Chunk` and `List`](https://github.com/pingcap/tidb/pull/7916)
* [Implement `Operand` and `Pattern` of the `cascades` planner](https://github.com/pingcap/tidb/pull/7910)
* [Add the TiDB version to DDL metrics](https://github.com/pingcap/tidb/pull/7902)
* [Add a session variable to make `Insert` compatible with MySQL](https://github.com/pingcap/tidb/pull/7863)
* [Add the `json_keys` built-in function](https://github.com/pingcap/tidb/pull/7776)
* [Add an `EXPLAIN` test for partition pruning](https://github.com/pingcap/tidb/pull/7505)

## Improved

* [Improve the MySQL compatibility by adding the `USAGE` privilege for the `showGrants` statement](https://github.com/pingcap/tidb/pull/7955)
* [Log more information when `OtherError` occurs in `coprocessor`](https://github.com/pingcap/tidb/pull/7948)
* [Update the Delta information for the partitioned table in statistics](https://github.com/pingcap/tidb/pull/7947)
* [Limit the length of sample values in statistics](https://github.com/pingcap/tidb/pull/7931)
* [Refine `ColumnPrune` for `LogicalUnionAll`](https://github.com/pingcap/tidb/pull/7930)
* [Eliminate `if null` on the non-`null` column when building `Projection`](https://github.com/pingcap/tidb/pull/7924)
* [Support `Group` and `GroupExpr` for the `cascades` planner](https://github.com/pingcap/tidb/pull/7917)
* [Eliminate `projection` after aggregation pruning](https://github.com/pingcap/tidb/pull/7909)
* [Handle the DDL event for the partitioned table in statistics](https://github.com/pingcap/tidb/pull/7903)
* [Refine `Explain Analyze`](https://github.com/pingcap/tidb/pull/7888)
* [Remove the `kv.BypassLatch` option and enable the latch scheduler by default](https://github.com/pingcap/tidb/pull/7882)
* [Refine the error log when the DDL job is canceled](https://github.com/pingcap/tidb/pull/7875)
* [Improve the MySQL compatibility for the `current_user()` built-in function](https://github.com/pingcap/tidb/pull/7801)
* [Propagate constants over `outer join`](https://github.com/pingcap/tidb/pull/7794)
* [Support changing `null` to `not null` in the `alter table` statement](https://github.com/pingcap/tidb/pull/7771)

## Fixed

* [Fix an invalid DDL job which makes TiDB panic](https://github.com/pingcap/tidb/pull/7940)
* [Fix a panic in `limit N` when `N` is too large and overflows an integer](https://github.com/pingcap/tidb/pull/7936)
* [Fix a bug in `point get`](https://github.com/pingcap/tidb/pull/7934)
* [Fix date time parsing for the `YYYY-MM-DD HH` format](https://github.com/pingcap/tidb/pull/7933)
* [Maintain `DeferredExpr` in aggressive constant folding](https://github.com/pingcap/tidb/pull/7915)
* [Fix a panic caused by the empty histogram in statistics](https://github.com/pingcap/tidb/pull/7912)
* [Fix a panic caused by the empty schema of `LogicalTableDual`](https://github.com/pingcap/tidb/pull/7906)
* [Fix data race when initializing the `systemTZ` variable](https://github.com/pingcap/tidb/pull/7901)
* [Fix the `admin check table` bug of byte comparing](https://github.com/pingcap/tidb/pull/7887)
* [Add the check in DDL when creating a table with a foreign key](https://github.com/pingcap/tidb/pull/7885)
* [Fix the histogram boundaries overflow error in statistics](https://github.com/pingcap/tidb/pull/7883)
* [Convert `DataSource` to `TableDual` only when the empty range is not derived from parameterized constants](https://github.com/pingcap/tidb/pull/7808)

# Weekly update in TiSpark

Last week, we landed [2 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-10-15..2018-10-21+) in the TiSpark repository.

## Fixed

* [Fix a bug in `pyspark` in Spark 2.3 that does not initialize a session correctly](https://github.com/pingcap/tispark/pull/460)

# Weekly update in TiKV and PD

Last week, we landed [16 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-10-15..2018-10-21&type=Issues) in the TiKV and PD repositories.

## Added

- Support more functions in Coprocessor:
    
    * [`Exp`](https://github.com/tikv/tikv/pull/3686)
    * [`Radians`](https://github.com/tikv/tikv/pull/3683)

- [Add the version information for tikv-ctl](https://github.com/tikv/tikv/pull/3662)
- [Add `tikv raftstore event duration` to metrics](https://github.com/tikv/tikv/pull/3657)

## Fixed

- [Fix the cluster test of PD](https://github.com/pingcap/pd/pull/1278)
- [Fix the building failure on Mac OS X](https://github.com/pingcap/pd/pull/1275)
- [Fix `WaitGroup` data race](https://github.com/pingcap/pd/pull/1273)

## Improved

- [Remove the PD source code and build binary from the docker image](https://github.com/pingcap/pd/pull/1283)
- [Update pd-ctl commands `health` and `topsize`](https://github.com/tikv/tikv/pull/3684)
- [Release TiKV v2.0.8](https://github.com/tikv/tikv/pull/3676)
- [Use the implicit project layout](https://github.com/tikv/tikv/pull/3674)
- [Export `ThreadCollector` to use it later](https://github.com/tikv/tikv/pull/3672)
- [Introduce `eval_func` and `eval_func_with helper`](https://github.com/tikv/tikv/pull/3670)
- [Extract `panic_hook`](https://github.com/tikv/tikv/pull/3666)
- [Use `go mod` to manage dependency](https://github.com/pingcap/pd/pull/1269)

# New contributor (Thanks!)

tidb: [tianjiqx](https://github.com/tianjiqx)
