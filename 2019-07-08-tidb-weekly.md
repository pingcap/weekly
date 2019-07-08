---
title: Weekly update (July 01 ~ July 07, 2019)
date: 2019-07-08
summary: Last week, we landed 69 PRs in the TiDB repository, 18 PRs in the TiSpark repository, and 34 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [69 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-07-01..2019-07-07+) in the TiDB repository.

## Added

- [Make `TxnEntryCountLimit` and `TxnTotalSizeLimit` configurable](https://github.com/pingcap/tidb/pull/11058)
- [Add `delay-clean-table-lock` when the session is closed](https://github.com/pingcap/tidb/pull/11038)
- [Add the `affinity-cpus` starting argument](https://github.com/pingcap/tidb/pull/10773)
- [Allow more charset/collation modifications for the database/table](https://github.com/pingcap/tidb/pull/10958)

## Improved

- [Disallow modifying the generated expression of a stored or an indexed column](https://github.com/pingcap/tidb/pull/10932)
- [Remove the maximum gRPC message limitation for key-value requests](https://github.com/pingcap/tidb/pull/11005)
- [Add a recover in the `runDDLJob` function](https://github.com/pingcap/tidb/pull/10981)

## Fixed

- [Fix a logical error about `update ignore` introduced in the previous refactoring process](https://github.com/pingcap/tidb/pull/11060)
- [Fix the issue that the decimal fraction is missed for the default `CURRENT_TIMESTAMP`](https://github.com/pingcap/tidb/pull/11070)
- [Fix the invalid key error of fast `Analyze`](https://github.com/pingcap/tidb/pull/11072)
- [Make a deep copy of the string when assigning it to a user variable](https://github.com/pingcap/tidb/pull/11041)
- [Handle the unsigned primary key for fast `Analyze`](https://github.com/pingcap/tidb/pull/11074)
- [Fix the `PointGet` snapshot TS for pessimistic transactions](https://github.com/pingcap/tidb/pull/11012)
- [Fix a bug of canceling an OOM action](https://github.com/pingcap/tidb/pull/10993)
- [Fix a bug that double closes channels](https://github.com/pingcap/tidb/pull/10991)
- [Fix a corner case in the column pruning rule](https://github.com/pingcap/tidb/pull/10974)
- [Fix a bug of modifying a column from null to not null](https://github.com/pingcap/tidb/pull/10948)
- [Make the `sleep` function respond to the `KILL` statement](https://github.com/pingcap/tidb/pull/10959)

# Weekly update in TiSpark

Last week, we landed [18 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-07-01..2019-07-07+) in the TiSpark repository and released TiSpark [2.1.1](https://github.com/pingcap/tispark/releases/tag/v2.1.1) and [1.2.1](https://github.com/pingcap/tispark/releases/tag/v1.2.1).

## Added

- [Support Region split for tables](https://github.com/pingcap/tispark/pull/881)
- [Add support for delaying cleaning the table lock](https://github.com/pingcap/tispark/pull/905)

## Fixed

- [Fix the count error when `advanceNextResponse` is empty](https://github.com/pingcap/tispark/pull/878)
- [Fill zero for an encoding binary type](https://github.com/pingcap/tispark/pull/888)

# Weekly update in TiKV and PD

Last week, we landed [34 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-07-01..2019-07-07&type=Issues) in the TiKV and PD repositories.

## Improved

- [Set `blob_run_mode=ReadOnly` for non-default CFs](https://github.com/tikv/tikv/pull/4991)
- [Ignore the `not found` error when rotating log files](https://github.com/tikv/tikv/pull/4971)
- [Reduce the size of `Duration` to 8 bytes](https://github.com/tikv/tikv/pull/4858)
- [Handle `BatchCommandsEmptyRequest`](https://github.com/tikv/tikv/pull/5001)
- [Keep the comment consistent with the code](https://github.com/pingcap/pd/pull/1615)
- [Optimize memtable `desc` scan](https://github.com/tikv/tikv/pull/5015)
- [Log all divergent routines when filtering the target store](https://github.com/pingcap/pd/pull/1614)
- [Tune the default limit for hot Region scheduling](https://github.com/pingcap/pd/pull/1616)
- [Remove the limit on the size of received messages](https://github.com/tikv/tikv/pull/4992)
- [Set influence according to the Region size](https://github.com/pingcap/pd/pull/1613)
- [Check the maximum number of open files required for Titan](https://github.com/tikv/tikv/pull/5026)
- [Refine `convert_*_to_int` functions](https://github.com/tikv/tikv/pull/4962)

## Added

- [Add the `titan-key-only` option](https://github.com/tikv/tikv/pull/4966)
- [Support the variable number of arguments](https://github.com/tikv/tikv/pull/5007)
- [Adds the `/config` endpoint to the status server that returns the TiKV configuration](https://github.com/tikv/tikv/pull/4997)
- [Support the request snapshot on the leader's side](https://github.com/tikv/tikv/pull/4926)
- [Add the `abs` RPN function](https://github.com/tikv/tikv/pull/4982)
- [Add the `IN()` RPN function](https://github.com/tikv/tikv/pull/5016)
- [Support `CASE_WHEN`](https://github.com/tikv/tikv/pull/5020)

## Fixed

- [Check the replica for hot Regions](https://github.com/pingcap/pd/pull/1609)
- [Fix duplicated plus assign](https://github.com/tikv/tikv/pull/5038)

# New contributors (Thanks!)

tidb:

- [tcmichael](https://github.com/tcmichael)

tikv:

- [jlerche](https://github.com/jlerche)
- [mapleFU](https://github.com/mapleFU)

tidb-operator:

- [shinnosuke-okada](https://github.com/shinnosuke-okada)
- [thecodeassassin](https://github.com/thecodeassassin)
