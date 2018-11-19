---
title: Weekly update (November 12 ~ November 18, 2018)
date: 2018-11-19
summary: Last week, we landed 54 PRs in the TiDB repository, 3 PRs in the TiSpark repository, and 29 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [54 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-11-12..2018-11-18+) in the TiDB repository.

## Added

- [Add a variable `max-txn-time-use` to make `maxTxnTimeUse` configurable](https://github.com/pingcap/tidb/pull/8215)

## Improved

- [Validate the variable value when you set `tx_isolation`](https://github.com/pingcap/tidb/pull/8299)
- [Refine `HashJoinExec` of a specific JoinType for the nil outer/inner case](https://github.com/pingcap/tidb/pull/8296)
- [Add SQL type labels to commit and retry logs](https://github.com/pingcap/tidb/pull/8281)
- [Delay initializing `Txn()` to the statements that really need it](https://github.com/pingcap/tidb/pull/8260)
- [Adjust the `TIDB_INLJ` Hint to specify the inner table](https://github.com/pingcap/tidb/pull/8243)
- [Support the `NO_AUTO_CREATE_USER` SQL mode](https://github.com/pingcap/tidb/pull/8160)
- [Validate specified values for the `enum/set` type column in DDL](https://github.com/pingcap/tidb/pull/8003)

## Fixed

- [Clone `AggDesc` before modifying its `Mode` in `AggDesc.Split`](https://github.com/pingcap/tidb/pull/8328)
- [Close the child executor before calling `ExplainExec.explain.RenderResult()`](https://github.com/pingcap/tidb/pull/8324)
- [Escape backquotes in identifiers in `SHOW CREATE TABLE` properly](https://github.com/pingcap/tidb/pull/8302)
- [Convert `Zero` input correctly for column type `year`](https://github.com/pingcap/tidb/pull/8292)
- [Eliminate extra columns introduced by `OrderBy` upon `Union`](https://github.com/pingcap/tidb/pull/8290)
- [Fix the error caused by different lengths between embedded and outer `OrderByItems`s](https://github.com/pingcap/tidb/pull/8273)
- [Consider null for comparing operators in expression rewriting](https://github.com/pingcap/tidb/pull/8269)
- [Impose specified `OrderBy` on the union result of `TableDual`](https://github.com/pingcap/tidb/pull/8251)
- [Use `Column.UniqueID` in `conditionChecker` of `ranger`](https://github.com/pingcap/tidb/pull/8236)

# Weekly update in TiSpark

Last week, we landed [3 PRs](https://github.com/pingcap/tispark/pulls?page=1&q=is%3Apr+is%3Amerged+merged%3A2018-11-12..2018-11-18&utf8=%E2%9C%93) in the TiSpark repository.

## Added

- [Add the partition information in `TiTableInfo`](https://github.com/pingcap/tispark/pull/486)

## Fixed

- [Fix isolation level settings](https://github.com/pingcap/tispark/pull/488)

# Weekly update in TiKV and PD

Last week, we landed [29 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-11-12..2018-11-18&type=Issues) in the TiKV and PD repositories.

## Added

- [Add a memory `BTreeEngine` for the local test](https://github.com/tikv/tikv/pull/3723)
- [Support reversing `raw_scan` and `raw_batch_scan` in storage](https://github.com/tikv/tikv/pull/3724)
- [Add the `ldb` argument in tikv-ctl to support the `rocksdb` command](https://github.com/tikv/tikv/pull/3753)
- Support more functions in Coprocessor: 
	
    * [`ToBase64` and `FromBase64`](https://github.com/tikv/tikv/pull/3716)
    * [`Substring2Args` and `Substring3Args`](https://github.com/tikv/tikv/pull/3742)
    * [`DayName`, `DayOfMouth`, `DayOfWeek` and `DayOfYear`](https://github.com/tikv/tikv/pull/3774)

## Improved

- [Use a block strategy for the file logger](https://github.com/tikv/tikv/pull/3755)
- [Use `lifetime` to manage the start and the stop of `Storage`](https://github.com/tikv/tikv/pull/3769) 
- [Optimize ingesting snapshots](https://github.com/tikv/tikv/pull/3775)
- [Avoid large Write batch during the GC process of Raft logs](https://github.com/tikv/tikv/pull/3788)
- [Omit some logs about `compact log`](https://github.com/tikv/tikv/pull/3798)
- [Check the store state before creating operators](https://github.com/pingcap/pd/pull/1326)

## Fixed

- [Fix the issue about parsing ambiguous time](https://github.com/tikv/tikv/pull/3786)

# New contributor (Thanks!)

tikv: [kamijin-fanta](https://github.com/kamijin-fanta)