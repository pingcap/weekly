---
title: Weekly update (July 02 ~ July 08, 2018)
date: 2018-07-09
summary: Last week, we landed 34 PRs in the TiDB repositories, 5 PRs in the TiSpark repositories, and 26 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [34 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-07-02..2018-07-08) in the TiDB repositories.

## Added

- [Support session variables `warning_count` and `error_count`](https://github.com/pingcap/tidb/pull/6945)
- [Support `BIT_OR` in the new aggregation function framework](https://github.com/pingcap/tidb/pull/6975)

## Fixed

- [Fix the privilege bug when reusing chunks](https://github.com/pingcap/tidb/pull/6976)
- [Fix the issue that the `Hash Aggregate` operator cannot exit](https://github.com/pingcap/tidb/pull/6982)
- [Fix a panic on `Stream Aggregate`](https://github.com/pingcap/tidb/pull/6984)
- [Fix the results of `SHOW CREATE TABLE` when adding indices](https://github.com/pingcap/tidb/pull/6993)
- [Fix the results of non-integer inputs for bit related aggregate functions](https://github.com/pingcap/tidb/pull/6994)

## Improved

- [Use feedback to refine updating statistics information](https://github.com/pingcap/tidb/pull/6796)
- [Refactor statistics updating mechanism to speed up analyzing tables](https://github.com/pingcap/tidb/pull/6901)
- [Allow the user to kill his own connections without the `SUPER` privilege](https://github.com/pingcap/tidb/pull/6954)

# Weekly update in TiSpark

Last week, we landed [5 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-07-02..2018-07-08) in the TiSpark repositories.

## Improved

- [Allow TiSpark to retrieve row ID](https://github.com/pingcap/tispark/pull/367)
- [Add more rules for `scalafmt`](https://github.com/pingcap/tispark/pull/386)

## Fixed

- [Fix the issue that the scan iterator throws `NoSuchElement Exception` when encountering the last Region](https://github.com/pingcap/tispark/pull/383)
- [Fix the issue that tispark-sql `dbName` is displayed as the table name](https://github.com/pingcap/tispark/pull/379)

# Weekly update in TiKV and PD

Last week, we landed [26 PRs](https://github.com/search?p=1&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-07-02..2018-07-08&type=Issues&utf8=%E2%9C%93) in the TiKV and PD repositories.

## Added

- [Add a new scalar function `multiply_int_unsigned`](https://github.com/pingcap/tikv/pull/3277)
- [Support getting Region approximate middle key by tikv-ctl](https://github.com/pingcap/tikv/pull/3260)
- [Add an option to restrict the number of RocksDB log files](https://github.com/pingcap/tikv/pull/3259)
- [Add the development workflow file for PD](https://github.com/pingcap/pd/pull/1141)

## Fixed

- [Fix the split check bug when `region_max_size` equals to `region_split_size`](https://github.com/pingcap/tikv/pull/3274)
- [Fix the panic issue when no operator is produced by the adjacent Region scheduler](https://github.com/pingcap/pd/pull/1139)
- [Fix the issue that the store space is used up due to moving replicas](https://github.com/pingcap/pd/pull/1138)

## Improved

- [Use `crossbeam-channel` to improve the performance](https://github.com/pingcap/tikv/pull/3278)
- [Enlarge the total slots of the scheduler latch](https://github.com/pingcap/tikv/pull/3283)
- [Exit all Goroutines ASAP when the PD client is closed](https://github.com/pingcap/pd/pull/1135)
- [Send back HTTP 400 where there is a client error](https://github.com/pingcap/pd/pull/1131)

# New contributors (Thanks!)

- TiDB: [zbdba](https://github.com/zbdba)
- TiSpark: [gkdoc](https://github.com/gkdoc)
- TiKV: [GuillaumeGomez](https://github.com/GuillaumeGomez)