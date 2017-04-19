---
layout: post
title: Weekly Update
---
## Weekly update in TiDB

# 2017-04-17

Last two weeks, we landed [26 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-04-10..2017-04-16%20) in the TiDB repositories.

## Added

* [Update etcd client in vendor.](https://github.com/pingcap/tidb/pull/3032)

* Add builtin function [`time-to-sec`](https://github.com/pingcap/tidb/pull/2987)

* Add definition for builtin functions: [`bit_count `, `to_base64 `, `right `](https://github.com/pingcap/tidb/pull/3016/files)


## Fixed

* [Fix the error message for data overflow.](https://github.com/pingcap/tidb/pull/3017)

* [Fix a panic.](https://github.com/pingcap/tidb/pull/3020)

* [Fix a bug in top-n pushdown.](https://github.com/pingcap/tidb/pull/3021)

* [Fix a data race bug in session context.](https://github.com/pingcap/tidb/pull/3049)

* [Fix a bug in name resolver for GroupBy clause.](https://github.com/pingcap/tidb/pull/3050)


## Improved

* Refactor optimizer: [Implement new planner interface for projection and sort.](https://github.com/pingcap/tidb/pull/3006)

* Refactor statistic module.[#3014](https://github.com/pingcap/tidb/pull/3014), [#3019](https://github.com/pingcap/tidb/pull/3019), [#3029](https://github.com/pingcap/tidb/pull/3029), [#3031](https://github.com/pingcap/tidb/pull/3031), [#3044](https://github.com/pingcap/tidb/pull/3044), [#3048](https://github.com/pingcap/tidb/pull/3048), [#3053](https://github.com/pingcap/tidb/pull/3053)

* Refactor coprocessor architecture: [#3009](https://github.com/pingcap/tidb/pull/3009), [#3027](https://github.com/pingcap/tidb/pull/3027)

* [Use etcd for privilege update notification among tidb-servers.](https://github.com/pingcap/tidb/pull/3030)

* [Enlarge the limitation of write flow to TiKV.](https://github.com/pingcap/tidb/pull/3035)

* [Reduce memory usage in HashAggregate operator.](https://github.com/pingcap/tidb/pull/3028)

* [Reduce memory usage in Distinct operator.](https://github.com/pingcap/tidb/pull/3033)

* [Code cleanup in type infer.](https://github.com/pingcap/tidb/pull/3039)

## New Contributors

**Thank you guys!**

* [Xuanwo](https://github.com/Xuanwo)

*[fudali113](https://github.com/fudali113)

# Weekly update in TiKV

# 2017-04-17

Last week, We landed [18 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-04-09..2017-04-15&type=Issues) in the TiKV repositories.

## Added

* Support [memory profiling](https://github.com/pingcap/tikv/pull/1723).

* Add [block cache](https://github.com/pingcap/tikv/pull/1739) monitoring.

* Add log for [critical](https://github.com/pingcap/pd/pull/610) operations.  

* Use `tokio-core` to support asynchronous PD client, see [1745](https://github.com/pingcap/tikv/pull/1745), [1752](https://github.com/pingcap/tikv/pull/1752), [1753](https://github.com/pingcap/tikv/pull/1753).

## Fixed

* Always [update PD client](https://github.com/pingcap/tikv/pull/1759) to avoid PD client can not reconnecting to PD server after network error.  

* Fix the bug when [decode empty data](https://github.com/pingcap/pd/pull/617) to a `StringSlice`. 

* Fix a [deadlock](https://github.com/pingcap/tikv/pull/1768) bug when PD client reconnects server.

## Improved

* Add lots of test cases to improve stability, see [1737](https://github.com/pingcap/tikv/pull/1737) , [1738](https://github.com/pingcap/tikv/pull/1738), [1742](https://github.com/pingcap/tikv/pull/1742).
