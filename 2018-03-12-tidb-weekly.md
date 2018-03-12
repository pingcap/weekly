---
title: Weekly update (March 05 ~ March 11, 2018)
date: 2018-03-12
summary: Last week, we landed 38 PRs in the TiDB repositories, 8 PRs in the TiSpark repositories, and  32 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# TiDB 2.0 RC1 release

[TiDB 2.0 RC1 is released](https://www.pingcap.com/blog/2018-03-09-2rc1/). This release has great improvement in MySQL compatibility, SQL optimization and stability.

# Weekly update in TiDB

Last week, we landed [38 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftidb+is%3Apr+is%3Amerged+merged%3A2018-03-05..2018-03-11) in the TiDB repositories.

## Added

- [Supprt checking the consistency of an index](https://github.com/pingcap/tidb/pull/5932)
- [Support decoding a column value by HTTP API](https://github.com/pingcap/tidb/pull/5927)
- [Add validation for configuration](https://github.com/pingcap/tidb/pull/5864)
- [Add HTTP API for settings](https://github.com/pingcap/tidb/pull/5860)
- [Employ memory Tracker to track memory usage during query execution](https://github.com/pingcap/tidb/pull/5826)

## Fixed

- [Fix inconsistent behavior for `insert`](https://github.com/pingcap/tidb/pull/5968)
- [Correct the behavior of the bit aggregate function](https://github.com/pingcap/tidb/pull/5954)
- [Fix a bug that index is not used in a special case](https://github.com/pingcap/tidb/pull/5947)
- [Fix the field length of Boolean type](https://github.com/pingcap/tidb/pull/5944)
- [Handle warnings returned from `tikv`/`mocktikv`](https://github.com/pingcap/tidb/pull/5906)

## Improved

- [Set low priority for adding an index](https://github.com/pingcap/tidb/pull/5976)
- [Support pseudo `profiling` table for compatibility](https://github.com/pingcap/tidb/pull/5960)
- [Enhance decorrelation](https://github.com/pingcap/tidb/pull/5953)
- [Check the password format for `create user identified by password XXX`](https://github.com/pingcap/tidb/pull/5948)
- [Avoid the random error during Leader checking in GC](https://github.com/pingcap/tidb/pull/5816)
- [Make `CommitMaxBackoff` configurable](https://github.com/pingcap/tidb/pull/5764)

# Weekly update in TiSpark

Last week, we landed [8 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-03-05..2018-03-11) in the TiSpark repositories.

## Added

* [Add statistics information module](https://github.com/pingcap/tispark/pull/244)
* [Add the SQL dump for the Meta-server database](https://github.com/pingcap/tispark/pull/247)

## Fixed

* [Fix the parse exception when a table name contains symbols](https://github.com/pingcap/tispark/pull/252)
* [Fix `group by` in `DAGRequest`](https://github.com/pingcap/tispark/pull/256)
* [Fix a document link](https://github.com/pingcap/tispark/pull/260)

## Improved

* [Reduce `jar` size](https://github.com/pingcap/tispark/pull/254)

# Weekly update in TiKV and PD

Last week, we landed [32 PRs](https://github.com/search?q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-03-05..2018-03-11) in the TiKV and PD repositories.

## Added

- [Configure the check SSD](https://github.com/pingcap/tikv/pull/2747)
- [Check critical configurations when TiKV starts](https://github.com/pingcap/tikv/pull/2764)
- [Initialize `api` for metrics](https://github.com/pingcap/tikv/pull/2780)

## Fixed

- [Create a parent directory if it does not exist](https://github.com/pingcap/tikv/pull/2809)
- [Exclude offline store in `FilterSource`](https://github.com/pingcap/pd/pull/983)
- [Fix usage template](https://github.com/pingcap/pd/pull/982)
- [Fix a bug in SSD test](https://github.com/pingcap/tikv/pull/2802)
- [Cancel unused Region heartbeat RPC](https://github.com/pingcap/tikv/pull/2798)
- [Delete the overlap from etcd](https://github.com/pingcap/pd/pull/979)
- [Fix a panic caused by the merged Region](https://github.com/pingcap/pd/pull/978)
- [Fix stale Region information with overlaps that should be removed](https://github.com/pingcap/pd/pull/977)
- [Fix a segfault](https://github.com/pingcap/tikv/pull/2791)
- [Fix a bug of the operator type](https://github.com/pingcap/pd/pull/975)
- [Fix health status with TLS enabled](https://github.com/pingcap/pd/pull/969)

## Improved

- [Count the number of offline Regions](https://github.com/pingcap/pd/pull/986)
- [Tune the default snapshot I/O limitation](https://github.com/pingcap/tikv/pull/2808)
- [Increase the operator timeout](https://github.com/pingcap/pd/pull/981)
- [Record the elapsed time of `operatorStep`](https://github.com/pingcap/pd/pull/980)
- [Move storage read operations into `ReadPool`](https://github.com/pingcap/tikv/pull/2713)

# New contributors (Thanks!)

TiDB: 

- [shizy](https://github.com/colinback)
- [杨 洋](https://github.com/qxhy123)
