---
title: Weekly update (May 06 ~ May 12, 2019)
date: 2019-05-13
summary: Last week, we landed 48 PRs in the TiDB repository, 8 PRs in the TiSpark repository, and 45 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [48 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-05-06..2019-05-12+) in the TiDB repository.

## Added

- [Make incremental `Analyze` support feedback](https://github.com/pingcap/tidb/pull/10355)
- [Support pessimistic transactions (experimental feature)](https://github.com/pingcap/tidb/pull/10297)
- [Support dumping history statistics](https://github.com/pingcap/tidb/pull/10291)
- [Support `SET ROLE` statements](https://github.com/pingcap/tidb/pull/10268)

## Improved

- [Handle virtual columns when fetching duplicate rows in `batchChecker`](https://github.com/pingcap/tidb/pull/10370)
- [Split unit tests to shorten execution time](https://github.com/pingcap/tidb/pull/10364)
- [Make `Desc` and `show columns` statements compatible with MySQL](https://github.com/pingcap/tidb/pull/10358)
- [Reduce duplicate `DigestHash` calls](https://github.com/pingcap/tidb/pull/10352)
- [Add a variable to control the back off time and disable transaction automatic retry by default](https://github.com/pingcap/tidb/pull/10266)
- [Add the `SplitIndexRegion` syntax](https://github.com/pingcap/tidb/pull/10203)
- [Enable hash partition and range column partition by default](https://github.com/pingcap/tidb/pull/9936)

## Fixed

- [Fix wrong column calculation in `ColumnPruning` for `LogicalUnionAll`](https://github.com/pingcap/tidb/pull/10384)
- [Fix the issue that `period_add` is not compatible with MySQL](https://github.com/pingcap/tidb/pull/10380)
- [Fix the issue that the result of `cast(-1 as datetime)` is not compatible with MySQL](https://github.com/pingcap/tidb/pull/10368)
- [Fix the wrong behavior of `PushDownNot` in some cases](https://github.com/pingcap/tidb/pull/10363)
- [Fix the issue that addition between `datetime` and the real `interval` is not compatible with MySQL](https://github.com/pingcap/tidb/pull/10347)
- [Fix the issue that addition between `datetime` and `interval` is not compatible with MySQL](https://github.com/pingcap/tidb/pull/10329)
- [Fix `token too long` errors when parsing slow query logs](https://github.com/pingcap/tidb/pull/10328)
- [Fix the issue of updating the self-schema version and update logs](https://github.com/pingcap/tidb/pull/10324)
- [Fix wrong `DATE/DATETIME` comparison in the `BETWEEN` function](https://github.com/pingcap/tidb/pull/10313)
- [Fix the panic in the `regions/meta` API](https://github.com/pingcap/tidb/pull/10222)

# Weekly update in TiSpark

Last week, we landed [8 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-05-06..2019-05-12+) in the TiSpark repository.

## Fixed

- [Fix the index pushdown issue](https://github.com/pingcap/tispark/pull/697)
- [Fix the `Table not exist` exception in testing](https://github.com/pingcap/tispark/pull/710)

# Weekly update in TiKV and PD

Last week, we landed [45 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-05-06..2019-05-12&type=Issues) in the TiKV and PD repositories.

## Added

* [Introduce `tipb_helper`](https://github.com/tikv/tikv/pull/4634)
* [Add the tick registry for `raftstore`](https://github.com/tikv/tikv/pull/4632)
* [Add `*AnyValue` functions](https://github.com/tikv/tikv/pull/4629)
* [Add `cop_codegen` to the `tikv_alloc` whitelist](https://github.com/tikv/tikv/pull/4626)
* [Add `RPN` comparison functions for `Int`, `Decimal`, `String`, `Time`, `Duration` and `Json`](https://github.com/tikv/tikv/pull/4625)
* [Support CPU profiling sections of code](https://github.com/tikv/tikv/pull/3971)
* [Support the `exec` summary for the `Limit` executor](https://github.com/tikv/tikv/pull/4599)

## Improved

* [Make some small improvements for `codec`](https://github.com/tikv/tikv/pull/4664)
* [Make tiny refactor for `peer_storage` in `raftstore`](https://github.com/tikv/tikv/pull/4668)
* [Skip deleting range check on raft `cf`](https://github.com/tikv/tikv/pull/4663)
* [Use `raw_key` in `Error` and reduce copies](https://github.com/tikv/tikv/pull/4631)
* [Simplify some code using field type conversion](https://github.com/tikv/tikv/pull/4649)
* [Make hot Region balance not affected by `balance-region-scheduler-limit`](https://github.com/pingcap/pd/pull/1522)

## Fixed

* [Fix the issue that metrics might be counted multiple times](https://github.com/tikv/tikv/pull/4654)
* [Fix `tick_after_destroy` in testing](https://github.com/tikv/tikv/pull/4647)
* [Fix the issue that the first `safe_point` sent to PD does not trigger GC](https://github.com/tikv/tikv/pull/4641)

# New contributor (Thanks!)

tikv: [H-ZeX](https://github.com/H-ZeX)