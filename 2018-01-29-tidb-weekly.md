---
title: Weekly update (January 22 ~ January 28, 2018)
date: 2018-01-29
summary: Last week, we landed 28 PRs in the TiDB repositories, 4 PRs in the TiSpark repositories, and 17 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [28 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is:pr+is:merged+merged:2018-01-22..2018-01-28) in the TiDB repositories.

## Added

* [Add the importer tool](https://github.com/pingcap/tidb/pull/5695)
* [Add metrics for GC failure count](https://github.com/pingcap/tidb/pull/5694)
* [Add metrics for TiDB-server panic](https://github.com/pingcap/tidb/pull/5692)
* [Add metrics for async secondary lock cleanup](https://github.com/pingcap/tidb/pull/5575)
* [Support create time in `information_schema`](https://github.com/pingcap/tidb/pull/5590/files)

## Removed

* [Remove `GetSessionVars()` in expression evaluation](https://github.com/pingcap/tidb/pull/5683)
* [Remove `varsutil` package, and make `Systems` a private member of `SessionVars`](https://github.com/pingcap/tidb/pull/5544)

## Fixed

* [Avoid the generation of mysql.TypeNewDate](https://github.com/pingcap/tidb/pull/5705)
* [Push down binaryliterals as varstring](https://github.com/pingcap/tidb/pull/5665)

## Improved

* [Keep slow query log entry in order](https://github.com/pingcap/tidb/pull/5732)
* [Make `list.MemoryUsage()` more efficient](https://github.com/pingcap/tidb/pull/5723)
* [Limit statement count in a transaction](https://github.com/pingcap/tidb/pull/5704)
* [Remove `WithCancel` in `copIterator`](https://github.com/pingcap/tidb/pull/5701)
* [Uniform the way of iterating rows within a `Chunk`](https://github.com/pingcap/tidb/pull/5674)

# Weekly update in TiSpark

Last week, we landed [4 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-01-22..2018-01-28) in the TiSpark repositories.

## Improved

* [Improved index double read performance by around 30%](https://github.com/pingcap/tispark/pull/172)
* [Verified and added document for Hive integration](https://github.com/pingcap/tispark/pull/225)

## Fixed

* [Fixed test for between expression](https://github.com/pingcap/tispark/pull/222)
* [Added placeholder for unsupported type preventing schema reading crash](https://github.com/pingcap/tispark/pull/218)

# Weekly update in TiKV and PD

Last week, we landed [17 PRs](https://github.com/search?q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-01-22..2018-01-28) in the TiKV and PD repositories.

## Added

* [Add ImportSST/UploadSST API](https://github.com/pingcap/tikv/pull/2662)
* [Add drop region admin command](https://github.com/pingcap/pd/pull/931)

## Fixed

* [Convert int to decimal in sum](https://github.com/pingcap/tikv/pull/2694)
* [Fix join failure when log dir is the same as data dir](https://github.com/pingcap/pd/pull/929)
* [Disable the portable on MacOS](https://github.com/pingcap/tikv/pull/2696)

## Improved

* [Limit data size for scan lock](https://github.com/pingcap/tikv/pull/2664)
* [Add metrics for checkers](https://github.com/pingcap/pd/pull/928)
* [Remove schedule empty apply task](https://github.com/pingcap/tikv/pull/2706)
* [Ignore Prometheus encoding error](https://github.com/pingcap/tikv/pull/2707)
* [Debug trait for snapshot](https://github.com/pingcap/tikv/pull/2685)
* [Reduce the lock overhead](https://github.com/pingcap/pd/pull/930)
* [Update the region size](https://github.com/pingcap/tikv/pull/2636)

# New contributor (Thanks!)

* TiDB: [yuananf](https://github.com/yuananf)