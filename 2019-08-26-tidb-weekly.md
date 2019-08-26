---
title: Weekly update (August 19 ~ August 25, 2019)
date: 2019-08-26
summary: Last week, we landed 59 PRs in the TiDB repository, 14 PRs in the TiSpark repository, and 38 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [59 PRs](https://github.com/pingcap/tidb/pulls?utf8=✓&q=is%3Apr+is%3Amerged+merged%3A2019-08-19..2019-08-25+) in the TiDB repository.

## Added

- [Introduce vectorized evaluation methods for each hybrid type](https://github.com/pingcap/tidb/pull/11815)
- [Make `Column` support hybrid types in the vectorized evaluation](https://github.com/pingcap/tidb/pull/11803)
- [Support the syntax of query block](https://github.com/pingcap/tidb/pull/11761)

## Improved

- [Support `IndexJoin` over `UnionScan` for release-2.1](https://github.com/pingcap/tidb/pull/11843)
- [Record `startTime` of a query to the `Session` variables](https://github.com/pingcap/tidb/pull/11822)
- [Record the index name in the slow log instead of in the index ID](https://github.com/pingcap/tidb/pull/11795)
- [Fix the wasted sleep and return an error in the last backoff](https://github.com/pingcap/tidb/pull/11788)
- [Use `BatchPointGet` to improve the execution performance of the `SELECT ... WHERE IN` statement](https://github.com/pingcap/tidb/pull/11750)
- [Split a separate Region for an index when splitting the table Region](https://github.com/pingcap/tidb/pull/11721)

## Fixed

- [Fix `DIV` with the decimal type](https://github.com/pingcap/tidb/pull/11804)
- [Fix the error check in `EvalSubquery`](https://github.com/pingcap/tidb/pull/11802)
- [Fix the `for update` condition for the `PointGet` query](https://github.com/pingcap/tidb/pull/11771)
- [Fix the panic when executing SQL statements to change the Pump state](https://github.com/pingcap/tidb/pull/11730)
- [Fix `TxnSize` to be the number of involved keys in the Region](https://github.com/pingcap/tidb/pull/11725)
- [Fix the failure of privilege check for `CREATE USER` and `DROP USER`](https://github.com/pingcap/tidb/pull/11589)
- [Fix the failure of privilege check for `SET DEFAULT ROLE`](https://github.com/pingcap/tidb/pull/11201)
- [Fix the wrong results of `Not`/`IsTrue`/`IsFalse` functions](https://github.com/pingcap/tidb/pull/10498)

# Weekly update in TiSpark

Last week, we landed [14 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-08-19..2019-08-25+) in the TiSpark repository.

## Fixed

- [Fix the bug that tables are not found in the TiSession because of the synchronization](https://github.com/pingcap/tispark/pull/1041)
- [Disable the pushdown aggregate with an alias to fix the bug that `DISTINCT` is failed without an alias](https://github.com/pingcap/tispark/pull/1054)
- [Fix the incorrect usage of `removeIf` when using `UnmodifiableIterator`](https://github.com/pingcap/tispark/pull/1057)

# Weekly update in TiKV and PD

Last week, we landed [38 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-08-19..2019-08-25&type=Issues) in the TiKV and PD repositories.

## Added

- [Support `EndKey` in the PD `ScanRegions` request](https://github.com/pingcap/pd/pull/1700)
- [Add the `config-check` flag to `pd-server`](https://github.com/pingcap/pd/pull/1695)
- [Add `config-check` flag to `tikv-server`](https://github.com/tikv/tikv/pull/5298)
- [Assign high priority to the PD administration operators](https://github.com/pingcap/pd/pull/1687)
- [Use `LeaderLease` to determine the validity of PD TSO service](https://github.com/pingcap/pd/pull/1676)
- [Implement `ConvertTo<Json>/CAST` as `Duration` for evaluable types in the Coprocessor](https://github.com/tikv/tikv/pull/5199)

## Improved

- [Improve the performance when collecting scanning details](https://github.com/tikv/tikv/pull/5308)
- [Improve the performance of `decode_decimal` in the Coprocessor](https://github.com/tikv/tikv/pull/5259)
- [Improve the performance of detecting deadlocks in a transaction](https://github.com/tikv/tikv/pull/5028)

## Fixed

- [Fix the command help message for tikv-ctl](https://github.com/tikv/tikv/pull/5294)

# New contributors (Thanks!)

tidb:

- [ZYunH](https://github.com/ZYunH)
- [jiyfhust](https://github.com/jiyfhust)
- [EmilStenstrom](https://github.com/EmilStenstrom)
- [zhiqiangxu](https://github.com/zhiqiangxu)

tikv:

- [928234269](https://github.com/928234269)

docs-cn:

- [sydnever](https://github.com/sydnever)

parser:

- [ichn-hu](https://github.com/ichn-hu)
- [doggeral](https://github.com/doggeral)
