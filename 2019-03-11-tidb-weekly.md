---
title: Weekly update (March 04 ~ March 10, 2019)
date: 2019-03-11
summary: Last week, we landed 51 PRs in the TiDB repository, 2 PRs in the TiSpark repository, and 15 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [51 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-03-04..2019-03-10) in the TiDB repository.

## Added

- [Support the `first_value` and `last_value` window functions](https://github.com/pingcap/tidb/pull/9560)
- [Change all the MySQL versions from 5.7.10 to 5.7.25](https://github.com/pingcap/tidb/pull/9553)
- [Handle the default frame for window functions](https://github.com/pingcap/tidb/pull/9544)
- [Support the `show pump status` and `show drainer status` statements](https://github.com/pingcap/tidb/pull/9456)

## Improved

- [Add a new logger to help log `connID` and `recvTs`](https://github.com/pingcap/tidb/pull/9548)
- [Improve the `str_to_date` built-in function compatibility](https://github.com/pingcap/tidb/pull/9617)
- [Refine the rollback logic of canceling modifying a column and adding and dropping a foreign key](https://github.com/pingcap/tidb/pull/9613)
- [Convert `SemiJoin` to `InnerJoin` in more cases](https://github.com/pingcap/tidb/pull/9546)
- [Control the chunk size for `StreamAgg` and `HashAgg`](https://github.com/pingcap/tidb/pull/9512)
- [Refactor the code related to join reorder](https://github.com/pingcap/tidb/pull/9439)
- [Validate fsp for `datetime` and `timestamp` if they are used as the default value](https://github.com/pingcap/tidb/pull/9327)
- [Upgrade to Go 1.12](https://github.com/pingcap/tidb/pull/9299)
- [Update `ddl_slow_threshold`](https://github.com/pingcap/tidb/pull/9043)

## Fixed

- [Fix the error message that the table does not exist in Inner Join](https://github.com/pingcap/tidb/pull/9626)
- [Fix the `git describe` error in some cases](https://github.com/pingcap/tidb/pull/9611)
- [Fix an unexpected error when using window functions and View](https://github.com/pingcap/tidb/pull/9605)
- [Fix the error when setting `variable=''`](https://github.com/pingcap/tidb/pull/8537)
- [Fix the issue that etcd clients lost connection with the PD cluster in some cases](https://github.com/pingcap/tidb/pull/9575)
- [Quote the database name before running SQL statements](https://github.com/pingcap/tidb/pull/9547)
- [Fix the issue that the behavior of aggregation in subqueries is incompatible with MySQL](https://github.com/pingcap/tidb/pull/9542)
- [Fix the error occurred when canceling dropping a table or database in some cases](https://github.com/pingcap/tidb/pull/9524)
- [Fix the issue that the outer table is chosen wrongly when both tables are specified in `TIDB_INLJ`](https://github.com/pingcap/tidb/pull/9579)

# Weekly update in TiSpark

Last week, we landed [2 PRs](https://github.com/pingcap/tispark/pulls?utf8=✓&q=is%3Apr+is%3Amerged+merged%3A2019-03-04..2019-03-10+) in the TiSpark repository.

## Improved

- [Skip `LockResolverTest` when the PD client is not present](https://github.com/pingcap/tispark/pull/579)

# Weekly update in TiKV and PD

Last week, we landed [15 PRs](https://github.com/search?p=1&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-03-04..2019-03-10&type=Issues) in the TiKV and PD repositories.

## Added

* [Introduce the `VectorLike` enum for the endpoint](https://github.com/tikv/tikv/pull/4320)
* [Add checks for the SSE4.2 support](https://github.com/tikv/tikv/pull/4314)
* [Add the communication section in README](https://github.com/tikv/tikv/pull/4285)
* [Implement `sub_datetime_and_duration` and `sub_datetime_and_string`](https://github.com/tikv/tikv/pull/4269)
* [Add functions to build batch executors](https://github.com/tikv/tikv/pull/4243)

## Improved

* [Unify the log format in the Raftstore module](https://github.com/tikv/tikv/pull/4307)
* [Validate the scheduler name in the PD configuration](https://github.com/pingcap/pd/pull/1449)
* [Remove `extern crate` statements](https://github.com/tikv/tikv/pull/4297)
* [Remove message boxing and message unboxing](https://github.com/tikv/tikv/pull/4232)
* [Publish the important configuration to metrics](https://github.com/tikv/tikv/pull/4206)
* [Use the address instead of the store ID for metrics](https://github.com/pingcap/pd/pull/1429)
* [Make the heartbeat more reasonable in the simulator](https://github.com/pingcap/pd/pull/1418)

## Fixed

* [Fix the issue that the low space store cannot be added in PD](https://github.com/pingcap/pd/pull/1453)
* Fix several typos
    - [#1451](https://github.com/pingcap/pd/pull/1451)
    - [#4305](https://github.com/tikv/tikv/pull/4305)

# New contributors (Thanks!)

tikv:

- [wujunze](https://github.com/wujunze)

pd:

- [blankstars](https://github.com/blankstars)

parser:

- [sunxiaoguang](https://github.com/sunxiaoguang)