---
title: Weekly update (March 25 ~ March 31, 2019)
date: 2019-04-01
summary: Last week, we landed 62 PRs in the TiDB repository, 10 PRs in the TiSpark repository, and 21 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---


# Weekly update in TiDB

Last week, we landed [62 PRs](https://github.com/pingcap/tidb/pulls?page=1&q=is%3Apr+is%3Amerged+merged%3A2019-03-25..2019-03-31&utf8=%E2%9C%93) in the TiDB repository.

## Added

- [Introduce a new executor to support SQL statements like `GRANT roles TO users`](https://github.com/pingcap/tidb/pull/9721)

## Improved

- [Refine the `ErrEntryTooLarge` error message](https://github.com/pingcap/tidb/pull/9881)
- [Use the unified log format for the `server` package and the remaining packages](https://github.com/pingcap/tidb/pull/9878)
- [Make `tidb_disable_txn_auto_retry` disable retry only for the write conflict](https://github.com/pingcap/tidb/pull/9827)
- [Enhance the UTF-8 charset upgrade compatibility](https://github.com/pingcap/tidb/pull/9820)
- [Add the HTTP status host](https://github.com/pingcap/tidb/pull/9814)
- [Improve NULL count estimation for single-column indexes](https://github.com/pingcap/tidb/pull/9474)
- [Add the audit plugin extension point](https://github.com/pingcap/tidb/pull/9136)

## Fixed

- [Fix the wrong result of `group_concat` for cases like `select group_concat(123, null)`](https://github.com/pingcap/tidb/pull/9921)
- [Fix the wrong result of `count(distinct)` when the parameter of `count(distinct)` is decimal](https://github.com/pingcap/tidb/pull/9901)
- [Fix the issue that converting `decimal` to `datetime` or `timestamp` is incompatible with MySQL in some cases](https://github.com/pingcap/tidb/pull/9899)
- [Fix the issue that plugin errors make TiDB exit in some cases](https://github.com/pingcap/tidb/pull/9889)
- [Fix the issue that results of `unix_timestamp()-unix_timestamp(now())` are wrong and not stable](https://github.com/pingcap/tidb/pull/9884)
- [Fix the issue that `date_add` and `date_sub` are incompatible with Mysql in some cases](https://github.com/pingcap/tidb/pull/9874)
- [Fix the issue that an invalid `YEAR` string is incompatible with MySQL](https://github.com/pingcap/tidb/issues/9767)
- [Fix the issue that `TIME_FORMAT` is incompatible with MySQL](https://github.com/pingcap/tidb/pull/9841)
- [Fix a wrong limit of `MaxInt64`](https://github.com/pingcap/tidb/pull/9834)
- [Fix a panic caused by a shallow copy of JSON](https://github.com/pingcap/tidb/pull/9833)
- [Fix the issue that `set time_zone` is incompatible with MySQL](https://github.com/pingcap/tidb/pull/9822)
- [Fix bugs when a window function meets `Prepare` in some cases](https://github.com/pingcap/tidb/pull/9795)
- [Fix the issue that `date_add` and `date_sub` are incompatible with MySQL](https://github.com/pingcap/tidb/pull/9702)
- [Set the correct return field type of the `CONVERT()` built-in function](https://github.com/pingcap/tidb/pull/9305)

# Weekly update in TiSpark

Last week, we landed [10 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-03-25..2019-03-31+) in the TiSpark repository.

## Added

- [Support `ShowColumnsCommand`](https://github.com/pingcap/tispark/pull/614)

## Improved

- [Clean up the `TiDAGRequest` code](https://github.com/pingcap/tispark/pull/616)

# Weekly update in TiKV and PD

Last week, we landed [21 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-03-25..2019-03-31&type=Issues) in the TiKV and PD repositories.

## Added

* [Add the batch index scan executor](https://github.com/tikv/tikv/pull/4419)
* [Add an API to clear tombstone stores](https://github.com/pingcap/pd/pull/1472)
* [Implement the `is_ipv4_compat` and `is_ipv4_mapped` coprocessor built-in functions](https://github.com/tikv/tikv/pull/4407)

## Fixed

* [Fix a Region statistics bug caused by a typo](https://github.com/tikv/tikv/pull/4452)
* [Fix a store statistics bug caused by a typo](https://github.com/tikv/tikv/pull/4436)
* [Fix a bug of `GetHotStores`](https://github.com/pingcap/pd/pull/1487)
* [Fix a log truncation issue during the exiting process](https://github.com/tikv/tikv/pull/4448)

# New contributors (Thanks!)

tidb:

- [Debiancc](https://github.com/Debiancc)

tikv:

- [myguyy](https://github.com/myguyy)
- [seansu4you87](https://github.com/seansu4you87)
- [xiaobogaga](https://github.com/xiaobogaga)
- [yaalsn](https://github.com/yaalsn)

pd:

- [bradyjoestar](https://github.com/bradyjoestar)

parser:

- [wuudjac](https://github.com/wuudjac)