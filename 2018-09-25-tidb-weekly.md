---
title: Weekly update (September 17 ~ September 23, 2018)
date: 2018-09-25
summary: Last week, we landed 29 PRs in the TiDB repository and 14 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [29 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-09-17..2018-09-23+) in the TiDB repository.

## Added

* [Support dumping statistics for partitioned tables](https://github.com/pingcap/tidb/pull/7753)
* [Add a variable to control the statement priority of a TiDB server](https://github.com/pingcap/tidb/pull/7694)
* [Add a `WithRecovery()` function in the `util` package](https://github.com/pingcap/tidb/pull/7666)

## Improved

* [Remove the `DDL` version in metrics](https://github.com/pingcap/tidb/pull/7737)
* [Set `TiDBMemQuotaQuery` to the value in the configuration file](https://github.com/pingcap/tidb/pull/7729)
* [Prune columns for `LogicalTableDual`](https://github.com/pingcap/tidb/pull/7725)
* [Optimize the `IsPoint()` function for performance](https://github.com/pingcap/tidb/pull/7722)
* [Support `limit`/`group-by`/`order-by` clauses in `Point_Get`](https://github.com/pingcap/tidb/pull/7720)
* [Reuse chunks to reduce memory usage in `UnionScan`](https://github.com/pingcap/tidb/pull/7717)
* [Add correctness check for some system variables](https://github.com/pingcap/tidb/pull/7716)
* [Optimize constant fold for null parameter expressions to simplify the outer join](https://github.com/pingcap/tidb/pull/7696)
* [Enhance predicate pushdown over `join`](https://github.com/pingcap/tidb/pull/7645)
* [Support the `init_vector` argument for the built-in function `AES_ENCRYPT`/`AES_DECRYPT`](https://github.com/pingcap/tidb/pull/7425)

## Fixed

* [Fix a bug in the `Format()` function for some expressions](https://github.com/pingcap/tidb/pull/7770)
* [Fix the session time in `show processlist`](https://github.com/pingcap/tidb/pull/7765)
* [Fix `INFORMATION_SCHEMA.SCHEMATA` to show correct charset and collation](https://github.com/pingcap/tidb/pull/7751)
* [Fix incorrect unquoted functions for JSON escape sequences](https://github.com/pingcap/tidb/pull/7745)
* [Consider the timezone when adding an index in the timestamp column](https://github.com/pingcap/tidb/pull/7724)
* [Fix predicate pushdown for `UnionScan`](https://github.com/pingcap/tidb/pull/7695)
* [Fix mistaken conversion from the outer join to the inner join](https://github.com/pingcap/tidb/pull/7689)
* [Fix a bug caused by the schema of `union`](https://github.com/pingcap/tidb/pull/7680)

# Weekly update in TiKV and PD

Last week, we landed [14 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-09-17..2018-09-23&type=Issues) in the TiKV and PD repositories.

## Added

* [Add the `sha1` built-in function](https://github.com/tikv/tikv/pull/3612)
* [Add unpushed built-in UDFs `Log1Arg` and `Log2Args`](https://github.com/tikv/tikv/pull/3603)

## Improved

* [Refactor `Month` by using new `handle_invalid_time_error`](https://github.com/tikv/tikv/pull/3615)
* [Make `Runable::run` a default method](https://github.com/tikv/tikv/pull/3593)
* [Move Coprocessor to the read pool](https://github.com/tikv/tikv/pull/3515)
* [Adjust the PD project layout](https://github.com/pingcap/pd/pull/1245)
* [Make some parameters configurable in the simulator](https://github.com/pingcap/pd/pull/1248)

## Fixed

* [Fix the `from_hex` bug](https://github.com/tikv/tikv/pull/2873)
* [Fix `micro_secs` of `Duration`](https://github.com/tikv/tikv/pull/3625)
* [Fix the panic of `adjacent-region-scheduler` after PD transfers the leader](https://github.com/pingcap/pd/pull/1250)
* [Fix the `DisableNamespaceRelocation` option clone behavior](https://github.com/pingcap/pd/pull/1251)

# New contributors (Thanks!)

TiDB:

- [FateTHarlaown](https://github.com/FateTHarlaown)
- [Kingwl](https://github.com/Kingwl)
- [chenyanzhe](https://github.com/chenyanzhe)

TiKV:

- [haoxiang47](https://github.com/haoxiang47)
- [koushiro](https://github.com/koushiro)
- [sch00lb0y](https://github.com/sch00lb0y)

docs-cn:

- [oasangqi](https://github.com/oasangqi)