---
title: Weekly update (June 03 ~ June 09, 2019)
date: 2019-06-10
summary: Last week, we landed 70 PRs in the TiDB repository, 17 PRs in the TiSpark repository, and 28 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [70 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-06-03..2019-06-09+) in the TiDB repository.

## Added

- [Add a configuration item for the bind info lease](https://github.com/pingcap/tidb/pull/10725)
- [Support the `:=` MySQL extension syntax in variable assignment](https://github.com/pingcap/tidb/pull/10700)
- [Add the host column in the `slow_query` table](https://github.com/pingcap/tidb/pull/10693)
- [Support the deadlock detector in `mocktikv` for pessimistic transactions](https://github.com/pingcap/tidb/pull/10669)
- [Support single statement rollback for pessimistic transactions](https://github.com/pingcap/tidb/pull/10654)
- [Support `SplitIndexRegion` with lower and upper values](https://github.com/pingcap/tidb/pull/10409)
- [Add a configuration item to specify GC concurrency manually](https://github.com/pingcap/tidb/pull/10561)

## Improved

- [Print an expensive log when a query exceeds the time threshold](https://github.com/pingcap/tidb/pull/10350)
- [Use the maximum correlation in heuristic row count estimation](https://github.com/pingcap/tidb/pull/10537)
- [Optimize `addSpecialComment` by reusing compiled regular expressions](https://github.com/pingcap/tidb/pull/10502)

## Fixed

- [Commit the current transaction automatically before executing some statements](https://github.com/pingcap/tidb/pull/10707)
- [Fix the wrong output of `show create table` for partitioned tables](https://github.com/pingcap/tidb/pull/10682)
- [Fix an issue for RBAC methods when enabling `--skip-grant-table`](https://github.com/pingcap/tidb/pull/10681)
- [Fix fast `Analyze` bugs during the `Analyze` process](https://github.com/pingcap/tidb/pull/10680)
- [Fix a shallow copy problem about `slow_query`](https://github.com/pingcap/tidb/pull/10696)
- [Fix a panic for `CreateView` using `Prepare`](https://github.com/pingcap/tidb/pull/10651)
- [Fix the issue that duplicate values might occur when the `uuid` function is executed simultaneously on multiple nodes](https://github.com/pingcap/tidb/pull/10590)
- [Check whether the JSON value is valid before `UnmarshalJSON`](https://github.com/pingcap/tidb/pull/10510)
- [Fix the bug that a blob column is changed to a text column when altering the table charset](https://github.com/pingcap/tidb/pull/10477)
- [Fix an issue when the constant overflows the range of the primary key type](https://github.com/pingcap/tidb/pull/10676)
- [Fix an issue when the predicate is PKIsHandle = `1.1`](https://github.com/pingcap/tidb/pull/10716)

# Weekly update in TiSpark

Last week, we landed [17 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-06-03..2019-06-09+) in the TiSpark repository.

## Fixed

- [Fix the `IndexOutOfBoundException` issue when trying to get the PD member](https://github.com/pingcap/tispark/pull/788)
- [Fix the issue that the `key not in range` exception is thrown](https://github.com/pingcap/tispark/pull/795)

## Added

- [Support the auto increment attribute for batch writes](https://github.com/pingcap/tispark/pull/793)

# Weekly update in TiKV and PD

Last week, we landed [28 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-06-03..2019-06-09&type=Issues) in the TiKV and PD repositories.

## Added

- Add batch aggregate functions  
  - [`MultiplyDecimal`](https://github.com/tikv/tikv/pull/4849)
  - [`MAX()`](https://github.com/tikv/tikv/pull/4837)
  - [`MIN()`](https://github.com/tikv/tikv/pull/4837)
  - [`BitAnd()`](https://github.com/tikv/tikv/pull/4824)
  - [`BitOr()`](https://github.com/tikv/tikv/pull/4824)
  - [`BitXor()`](https://github.com/tikv/tikv/pull/4824)
  - [`UnaryNot`](https://github.com/tikv/tikv/pull/4808)
- [Add the batch Top-N executor](https://github.com/tikv/tikv/pull/4825)
- [Add the initialized flag in the cluster status](https://github.com/pingcap/pd/pull/1555)
- [Add the HTTP endpoint to enable the `Jemalloc` profile](https://github.com/tikv/tikv/pull/4600)

## Improved

- [Upgrade `sys-info`](https://github.com/tikv/tikv/pull/4760)

## Fixed

- [Fix the issue that the TiKV snapshot might not be replicated](https://github.com/tikv/tikv/pull/4850)

# New contributors (Thanks!)

tidb:

- [suzaku](https://github.com/suzaku)
- [tangenta](https://github.com/tangenta)

tikv:

- [YKG](https://github.com/YKG)
- [YangKeao](https://github.com/YangKeao)
- [benpigchu](https://github.com/benpigchu)
- [chenyukang](https://github.com/chenyukang)
- [hhhowyou](https://github.com/hhhowyou)

parser:

- [tangenta](https://github.com/tangenta)