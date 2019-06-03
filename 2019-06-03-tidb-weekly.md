---
title: Weekly update (May 27 ~ June 02, 2019)
date: 2019-06-03
summary: Last week, we landed 37 PRs in the TiDB repository, 4 PRs in the TiSpark repository, and 38 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [37 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-05-27..2019-06-02+) in the TiDB repository.

## Added

- [Support the `SQL_BIG_RESULT`, `SQL_SMALL_RESULT`, and `SQL_BUFFER_RESULT` syntax](https://github.com/pingcap/tidb/pull/10658)
- [Add `usability-team` in PR guidelines](https://github.com/pingcap/tidb/pull/10601)

## Improved

- [Check `Deadlock` in `KeyError` of the pessimistic locking operation result returned by TiKV](https://github.com/pingcap/tidb/pull/10624)
- [Remove canceled requests before sending them to TiKV](https://github.com/pingcap/tidb/pull/10634)
- [Implement `IterReverse` and use it to speed up `admin show ddl jobs`](https://github.com/pingcap/tidb/pull/10152)
- [Preload frequently used variables](https://github.com/pingcap/tidb/pull/10463)
- [Improve the UT coverage of the `expression` package to 80%](https://github.com/pingcap/tidb/pull/10641)
- [Improve the UT coverage of the `distsql` package to 85%](https://github.com/pingcap/tidb/pull/10582)
- [Speed up testing by 50% in the `ddl` package](https://github.com/pingcap/tidb/pull/10609)

## Fixed

- [Skip virtual generated column during collecting statistics](https://github.com/pingcap/tidb/pull/10623)
- [Fix a potential goroutine leak in `gcworker`](https://github.com/pingcap/tidb/pull/10622)
- [Fix the `Analyze` worker panic caused by sending messages in the closed channel](https://github.com/pingcap/tidb/pull/10603)
- [Fix the unexpected result of `unsigned_int_col >= -int_cnst` in the planner](https://github.com/pingcap/tidb/pull/10471)
- [Fix a panic when using the `Window` function in some cases](https://github.com/pingcap/tidb/pull/10452)
- [Fix `SHOW VIEW` privileges for `EXPLAIN`](https://github.com/pingcap/tidb/pull/10585)
- [Fix the goroutine leak when TiKV is offline](https://github.com/pingcap/tidb/pull/10616)
- [Fix the issue that `StreamAggExec` does not clean up resources when the `Close` function is called](https://github.com/pingcap/tidb/pull/10615)

# Weekly update in TiSpark

Last week, we landed [4 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-05-27..2019-06-02+) in the TiSpark repository.

## Fixed

- [Fix the issue that the `MatchError` exception might occur when unsigned `BigInt` is used in the `group by` column](https://github.com/pingcap/tispark/pull/780)

# Weekly update in TiKV and PD

Last week, we landed [38 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-05-27..2019-06-02&type=Issues) in the TiKV and PD repositories.

## Added

- Add batch aggregate functions  
  - [`SUM()`](https://github.com/tikv/tikv/pull/4797)
  - [`AVG()`](https://github.com/tikv/tikv/pull/4777)
  - [`FIRST()`](https://github.com/tikv/tikv/pull/4771)
- [Add `BatchStreamAggregationExecutor`](https://github.com/tikv/tikv/pull/4786)
- [Support `resolve_lock_lite`](https://github.com/tikv/tikv/pull/4589)

## Improved

- [Reuse `monotonic-raw-now` for each round in raftstore](https://github.com/tikv/tikv/pull/4798)
- [Improve batch vector performance](https://github.com/tikv/tikv/pull/4796)

## Fixed

- [Fix the issue that the TiKV snapshot might not be synchronized](https://github.com/tikv/tikv/pull/4811)
- [Fix the TiKV read stale issue after role change](https://github.com/tikv/tikv/pull/4810)
- [Fix the issue that the hot Region limit for PD might be 0](https://github.com/pingcap/pd/pull/1552)
- [Fix a TiKV panic when no aggregate function exists in the batch executor](https://github.com/tikv/tikv/pull/4782)
- [Fix `Duration::parse` bugs](https://github.com/tikv/tikv/pull/4497)

# New contributors (Thanks!)

tikv:

- [senden9](https://github.com/senden9)

parser:

- [b41sh](https://github.com/b41sh)
- [db-storage](https://github.com/db-storage)

docs-cn:

- [emhlbmc](https://github.com/emhlbmc)
