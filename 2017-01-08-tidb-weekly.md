---
date: 2017-01-08T00:00:00Z
title: Weekly Update
url: /2017/01/08/tidb-weekly/
---

## Weekly update in TiDB

Last week, we landed [38 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-01-02..2017-01-08%20) in the TiDB repositories.

## Added

* [Add nested loop join.](https://github.com/pingcap/tidb/pull/2365)

* [Support the `UNIX_TIMESTAMP` built-in function.](https://github.com/pingcap/tidb/pull/2369)

* [Support the `INTERVAL` built-in function.](https://github.com/pingcap/tidb/pull/2370)

* [Support the `FIND_IN_SET` built-in function.](https://github.com/pingcap/tidb/pull/2373)

* [Support the `DATEDIFF` built-in function.](https://github.com/pingcap/tidb/pull/2374)

* [Enable pushing down `IF` expr to TiKV coprocessor](https://github.com/pingcap/tidb/pull/2387)

## Fixed

* [In prepared statement, limit and offset could be parameter marker.](https://github.com/pingcap/tidb/pull/2364)

* [When creating table, index option could be a list.](https://github.com/pingcap/tidb/pull/2366)

* [Fix a bug in creating table, some field length is missing.](https://github.com/pingcap/tidb/pull/2382)

* [Fix a bug about parsing datetime overflow.](https://github.com/pingcap/tidb/pull/2401)

* [Trim leading zeros before parsing int literal.](https://github.com/pingcap/tidb/pull/2404)

* [Fix float truncate bug.](https://github.com/pingcap/tidb/pull/2405)

## Improved

* [Improve TiDB schema lease checker.](https://github.com/pingcap/tidb/pull/2327)

* [Speed up alter table add index statement.](https://github.com/pingcap/tidb/pull/2341)

* [Refactor system variable related code.](https://github.com/pingcap/tidb/pull/2359)

* Refactor built-in function, add function class and function signature: [#2361](https://github.com/pingcap/tidb/pull/2361), [#2384](https://github.com/pingcap/tidb/pull/2384), [#2385](https://github.com/pingcap/tidb/pull/2385), [#2389](https://github.com/pingcap/tidb/pull/2389), [#2391](https://github.com/pingcap/tidb/pull/2391), [#2399](https://github.com/pingcap/tidb/pull/2399), [#2410](https://github.com/pingcap/tidb/pull/2410)

* [Add unique key information into plan's schema](https://github.com/pingcap/tidb/pull/2376), this will be used for plan optimizing.

* [Fetch tso and compiling statement concurrently](https://github.com/pingcap/tidb/pull/2393): reduce the latency of small transaction.

* [Load data in a batch way](https://github.com/pingcap/tidb/pull/2394): make it easier for loading large data.

* [Extract a built-in function factory for date arithmetic operations.](https://github.com/pingcap/tidb/pull/2403)


## New contributor

* [idlesummerbreeze](https://github.com/idlesummerbreeze)


# Weekly update in TiKV

Last week, We landed [15 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-01-02..2017-01-08&type=Issues&ref=searchresults) in the TiKV repositories.

## Added

* Support [pre vote](https://github.com/pingcap/tikv/pull/1444) feature for raft.

* Schedule replicas according to the [location of the stores](https://github.com/pingcap/pd/pull/462).

* Coprocessor support [`if`](https://github.com/pingcap/tikv/pull/1459), [`IsNull`](https://github.com/pingcap/tikv/pull/1460), [`IfNull`](https://github.com/pingcap/tikv/pull/1461) and [`NullIf`](https://github.com/pingcap/tikv/pull/1463).

## Fixed

* Check [cluseter ID](https://github.com/pingcap/pd/pull/456) to avoid PD joining different cluster.

## Improved

* Return [`StoreNotMatch`](https://github.com/pingcap/tikv/pull/1457) error when store ID doesn't match.

* Use [upper bound](https://github.com/pingcap/tikv/pull/1470) for scanner.

* [Unify logger](https://github.com/pingcap/tikv/pull/1476) to make the log format the same with TiDB/PD.
