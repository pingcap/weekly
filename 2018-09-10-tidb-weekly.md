---
title: Weekly update (September 03 ~ September 09, 2018)
date: 2018-09-10
summary: Last week, we landed 39 PRs in the TiDB repository, 10 PRs in the TiSpark repository, and 50 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [39 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-09-03..2018-09-09+) in the TiDB repository.

## Added

* [Add different labels for restricted SQL and general SQL metrics](https://github.com/pingcap/tidb/pull/7631)
* [Add the `USR1` signal handler to dump goroutine](https://github.com/pingcap/tidb/pull/7587)
* [Use the `point get` plan for the `UPDATE` statement](https://github.com/pingcap/tidb/pull/7586)
* [Support `load data` with `IgnoreLines`](https://github.com/pingcap/tidb/pull/7576)
* [Support the `json_contains` builtin function](https://github.com/pingcap/tidb/pull/7443)

## Improved

* [Make `Analyze` `Buckets` number configurable](https://github.com/pingcap/tidb/pull/7619)
* [Set `HIGH_PRIORITY` for the bootstrap SQL statements](https://github.com/pingcap/tidb/pull/7616)
* [Only check the range typed partition when creating a partitioned table](https://github.com/pingcap/tidb/pull/7599)
* [Make a tiny refactor in the reorganization stage of adding indices](https://github.com/pingcap/tidb/pull/7598)
* [Relax the `tso` backoff limit](https://github.com/pingcap/tidb/pull/7589)
* [Reduce chunk's iterator function call](https://github.com/pingcap/tidb/pull/7585)
* [Improve compatibility for the MariaDB client](https://github.com/pingcap/tidb/pull/7573)
* [Do `AutoAnalyze` on a certain period of a day](https://github.com/pingcap/tidb/pull/7570)
* [Change the logic of converting the logical join to the index join](https://github.com/pingcap/tidb/pull/7553)
* [Read the inner table and build hash table parallel in hash join](https://github.com/pingcap/tidb/pull/7544)
* [Add batch copy to the inner join and the left and right outer join](https://github.com/pingcap/tidb/pull/7493)
* [Add a `ctxPool` field to the `worker` struct to make executing the SQL statement in the `DDL` package possible](https://github.com/pingcap/tidb/pull/7447)

## Fixed

* [Fix some `datetime` related cases which are inconsistent with MySQL](https://github.com/pingcap/tidb/pull/7636)
* [Fix a compatibility problem of analyzing period variables](https://github.com/pingcap/tidb/pull/7633)
* [Fix an error in the parser when parsing a single line comment ended with a newline character](https://github.com/pingcap/tidb/pull/7612)
* [Fix an issue that the `gc_delete_range` table is queried with a wrong form of timestamp](https://github.com/pingcap/tidb/pull/7610)
* [Fix an issue that the bit type can use `null` as its default value](https://github.com/pingcap/tidb/pull/7604)
* [Return the correct column name and column label name](https://github.com/pingcap/tidb/pull/7600)
* [Fix a panic when logging detailed statistics](https://github.com/pingcap/tidb/pull/7588)
* [Fix a wrong `count` output of `explain` for the `TableScan` plan](https://github.com/pingcap/tidb/pull/7583)
* [Fix the `update join` result when the join table order is changed](https://github.com/pingcap/tidb/pull/7571)
* [Fix the issue that creating a partitioned table with `bigint` columns fails](https://github.com/pingcap/tidb/pull/7520)

# Weekly update in TiSpark

Last week, we released a new version [1.1](https://github.com/pingcap/tispark/releases/tag/1.1) and landed [10 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-09-03..2018-09-09+) in the TiSpark repository.

## Fixed

- [Remove the experimental split function and related parameters](https://github.com/pingcap/tispark/pull/440)
- [Fix the `SharedState` behavior in `ThriftServer`](https://github.com/pingcap/tispark/pull/437)
- [Fix the issue that `start-tithriftserver.sh` loses extra options](https://github.com/pingcap/tispark/pull/436)

# Weekly update in TiKV and PD

Last week, we landed [50 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-09-03..2018-09-09&type=Issues) in the TiKV and PD repositories.

## Added

- Add new built-in functions:
    
    - [`builtin-Greatest*/Least*`](https://github.com/tikv/tikv/pull/3113)
    - [`builtin-BitCount`](https://github.com/tikv/tikv/pull/3394)
    - [`builtin-LTrim/RTrim`](https://github.com/tikv/tikv/pull/3400)
    - [`builtin-math.Sin`](https://github.com/tikv/tikv/pull/3406)
    - [`builtin-Rand/RandWithSeed`](https://github.com/tikv/tikv/pull/3415)
    - [`builtin-Reverse/ReverseBinary)`](https://github.com/tikv/tikv/pull/3435)
    - [`builtin-CharLength`](https://github.com/tikv/tikv/pull/3461)
    - [`builtin-HexIntArg/HexStrArg`](https://github.com/tikv/tikv/pull/3478)
    - [`builtin-Asin/Acos)`](https://github.com/tikv/tikv/pull/3482)
    - [`builtin-Inet6Ntoa`](https://github.com/tikv/tikv/pull/3519)
    - [`builtin-MD5`](https://github.com/tikv/tikv/pull/3554)
    - [`builtin-Cot/Degrees`](https://github.com/tikv/tikv/pull/3543)
    - [`builtin-Elt`](https://github.com/tikv/tikv/pull/3555)
    - [`builtin-LastDay`](https://github.com/tikv/tikv/pull/3556)
    - [`builtin-Month`](https://github.com/tikv/tikv/pull/3569)

## Fixed

- [Always update read delegate's Regions to avoid stale Region information in `LocalReader`](https://github.com/tikv/tikv/pull/3565)
- [Remove read delegate on conf change `RemoveNode`](https://github.com/tikv/tikv/pull/3561)
- [Do not drop `MsgRequestPreVote` messages from newly split Regions](https://github.com/tikv/tikv/pull/3557) 

## Improved

- [Reduce key clone in GC](https://github.com/tikv/tikv/pull/3558)
- [Limit the garbage cleanup speed to avoid blocking snapshot application](https://github.com/tikv/tikv/pull/3547)
- [Remove extra Region clone when handling Region heartbeats](https://github.com/pingcap/pd/pull/1195)
- [Clean up residual Region clone](https://github.com/pingcap/pd/pull/1236)
- [Start schedulers based on the proportion of Regions](https://github.com/pingcap/pd/pull/1225)

# New contributors (Thanks!)

TiKV:

- [WPH95](https://github.com/WPH95)
- [chux0519](https://github.com/chux0519)
- [intellild](https://github.com/intellild)
- [liufuyang](https://github.com/liufuyang)
- [malc0lm](https://github.com/malc0lm)
- [mtunique](https://github.com/mtunique)

TiDB:

- [llvim](https://github.com/llvim)
- [xiangyuf](https://github.com/xiangyuf)