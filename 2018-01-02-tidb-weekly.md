---
title: Weekly update (December 25 ~ December 31, 2017)
date: 2018-01-02
summary: Last week, we landed 36 PRs in the TiDB repositories, 12 PRs in the TiSpark repositories, and 18 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [36 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2017-12-25..2017-12-31) in the TiDB repositories.

## Added

* [Add the Iterator interface in `Chunk`.](https://github.com/pingcap/tidb/pull/5476/files)

## Removed

* [Remove the useless aggregation function during `buildQuantifierPlan`.](https://github.com/pingcap/tidb/pull/5510)

## Fixed

* [`Flen` and `Decimal` of `TypeNewDecimal` should not be `-1`.](https://github.com/pingcap/tidb/pull/5523)
* [To pass sysbench Prepare tests, set `Fields` for `SelectStmt` in `PrepareExec`.](https://github.com/pingcap/tidb/pull/5504)
* [Fix the case that fails to split a table.](https://github.com/pingcap/tidb/pull/5496)
* [Correct the type inference of the `sum` and `avg` functions.](https://github.com/pingcap/tidb/pull/5495)
* [Make `set transaction read only` work, compatible with `JDBC` connector.](https://github.com/pingcap/tidb/pull/5483)

## Improved

* [Change `BuildRange` to build `column/index/table` range to improve performance.](https://github.com/pingcap/tidb/pull/5509)
* [Make `KvEncoder` support encoding Prepare SQL.](https://github.com/pingcap/tidb/pull/5505)
* [Refine codes about `maxOneRow`.](https://github.com/pingcap/tidb/pull/5501)
* [Use `chunk.Iterator` for `joinGenerator`.](https://github.com/pingcap/tidb/pull/5500)
* [Merge `ranger.IndexRange` and `ranger.ColumnRange` to `ranger.NewRange`.](https://github.com/pingcap/tidb/pull/5485)
* [Reduce allocation for `DetachCondsForSelectivity`, and add a Filter function.](https://github.com/pingcap/tidb/pull/5482)
* [Support alter table `auto_increment`.](https://github.com/pingcap/tidb/pull/5472)
* [Support pushing down stream aggregation on `mocktikv`.](https://github.com/pingcap/tidb/pull/5444)
* Support `Chunk` in executors: 
    - [`NestedLoopApply`](https://github.com/pingcap/tidb/pull/5475)
    - [`UnionScanExec`](https://github.com/pingcap/tidb/pull/5432)

# Weekly update in TiSpark

Last week, we landed [12 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2017-12-25..2017-12-31) in the TiSpark repositories.

## Improved

* [Dynamically downgrade the index scan plan to table scan plan.](https://github.com/pingcap/tispark/pull/140)
* [Optimize the column logic of Aggregation pushing down.](https://github.com/pingcap/tispark/pull/143)
* [Add the date type pushing down logic.](https://github.com/pingcap/tispark/pull/146)
* [Reduce dependencies.](https://github.com/pingcap/tispark/pull/190)
* [Add tests for issues.](https://github.com/pingcap/tispark/pull/165)
* [Add switching to ignore the unsupported type.](https://github.com/pingcap/tispark/pull/156)
* [Use the parent child POM mode instead of submodule.](https://github.com/pingcap/tispark/pull/159)

## Fixed

* [Fix the NPE issue of Aggregation pushing down.](https://github.com/pingcap/tispark/pull/164)
* [Remove time test cases.](https://github.com/pingcap/tispark/pull/166)
* [Modify integration scripts and `.gitignore` files.](https://github.com/pingcap/tispark/pull/171)
* [Remove the Scala lang provided in the POM file.](https://github.com/pingcap/tispark/pull/173)
* [Delete the unnecessary variable.](https://github.com/pingcap/tispark/pull/163)

# Weekly update in TiKV and PD

Last week, we landed [18 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-12-25..2017-12-31) in the TiKV and PD repositories.

## Added

* [Support builtin aggregation functions `bit_and`, `'bit_or` and `bit_xor` in Coprocessor.](https://github.com/pingcap/tikv/pull/2510)
* [Upgrade the version of gRPC-rs to 0.2.](https://github.com/pingcap/tikv/pull/2545)
* [Make `delete_range` configurable.](https://github.com/pingcap/tikv/pull/2573)
* [Enable table split by default.](https://github.com/pingcap/tikv/pull/2575)
* [Add trend API in PD.](https://github.com/pingcap/pd/pull/881)
* [Increase the priority of the raftstore thread.](https://github.com/pingcap/tikv/pull/2578)
* [Add `ScatterRegion` API in PD.](https://github.com/pingcap/pd/pull/890)
* [Move SST instead of copying in injestion.](https://github.com/pingcap/tikv/pull/2600)
* [Update the version of fail-rs to 0.2.](https://github.com/pingcap/tikv/pull/2620)

## Fixed

* [Fix the return type of `avg` and `sum` in Coprocessor.](https://github.com/pingcap/tikv/pull/2589)
* [Catch stale command in the scheduler.](https://github.com/pingcap/tikv/pull/2619)
* [Fix build error on macOS.](https://github.com/pingcap/tikv/pull/2628)

## Improved

* [Clean up the select interface in Coprocessor.](https://github.com/pingcap/tikv/pull/2606)
* [Collect metrics more efficiently in Coprocessor.](https://github.com/pingcap/tikv/pull/2616)
* [Make fail point tests more stable.](https://github.com/pingcap/tikv/pull/2621)

# New contributor (Thanks!)

* TiKV: [Rain Li](https://github.com/blacktear23)

