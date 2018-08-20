---
title: Weekly update (August 13 ~ August 19, 2018)
date: 2018-08-20
summary: Last week, we landed 46 PRs in the TiDB repository, 2 PRs in the TiSpark repository, and 48 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [46 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-08-13..2018-08-19+) in the TiDB repository.

## Added

- [Store the TiDB server information to PD and add the HTTP API handle](https://github.com/pingcap/tidb/pull/7082)
- [Support dropping the index for the partitioned table](https://github.com/pingcap/tidb/pull/7306)
- [Support the `Replace` operation for table partition](https://github.com/pingcap/tidb/pull/7309)
- [Add `BatchPut` and `BatchDelete` for the `Raw` client](https://github.com/pingcap/tidb/pull/7330)
- [Support `CharsetOpt` to load the data statement in `Parser`](https://github.com/pingcap/tidb/pull/7391)

## Fixed

- [Fix `group_concat` when the chunk size is set to 1](https://github.com/pingcap/tidb/pull/7323)
- [Fix the `admin check index` panic when the index contains the `pkIsHandle` column](https://github.com/pingcap/tidb/pull/7350)
- [Fix the fraction part handle of `current_timestamp`](https://github.com/pingcap/tidb/pull/7355)
- [Fix the panic in `checkRangePartitioningKeysConstraints` when creating table partitions by range columns](https://github.com/pingcap/tidb/pull/7366)
- [Set the proper customized timezone](https://github.com/pingcap/tidb/pull/7372)
- [Set the types of index columns in `CheckIndexRangeExec`](https://github.com/pingcap/tidb/pull/7376)
- [Fix the missing microsecond for the timestamp](https://github.com/pingcap/tidb/pull/7418)
- [Fix duplicate row check when the chunk size is small](https://github.com/pingcap/tidb/pull/7393)
- [Fix the return value of `resultType/flag` in the `enum`/`set` column information](https://github.com/pingcap/tidb/pull/7417)

## Improved

- [Log detailed statistics for the query feedback](https://github.com/pingcap/tidb/pull/7293)
- [Collect execution details and output them in the slow query log](https://github.com/pingcap/tidb/pull/7364)
- [Notify the statistics worker when truncating tables](https://github.com/pingcap/tidb/pull/7356)
- [Add a new interface `MergePartialResult` for the new aggregation framework](https://github.com/pingcap/tidb/pull/7281)

# Weekly update in TiSpark

Last week, we landed [2 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-08-13..2018-08-19) in the TiSpark repository.

## Fixed

- [Fix the Index Read error caused by splitting or moving Regions](https://github.com/pingcap/tispark/pull/415)
- [Refactor error handling](https://github.com/pingcap/tispark/pull/412)

# Weekly update in TiKV and PD

Last week, we landed [48 PRs](https://github.com/search?p=1&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-08-13..2018-08-19&type=Issues) in the TiKV and PD repositories.

## Added

- Support more functions in Coprocessor:

    - [`Sqrt`](https://github.com/tikv/tikv/pull/3476)
    - [`Pow`](https://github.com/tikv/tikv/pull/3475)
    - [`UnHex`](https://github.com/tikv/tikv/pull/3469)
    - [`is_ipv4`](https://github.com/tikv/tikv/pull/3460)
    - [`Tan`](https://github.com/tikv/tikv/pull/3456)
    - [`ASCII`](https://github.com/tikv/tikv/pull/3436)
    - [`Left`](https://github.com/pingcap/pd/pull/1184)
    - [`LeftShift`](https://github.com/tikv/tikv/pull/3391)

- [Add nodes dynamically in the PD simulator](https://github.com/pingcap/pd/pull/1202)
- [Add an option to disable the namespace checker](https://github.com/pingcap/pd/pull/1201)
- [Add `Version` and use `conf` to initialize nodes in the PD simulator](https://github.com/pingcap/pd/pull/1198)
- [Add `EvalConfigBuilder`](https://github.com/tikv/tikv/pull/3354)
- [Support `batch_split`](https://github.com/tikv/tikv/pull/3064)

## Fixed

- [Create a peer if needed when `pre-vote` is received](https://github.com/tikv/tikv/pull/3380)
- [Fix a bug in `do_div_mod`](https://github.com/tikv/tikv/pull/3336)

## Improved

- [Optimize MVCC scanners](https://github.com/tikv/tikv/pull/3449)
- [Refactor the PD Selector](https://github.com/pingcap/pd/pull/1194)
- [Optimize `prefix_next`](https://github.com/tikv/tikv/pull/3446)
- [Decode bytes in place](https://github.com/tikv/tikv/pull/3427)
- [Improve the performance of the Region tree](https://github.com/pingcap/pd/pull/1184)

# New contributors (Thanks!)

TiDB:

- [mengnan](https://github.com/supernan1994)

TiKV:

- [arosspope](https://github.com/arosspope)
- [bombless](https://github.com/bombless)
- [opensourcegeek](https://github.com/opensourcegeek)
- [xiangyuf](https://github.com/xiangyuf)

PD:

- [lerencao](https://github.com/lerencao)

docs:

- [lerencao](https://github.com/lerencao)

docs-cn:

- [ahdong2007](https://github.com/ahdong2007)
- [lerencao](https://github.com/lerencao)