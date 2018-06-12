---
title: Weekly update (June 04 ~ June 10, 2018)
date: 2018-06-11
summary: Last week, we landed 50 PRs in the TiDB repositories, 2 PRs in the TiSpark repositories, and 20 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [50 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-06-04..2018-06-10) in the TiDB repositories.

## Added

- [Support `ALTER TABLE RENAME KEY`](https://github.com/pingcap/tidb/pull/6475)
- [Support `SHOW MASTER STATUS`](https://github.com/pingcap/tidb/pull/6785)
- [Support setting TSO into the `tidb_snapshot` session variable](https://github.com/pingcap/tidb/pull/6749)
- [Support the `ALTER TABLE DROP COLUMN CASCADE` syntax](https://github.com/pingcap/tidb/pull/6791)

## Fixed

- [Make `TIDB_SMJ` take effect when no index can be used](https://github.com/pingcap/tidb/pull/6454)
- [Fix the `SelectLock` option for the `UNION` statement](https://github.com/pingcap/tidb/pull/6579)
- [Fix a bug of the `DROP USER` statement](https://github.com/pingcap/tidb/pull/6624)
- [Fix a bug of `WrapWithCastAsJSON`](https://github.com/pingcap/tidb/pull/6678)
- [Detect the duplication of table alias for the `JOIN` statement](https://github.com/pingcap/tidb/pull/6716)
- [Fix some bugs of the `DECIMAL` values](https://github.com/pingcap/tidb/pull/6721)
- [Do not allow the `YEAR` type to have the `UNSIGNED` flag](https://github.com/pingcap/tidb/pull/6745)
- [Refine row count estimation](https://github.com/pingcap/tidb/pull/6746)
- [Fix a bug of failing to fetch the profile by pprof](https://github.com/pingcap/tidb/pull/6747)
- [Fix the wrong result of the `UNION` statement](https://github.com/pingcap/tidb/pull/6752)
- [Fix the wrong result of `Merge Join`](https://github.com/pingcap/tidb/pull/6753)
- [Handle `NULL datum` when converting it to a string in statistics](https://github.com/pingcap/tidb/pull/6761)
- [Fix the issue of checking `LIMIT` and `ORDER BY` in the `UNION` statement](https://github.com/pingcap/tidb/pull/6783)

## Improved

- [Add max backoff settings for tikv-client](https://github.com/pingcap/tidb/pull/6770)
- [Support parallel projection](https://github.com/pingcap/tidb/pull/6323)
- [Make the error message of `ADMIN CHECK TABLE` more readable](https://github.com/pingcap/tidb/pull/6617)
- [Improve the constant folding for the `IF` and `IFNULL` built-in functions](https://github.com/pingcap/tidb/pull/6677)
- [Push the `FLOOR` built-in function to TiKV](https://github.com/pingcap/tidb/pull/6736)
- [Push the built-in functions `IS TRUE`/`IS FALSE` to TiKV](https://github.com/pingcap/tidb/pull/6751)
- [Append the current time into the error message when backoff occurs](https://github.com/pingcap/tidb/pull/6741)
- [Refine the result of the `EXPLAIN` statement](https://github.com/pingcap/tidb/pull/6755)

# Weekly update in TiSpark

Last week, we landed [2 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-06-04..2018-06-10) in the TiSpark repositories.

## Fixed

- [Fix a test failure](https://github.com/pingcap/tispark/pull/361)

# Weekly update in TiKV and PD

Last week, we landed [20 PRs](https://github.com/search?p=1&q=repo:pingcap/tikv+repo:pingcap/pd+is:pr+is:merged+merged:2018-06-04..2018-06-10&type=Issues&utf8=%E2%9C%93) in the TiKV and PD repositories.

## Added

- [Report the number of rows in the Region](https://github.com/pingcap/tikv/pull/3159)

## Fixed

- [Fix a bug in `do_sub`](https://github.com/pingcap/tikv/pull/3145)

## Improved

- [Increase metrics of sending and generating a snapshot](https://github.com/pingcap/tikv/pull/3132)
- [Add `ReadExecutor` to execute the Get and Snap commands](https://github.com/pingcap/tikv/pull/3161)
- [Upgrade etcd to master](https://github.com/pingcap/pd/pull/1101)
