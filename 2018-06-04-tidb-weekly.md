---
title: Weekly update (May 28 ~ June 03, 2018)
date: 2018-06-04
summary: Last week, we landed 50 PRs in the TiDB repositories, 2 PRs in the TiSpark repositories, and 20 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [50 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-05-28..2018-06-03) in the TiDB repositories.

## Added

- [Support the `Trace` syntax](https://github.com/pingcap/tidb/pull/6644)
- [Support the `TIDB_IS_DDL_OWNER` builtin function ](https://github.com/pingcap/tidb/pull/6682)
- [Support `ALL` for builtin aggregate function `BIT_AND`/`BIT_OR`/`BIT_XOR`](https://github.com/pingcap/tidb/pull/6685)

## Fixed

- [Check the correctness of decimal's exponent part](https://github.com/pingcap/tidb/pull/6631)
- [Fix the affected row count for the `UPDATE` statement](https://github.com/pingcap/tidb/pull/6656)
- [Fix the range construction for the `IN` builtin function](https://github.com/pingcap/tidb/pull/6667)
- [Fix the empty result of the `JOIN` statement](https://github.com/pingcap/tidb/pull/6669)
- [Fix row count estimation for the `LIMIT` operator](https://github.com/pingcap/tidb/pull/6679)
- [Fix the error message of the `DIV` builtin function](https://github.com/pingcap/tidb/pull/6683)
- [Check the schema name of the column for the `CREATE TABLE` statement](https://github.com/pingcap/tidb/pull/6708)
- [Fix the side effect of casting one decimal to another decimal](https://github.com/pingcap/tidb/pull/6723)

## Improved

- [Push `ABS` to TiKV](https://github.com/pingcap/tidb/pull/6571)
- [Wait for a while when some errors occurred to avoid retrying the DDL job too many times](https://github.com/pingcap/tidb/pull/6601)
- [Unify the log format of the connection ID](https://github.com/pingcap/tidb/pull/6670)
- [Ignore foreign keys in the `SHOW CREATE TABLE` statement](https://github.com/pingcap/tidb/pull/6693)
- [Change statistics delta update duration to 1 minute](https://github.com/pingcap/tidb/pull/6700)
- [Check invalid tasks after physical optimization](https://github.com/pingcap/tidb/pull/6702)
- [Unify the DDL logs](https://github.com/pingcap/tidb/pull/6719)

# Weekly update in TiSpark

Last week, we landed [2 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-05-28..2018-06-03) in the TiSpark repositories.

## Fixed

- [Fix the `ScanIterator` logic where the index may be out of bound](https://github.com/pingcap/tispark/pull/357)

## Improved

- [Update gRPC version to 1.12.0](https://github.com/pingcap/tispark/pull/359)

# Weekly update in TiKV and PD

Last week, we landed [20 PRs](https://github.com/search?p=1&q=repo:pingcap/tikv+repo:pingcap/pd+is:pr+is:merged+merged:2018-05-28..2018-06-03&type=Issues&utf8=%E2%9C%93) in the TiKV and PD repositories.

## Added

- [Encode and decode for arrow chunk](https://github.com/pingcap/tikv/pull/3001)

## Fixed

- [Report an error instead of getting a result if the divisor/dividend is 0 in `do_div_mod`](https://github.com/pingcap/tikv/pull/3099)
- [Fix the bug that the Learner flag mistakenly reports to PD](https://github.com/pingcap/tikv/pull/3112)

## Improved

- [Remove `NumberDecoder` trait from `codec`](https://github.com/pingcap/tikv/pull/3108)
- [Use the average Region size to check if stores need balance](https://github.com/pingcap/pd/pull/1085)
- [Check the Region epoch before adding operators](https://github.com/pingcap/pd/pull/1095)

# New contributors (Thanks!)

TiDB：

- [谷月轩](https://github.com/SilverRainZ)
- [bb7133](https://github.com/bb7133) 

TiKV：

- [bb7133](https://github.com/bb7133) 