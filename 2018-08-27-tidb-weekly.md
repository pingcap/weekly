---
title: Weekly update (August 20 ~ August 26, 2018)
date: 2018-08-27
summary: Last week, we landed 34 PRs in the TiDB repository, 3 PRs in the TiSpark repository, and 27 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [34 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-08-20..2018-08-26+) in the TiDB repository.

## Added

- [Make the query feedback work for the partitioned table](https://github.com/pingcap/tidb/pull/7394)
- [Support a new aggregate framework for `HashAggExec`](https://github.com/pingcap/tidb/pull/7268)

## Fixed

- [Fix a bug when using a correlated column as the index](https://github.com/pingcap/tidb/pull/7357)
- [Fix the `prepare` result for zero `timestamp`/`time`/`datetime`](https://github.com/pingcap/tidb/pull/7415)
- [Fix the `Enum` type flag bug](https://github.com/pingcap/tidb/pull/7438)
- [Make partition by range value accept the constant expression](https://github.com/pingcap/tidb/pull/7442)
- [Fix `concat` in the `GROUP` statement](https://github.com/pingcap/tidb/pull/7448)
- [Fix selecting null value for table partition](https://github.com/pingcap/tidb/pull/7452)
- [Use the unified `infoschema` in `select ... information_schema.tables`](https://github.com/pingcap/tidb/pull/7459)
- [Fix the `Format` function for the `Mod` opcode](https://github.com/pingcap/tidb/pull/7455)

## Improved

- [Split ranges if the slice is too big](https://github.com/pingcap/tidb/pull/7454)
- [Execute the `admin` command with `Super_priv`](https://github.com/pingcap/tidb/pull/7486)

# Weekly update in TiSpark

Last week, we landed [3 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-08-20..2018-08-26) in the TiSpark repository.

## Added

- [Decode `JSON` to `string`](https://github.com/pingcap/tispark/pull/417)

# Weekly update in TiKV and PD

Last week, we landed [27 PRs](https://github.com/search?p=1&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-08-20..2018-08-26&type=Issues) in the TiKV and PD repositories.

## Added

- Add new built-in functions:
    
    - [`builtin-cos`](https://github.com/tikv/tikv/pull/3410)
    - [`builtin-date`](https://github.com/tikv/tikv/pull/3428)
    - [`builtin-inet6_aton`](https://github.com/tikv/tikv/pull/3480)

- [Support producing multiple split keys in `split-checker`](https://github.com/tikv/tikv/pull/3464)

## Fixed

- [Update `approximate_size` and `approximate_keys` after the Region is merged](https://github.com/tikv/tikv/pull/3497) 

## Improved

- [Make a more efficient workflow for Raft `LocalReader`](https://github.com/tikv/tikv/pull/3443)
- [Remove the `IsolationLevel` and `ScanMode` options from `MvccTxn`](https://github.com/tikv/tikv/pull/3445)
- [Handle the API error properly instead of turning them into gRPC errors](https://github.com/tikv/tikv/pull/3450)
- [Add new forward/backward Scanners to improve the `scan` performance](https://github.com/tikv/tikv/pull/3458)
- [Try `ask_split` when `ask_batch_split` is incompatible](https://github.com/tikv/tikv/pull/3459)
- [Associate a buffer to `AggFuncExpr` to reduce memory allocation](https://github.com/tikv/tikv/pull/3490)

# New contributors (Thanks!)

TiKV:

- [hawkingrei](https://github.com/hawkingrei)
- [niedhui](https://github.com/niedhui)
- [vkorenev](https://github.com/vkorenev)

TiSpark:

- [alex-lx](https://github.com/alex-lx)