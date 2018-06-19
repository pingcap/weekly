---
title: Weekly update (June 11 ~ June 17, 2018)
date: 2018-06-19
summary: Last week, we landed 26 PRs in the TiDB repositories and 28 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [26 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-06-11..2018-06-17) in the TiDB repositories.

## Added

- [Support the MySQL syntax `show privileges`](https://github.com/pingcap/tidb/pull/6792)
- [Add the limit for the number of columns when adding columns](https://github.com/pingcap/tidb/pull/6778)
- [Add the sanity check of the precision and the scale for numeric types](https://github.com/pingcap/tidb/pull/6813)

## Fixed

- [Fix the wrong results of the `CONCAT_WS` built-in function](https://github.com/pingcap/tidb/pull/6762)
- [Fix a bug in right join when some predicates are pushed to the right table](https://github.com/pingcap/tidb/pull/6809)
- [Fix the missing start timestamp for `TableDual` in a transaction](https://github.com/pingcap/tidb/pull/6830)

## Improved

- [Refactor the structure of the DDL package](https://github.com/pingcap/tidb/pull/6449)
- [Remove new lines and add the user information in the query log](https://github.com/pingcap/tidb/pull/6748)
- [Make the limitation of query memory usage configurable](https://github.com/pingcap/tidb/pull/6788)
- [Change the factor of the descending scan according to the improvement of descending scan performance in TiKV](https://github.com/pingcap/tidb/pull/6812)

# Weekly update in TiKV and PD

Last week, we landed [28 PRs](https://github.com/search?p=1&q=repo:pingcap/tikv+repo:pingcap/pd+is:pr+is:merged+merged:2018-06-11..2018-06-17&type=Issues&utf8=%E2%9C%93) in the TiKV and PD repositories.

## Added

- [Enable `prevote` in PD by default](https://github.com/pingcap/pd/pull/1103)
- [Process approximate rows in Region](https://github.com/pingcap/pd/pull/1104)

## Fixed

- [Fix the issue of escaping the `\xFF` sequences to a single byte](https://github.com/pingcap/tikv/pull/3182)

## Improved

- [Shrink the pending command queue in `ApplyDelegate`](https://github.com/pingcap/tikv/pull/3106)
- [Output a log when GC finds too many versions for a single key](https://github.com/pingcap/tikv/pull/3178)
- [Upgrade `protobuf` and `grpcio`](https://github.com/pingcap/tikv/pull/3142)
- [Support initialization empty Region in `tikv-ctl`](https://github.com/pingcap/tikv/pull/3178)
- [Adjust the pending peer filter](https://github.com/pingcap/pd/pull/1110)

# New contributors (Thanks!)

TiDB:

- [chenyang8094](https://github.com/chenyang8094)
- [Angryrou](https://github.com/angryrou)

TiKV:

- [kbacha](https://github.com/kbacha)
- [maninalift](https://github.com/maninalift)
