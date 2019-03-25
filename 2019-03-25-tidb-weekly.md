---
title: Weekly update (March 18 ~ March 24, 2019)
date: 2019-03-25
summary: Last week, we landed 50 PRs in the TiDB repository, 4 PRs in the TiSpark repository, and 26 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [50 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-03-18..2019-03-24) in the TiDB repository.

## Added

- [Add the `/debug/zip` API to get useful debugging information at once](https://github.com/pingcap/tidb/pull/9651)
- [Support `SET ROLE` and `CURRENT_ROLE`](https://github.com/pingcap/tidb/pull/9581)

## Improved

- [Replace `map` in `GetFormatType` with `switch-case` to speed up execution](https://github.com/pingcap/tidb/pull/9851)
- [Change the type of `RoundMode` from string to `int32` to speed up execution](https://github.com/pingcap/tidb/pull/9809)
- [Support `Change` and `ChangeExec`](https://github.com/pingcap/tidb/pull/9789)
- [Improve row count estimation for the index range containing correlated columns](https://github.com/pingcap/tidb/pull/9738)
- [Unify the log format for the `util` package](https://github.com/pingcap/tidb/pull/9668)
- [Unify the log format for the `store` package](https://github.com/pingcap/tidb/pull/9664)
- [Unify the log format for the `ddl` package](https://github.com/pingcap/tidb/pull/9659)
- [Remove the wait time after canceling a job](https://github.com/pingcap/tidb/pull/9648)
- [Support chunk size control for Joiners and Join-executors](https://github.com/pingcap/tidb/pull/9614)
- [Unify the log format for the `statistics` package](https://github.com/pingcap/tidb/pull/9534)
- [Add more checks for `create table partition by range column`](https://github.com/pingcap/tidb/pull/9527)
- [Unify the log format for the `session` package](https://github.com/pingcap/tidb/pull/9517)
- [Unify the log format for the `table` package](https://github.com/pingcap/tidb/pull/9514)
- [Disable non-deterministic function calls for generated columns](https://github.com/pingcap/tidb/pull/9239)

## Fixed

- [Fix the panic in `SELECT * FROM information_schema.processlist`](https://github.com/pingcap/tidb/pull/9842)
- [Fix an unexpected overflow error when adding a big signed integer and a big unsigned integer](https://github.com/pingcap/tidb/pull/9840)
- [Fix the privilege check failure for `GRANT ON TABLE`](https://github.com/pingcap/tidb/pull/9828)
- [Fix the issue that `str_to_date` is not compatible with MySQL in some cases](https://github.com/pingcap/tidb/pull/9819)
- [Fix a panic in the window function when order-by items contain `NULL`](https://github.com/pingcap/tidb/pull/9800)
- [Fix a wrong format of the slow log](https://github.com/pingcap/tidb/pull/9759)
- [Fix the issue that `Select+1000` is not compatible with MySQL](https://github.com/pingcap/tidb/issues/9683)

# Weekly update in TiSpark

Last week, we landed [4 PRs](https://github.com/pingcap/tispark/pulls?utf8=✓&q=is%3Apr+is%3Amerged+merged%3A2019-03-18..2019-03-24+) in the TiSpark repository.

## Fixed

- [Update the `kvproto` version that breaks compilation](https://github.com/pingcap/tispark/pull/604)

# Weekly update in TiKV and PD

Last week, we landed [26 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-03-18..2019-03-25&type=Issues) in the TiKV and PD repositories.

## Added

* [Implement the `instr` coprocessor built-in function](https://github.com/tikv/tikv/pull/4337)

## Improved

* [Use single quotes in coprocessor error messages](https://github.com/tikv/tikv/pull/4413)
* [Improve `instr_binary`, `locate`, and `locate_binary` coprocessor built-in functions](https://github.com/tikv/tikv/pull/4378)
* [Support `batch` for the table scan executor](https://github.com/tikv/tikv/pull/4351)

## Fixed

* [Fix the issue of the PD scheduler removing the Region leader](https://github.com/pingcap/pd/pull/1470)
* [Return warnings when casting a float string to an integer string](https://github.com/tikv/tikv/pull/4336)

## Engineering

* [Use lite-runtime in `Protobuf`](https://github.com/tikv/tikv/pull/4425)
* [Abstract some new `jemalloc` code](https://github.com/tikv/tikv/pull/4411)
* [Fix a compiling warning](https://github.com/tikv/tikv/pull/4408)
* [Check SSE4.2 in the release build](https://github.com/tikv/tikv/pull/4399)
* [Use static metrics in the TiKV raw read](https://github.com/tikv/tikv/pull/4383)
* [Refactor `TableScanExecutor` and `IndexScanExecutor`](https://github.com/tikv/tikv/pull/4089)

# New contributors (Thanks!)

tikv:

- [Xuanwo](https://github.com/Xuanwo)

tidb:

- [b41sh](https://github.com/b41sh)

pd:

- [elitecodegroovy](https://github.com/elitecodegroovy)

parser:

- [aliiohs](https://github.com/aliiohs)
- [hawkingrei](https://github.com/hawkingrei)
- [loxp](https://github.com/loxp)
- [wjhuang2016](https://github.com/wjhuang2016)