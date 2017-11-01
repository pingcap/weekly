---
title: Weekly update (March 6 ~ March 12, 2017)
date: 2017-03-13
summary: Last week, we landed 30 PRs in the TiDB repositories and 13 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV']
---

# Weekly update in TiDB

Last week, we landed [30 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-03-06..2017-03-12%20) in the TiDB repositories.

## Added

* [Add context in exector](https://github.com/pingcap/tidb/pull/2748): prepare for canceling execution.

* [Support the `KILL` statement.](https://github.com/pingcap/tidb/pull/2768)

* [Support string literal with in the national character set `N'literal'`.](https://github.com/pingcap/tidb/pull/2773)

* [Check privilege when running create user statement.](https://github.com/pingcap/tidb/pull/2785)

* [Add a session variable to prevent eager aggregation.](https://github.com/pingcap/tidb/pull/2809)

## Fixed

* [Clean up pending task when close executor](https://github.com/pingcap/tidb/pull/2775): fix memory leak.

* [Make the type of coalesce function the same with MySQL.](https://github.com/pingcap/tidb/pull/2788)

* [Clean up process info when finish running statement.](https://github.com/pingcap/tidb/pull/2790)

* [Fix a bug in optimizer about pushing down limit across filter.](https://github.com/pingcap/tidb/pull/2793)

* [Fix a bug in optimizer about column prunning on union statement.](https://github.com/pingcap/tidb/pull/2796)

* [Use `QUOTE` as an identifier.](https://github.com/pingcap/tidb/pull/2805)


## Improved

* [Create user automatically when grant privilege for unexist user.](https://github.com/pingcap/tidb/pull/2756)

* [Speed up Add Column statement.](https://github.com/pingcap/tidb/pull/2769)

* [Update grpc version to v1.0.4 in vendor.](https://github.com/pingcap/tidb/pull/2784)

* [Avoid useless schema version update when running DDL.](https://github.com/pingcap/tidb/pull/2786)

* [Add metrics for potential time-consuming queries.](https://github.com/pingcap/tidb/pull/2795)



# Weekly update in TiKV

Last week, We landed [13 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-03-05..2017-03-11&type=Issues&ref=searchresults) in the TiKV repositories.

## Added

* Add [metric](https://github.com/pingcap/tikv/pull/1657) for RocksDB compaction.

* Collect [scanned key count](https://github.com/pingcap/tikv/pull/1661) to detect region access hotspot. 

* Support [`GetRegionByID`](https://github.com/pingcap/pd/pull/555) for `pd-ctl`.

* Enable [AutoCompactionRetention](https://github.com/pingcap/pd/pull/562) to reduce PD space occupation.

## Fixed

* [Reduce manual compaction](https://github.com/pingcap/tikv/pull/1664) for Lock CF to avoid too many WAL logs. 

* Only check scheduler busy error for  [Write](https://github.com/pingcap/tikv/pull/1668) command.

* Fix [data race](https://github.com/pingcap/pd/pull/559) for updating replication configuration. 

* Prohibit joining the PD cluster with [empty](https://github.com/pingcap/pd/pull/564) name.

## Improved

* [Beautify](https://github.com/pingcap/pd/pull/554) region log.  

* [Cleanup](https://github.com/pingcap/tikv/pull/1662) iterator creation. 

* Adjust [default leader scheduler limit](https://github.com/pingcap/pd/pull/566) to speed up leader balance.
