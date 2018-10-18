---
title: Weekly update (June 25 ~ July 01, 2018)
date: 2018-07-02
summary: Last week, we landed 39 PRs in the TiDB repositories and 25 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [39 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-06-25..2018-07-01) in the TiDB repositories.

## Added

- [Add a session variable `tidb_ddl_reorg_worker_cnt` to control the number of the DDL organization workers](https://github.com/pingcap/tidb/pull/6441)
- [Support parallel `HASH` aggregation and greatly improve the performance of the aggregation function](https://github.com/pingcap/tidb/pull/6658)
- [Print `explain` results in a tree style](https://github.com/pingcap/tidb/pull/6894)
- [Support the `SHOW ERRORS` statement and improve the `SHOW WARNINGS` statement](https://github.com/pingcap/tidb/pull/6936)

## Fixed

- [Make the `INSERT IGNORE` statement ignore `BadNullError`](https://github.com/pingcap/tidb/pull/6465)
- [Fix a bug when `only_full_group_by` is set in `SQL_MODE`](https://github.com/pingcap/tidb/pull/6734)
- [Fix the wrong results of `avg(double)`](https://github.com/pingcap/tidb/pull/6888)
- [Make the `CREATE TABLE IF NOT EXISTS LIKE` statement work again](https://github.com/pingcap/tidb/pull/6896)
- [Set the correct `startHandle` when some errors occur in adding indexes](https://github.com/pingcap/tidb/pull/6897)
- [Fix a bug in pushing down `TopN`](https://github.com/pingcap/tidb/pull/6899)
- [Fix the response result bug of `COM_FIELD_LIST`](https://github.com/pingcap/tidb/pull/6918)
- [Fix a bug of the `str_to_date()` function](https://github.com/pingcap/tidb/pull/6919)
- [Fix a bug of the `INSERT` statement when the field type is unsigned `float`/`double`](https://github.com/pingcap/tidb/pull/6939)

## Improved

- [Use the average error of the row count which is estimated by statistics to determine the pseudo column](https://github.com/pingcap/tidb/pull/6565)
- [Use `CorrelatedColumn` to calculate range](https://github.com/pingcap/tidb/pull/6779)
- [Make the frequency of updating the statistic metadata depend on the table size](https://github.com/pingcap/tidb/pull/6808)
- [Refactor the execution framework of the aggregate functions](https://github.com/pingcap/tidb/pull/6852)
- [Speed up the `CreateTable` operation](https://github.com/pingcap/tidb/pull/6861)
- [Stop calling `expression.Clone` in the `plan` package except `ResolveIndices`](https://github.com/pingcap/tidb/pull/6866)
- [Handle `\N` as `NULL` in `LOAD DATA`](https://github.com/pingcap/tidb/pull/6873)
- [Avoid holding the Write lock for a long time](https://github.com/pingcap/tidb/pull/6880)
- [Reduce the memory usage in the `INSERT INTO SELECT` statement](https://github.com/pingcap/tidb/pull/6891)
- [Enhance the row count estimation when the correlated column exists](https://github.com/pingcap/tidb/pull/6911)
- [Check the character set capitalization when creating a table](https://github.com/pingcap/tidb/pull/6914)
- [Improve the `accessPath` for the unique key](https://github.com/pingcap/tidb/pull/6925)

# Weekly update in TiKV and PD

Last week, we landed [25 PRs](https://github.com/search?p=1&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-06-25..2018-07-01&type=Issues&utf8=%E2%9C%93) in the TiKV and PD repositories.

## Added

- [Support splitting a Region by key using `tikv-ctl`](https://github.com/pingcap/tikv/pull/3244)
- [Provide `PerfContext` statistics in Coprocessor](https://github.com/pingcap/tikv/pull/3236)
- [Fuzz decimals](https://github.com/pingcap/tikv/pull/3190)
- [Collect thread state metrics](https://github.com/pingcap/tikv/pull/3173)

## Fixed

- [Fix the issue that the store runs out of space due to moving replicas](https://github.com/pingcap/pd/pull/1123)
- [Fix a bug in `do_sub` when the last nonzero digit is before the point](https://github.com/pingcap/tikv/pull/3223)
- [Fix potential stale Read during merging](https://github.com/pingcap/tikv/pull/3116)
- [Handle heartbeats of Regions with changed peers](https://github.com/pingcap/pd/pull/1119)

## Improved

- [Return the `UnknownSignature` error for unimplemented signatures](https://github.com/pingcap/tikv/pull/3246)
- [Remove `Box<>` around `Cursor`, `Snapshot` and `Engine`](https://github.com/pingcap/tikv/pull/3239)
- [Upgrade Rust to the `nightly-2018-06-14` version](https://github.com/pingcap/tikv/pull/3208)

# New contributors (Thanks!)

TiDB:

- [cityonsky](https://github.com/cityonsky)
- [mail2fish](https://github.com/mail2fish)

Docs:

- [yejiayu](https://github.com/yejiayu)