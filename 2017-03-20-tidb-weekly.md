---
title: Weekly update (March 13 ~ March 19, 2017)
date: 2017-03-20
summary: Last week, we landed 33 PRs in the TiDB repositories and 10 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV']
---

# Weekly update in TiDB

Last week, we landed [33 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-03-13..2017-03-19%20) in the TiDB repositories.

## Added

* [Add system table `mysql.stats_meta`](https://github.com/pingcap/tidb/pull/2766): used for storing statistic information.

* [Add a Restful API to get region info from pd.](https://github.com/pingcap/tidb/pull/2774)

* [Add a system variable to control the behavior of unfolding subquery in `in` expression.](https://github.com/pingcap/tidb/pull/2816)

* Add many builtin functions: [`acos, asin, atan`](https://github.com/pingcap/tidb/pull/2828), [`make_set`](https://github.com/pingcap/tidb/pull/2831), [`oct`](https://github.com/pingcap/tidb/pull/2835), [`pi`](https://github.com/pingcap/tidb/pull/2836), [`lpad`](https://github.com/pingcap/tidb/pull/2838), [`radians`](https://github.com/pingcap/tidb/pull/2841), [`exp`](https://github.com/pingcap/tidb/pull/2847), [`ip_v6`](https://github.com/pingcap/tidb/pull/2872)

## Fixed

* [Check truncated UTF8 string when casting value.](https://github.com/pingcap/tidb/pull/2819)

* [Fix data race.](https://github.com/pingcap/tidb/pull/2833)

* [Stop the service when meet critical error.](https://github.com/pingcap/tidb/pull/2854)

* [Keep the return value of builtin function `conv` consistent with MySQL when meet invalid input.](https://github.com/pingcap/tidb/pull/2842)

## Improved

* [Refactor tikv coprocessor client:](https://github.com/pingcap/tidb/pull/2804) make code cleaner and fix memory leak.

* [Refactor code about aggregation pushdown and aggregation prunning:](https://github.com/pingcap/tidb/pull/2820) make code cleaner.


## New Contributors

**Thank you guys!**

* [Huxley Hu](https://github.com/framlog)

* [Zhao Yi Jun](https://github.com/ariesdevil)

* [silenceper](https://github.com/silenceper)

* [Rick Yu](https://github.com/cosmtrek)

* [Qiannan](https://github.com/hsqlu)

* [Tao Meng](https://github.com/mtunique)

* [yangwenmai](https://github.com/yangwenmai)

* [Hongyuan Wang](https://github.com/yuanwhy)

* [8cbx](https://github.com/8cbx)

* [alston111111](https://github.com/alston111111)

* [Du Chuan](https://github.com/spongedu)

# Weekly update in TiKV

Last week, We landed [10 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-03-12..2017-03-18&type=Issues&ref=searchresults) in the TiKV repositories.

## Added

* Use [`SSE`](https://github.com/pingcap/tikv/pull/1677) support by default.

* Handle [`CTRL + D`] in `pd-ctl` (https://github.com/pingcap/pd/pull/570)

## Fixed

* [Avoid panic](https://github.com/pingcap/pd/pull/567) when get the tombstone store information. 

* [Check epoch](https://github.com/pingcap/tikv/pull/1682) in ReadIndex to avoid stale read. 

* [Clean ReadIndex callback](https://github.com/pingcap/tikv/pull/1683) when peer is destroyed to avoid deadlock.

## Improved

* [Queue vote](https://github.com/pingcap/tikv/pull/1670) to prevent followers from discarding it if region hasn’t been split. 

* Improve [random picking](https://github.com/pingcap/pd/pull/565) region from cache.
