---
title: Weekly update (December 03 ~ December 09, 2018)
date: 2018-12-10
summary: Last week, we landed 48 PRs in the TiDB repository, 4 PRs in the TiSpark repository, and 22 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [48 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-12-03..2018-12-09+) in the TiDB repository.

## Added

- [Add the HTTP API to query the DDL history](https://github.com/pingcap/tidb/pull/8591)
- [Add two metrics gauges to show CPU and memory usage](https://github.com/pingcap/tidb/pull/8580)
- [Propose the design to restore the SQL text from the AST tree](https://github.com/pingcap/tidb/pull/8533)
- [Add the implementation phase framework of the `cascades` planner](https://github.com/pingcap/tidb/pull/8449)
- [Add the `ddl_reorg_batch_size` variable to control the batch size of the DDL worker](https://github.com/pingcap/tidb/pull/8365)
- [Add the `gc_enable` variable to enable or disable GC](https://github.com/pingcap/tidb/pull/8282)
- [Add the transform phase framework of the `cascades` planner](https://github.com/pingcap/tidb/pull/7869)

## Improved

- [Speed up execution of unit tests for the `statistics` package](https://github.com/pingcap/tidb/pull/8597)
- [Disable the global variable cache when running unit tests](https://github.com/pingcap/tidb/pull/8594)
- [Do the DDL check for `Create Index` before putting it to the job queue](https://github.com/pingcap/tidb/pull/8592)
- [Speed up execution of unit tests for the `tikv` package](https://github.com/pingcap/tidb/pull/8562)
- [Improve compatibility when casting string as datetime](https://github.com/pingcap/tidb/pull/8516)
- [Support `Show Create Table` for hash partitioned tables](https://github.com/pingcap/tidb/pull/8477)
- [Support `batchInsert` of values for the `Insert` statement](https://github.com/pingcap/tidb/pull/8420)
- [Improve the current greedy join reorder algorithm to leverage cost estimation](https://github.com/pingcap/tidb/pull/8394)
- [Support `Select`/`Insert` for hash partitioned tables](https://github.com/pingcap/tidb/pull/8411)
- [Support `Truncate` for hash partitioned tables](https://github.com/pingcap/tidb/pull/8401)
- [Support `Alter Table Add Partition` for hash partitioned tables](https://github.com/pingcap/tidb/pull/8375)
- [Support `?` in `Order By`/`Group By`/`Limit Offset` clauses](https://github.com/pingcap/tidb/pull/8206)

## Fixed

- [Set correct concurrency for `Projection` below `Aggregation`](https://github.com/pingcap/tidb/pull/8601)
- [Handle corrupted length parameters for the `uncompress` built-in function](https://github.com/pingcap/tidb/pull/8586)
- [Fix failure of `Grant` in the `ANSI_QUOTES` SQL mode](https://github.com/pingcap/tidb/pull/8561)
- [Fix incorrect date arithmetics with the negative interval parameter](https://github.com/pingcap/tidb/pull/8523)
- [Fix the bug of cancelling `Drop Index`](https://github.com/pingcap/tidb/pull/8504)

# Weekly update in TiSpark

Last week, we landed [4 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-12-03..2018-12-09+) in the TiSpark repository.

## Fixed

- [Fix the unresolved column name when using `table.column`](https://github.com/pingcap/tispark/pull/512)
- [Fix the `LockResolverTest` error when sending requests using `callWithRetry`](https://github.com/pingcap/tispark/pull/518)

# Weekly update in TiKV and PD

Last week, we landed [22 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-12-03..2018-12-09&type=Issues) in the TiKV and PD repositories.

## Added

- [Add `StoreNotMatch` details](https://github.com/tikv/tikv/pull/3885)
- [Add the `strcmp` built-in function](https://github.com/tikv/tikv/pull/3879)
- [Add the `week_day` and the `week_of_year` built-in functions](https://github.com/tikv/tikv/pull/3871)
- [Add the `compress`, `uncompress` and `uncompressed_length` built-in functions](https://github.com/tikv/tikv/pull/3856)
- [Add the `end_key` support for `raw_scan`](https://github.com/tikv/tikv/pull/3847)
- [Add the `concat_ws` built-in function](https://github.com/tikv/tikv/pull/3818)

## Improved

- [Replace `FxHashMap` with `Hashbrown`](https://github.com/tikv/tikv/pull/3884)
- [Make `DeleteRange` safe again](https://github.com/tikv/tikv/pull/3883)

## Fixed

- [Reject transferring the leader to the recently added peers](https://github.com/tikv/tikv/pull/3878)
- [Change the merge match peers strategy](https://github.com/pingcap/pd/pull/1339)

# New contributors (Thanks!)

tidb:

- [lonnng](https://github.com/lonng)
- [ziyi-yan](https://github.com/ziyi-yan)

tikv:

- [kg88](https://github.com/kg88)
- [AbnerZheng](https://github.com/AbnerZheng)

docs-cn:

- [beckxie](https://github.com/beckxie)