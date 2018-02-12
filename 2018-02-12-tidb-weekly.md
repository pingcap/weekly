---
title: Weekly update (February 05 ~ February 11, 2018)
date: 2018-02-12
summary: Last week, we landed 67 PRs in the TiDB repositories, 6 PRs in the TiSpark repositories, and 19 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [67 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is:pr+is:merged+merged:2018-02-05..2018-02-11) in the TiDB repositories.

## Added

* [`CreateIndex` supports the LOCK option.](https://github.com/pingcap/tidb/pull/5851)
* [Add `GoVersion` info for `tidb_version`](https://github.com/pingcap/tidb/pull/5828)
* [Add a session variable to show the configuration](https://github.com/pingcap/tidb/pull/5784)
* [Support `show stats_healthy` to check if a table needs to be analyzed](https://github.com/pingcap/tidb/pull/5769) 

## Removed

* [Remove the useless field in `jsonColumn`](https://github.com/pingcap/tidb/pull/5813)
* [Clean up the abandoned storage engine](https://github.com/pingcap/tidb/pull/5808)                                                                             

## Fixed

* [Check the `CreateTable` statement charset option](https://github.com/pingcap/tidb/pull/5835)
* [Fix the bug of `show index` printing non-public index when `add index` operation is not finished](https://github.com/pingcap/tidb/pull/5833)
* [Treat a decimal truncate as a warning in update](https://github.com/pingcap/tidb/pull/5801)

## Improved

* [Run GC workers parallelly](https://github.com/pingcap/tidb/pull/5837)
* [Pass the operator label from `Plan` to `Executor`](https://github.com/pingcap/tidb/pull/5821)
* [Prepare the candidate index to improve performance](https://github.com/pingcap/tidb/pull/5809)
* [Use pseudo estimation when the stats of some table is outdated](https://github.com/pingcap/tidb/pull/5802)
* [Ignore the error and keep GC always working](https://github.com/pingcap/tidb/pull/5797)
* [Set a min count for `AutoAnalyze` to avoid the auto analysis of small tables](https://github.com/pingcap/tidb/pull/5796)
* Improve importer tools:
    - [Support `randDate` by statistics](https://github.com/pingcap/tidb/pull/5830)
    - [Support generating other types of columns randomly by statistics](https://github.com/pingcap/tidb/pull/5848)
    - [Generate a string by statistics](https://github.com/pingcap/tidb/pull/5804)
    - [Support VARCHAR in set](https://github.com/pingcap/tidb/pull/5800)
    - [Generate the integer data by `Histogram`](https://github.com/pingcap/tidb/pull/5795)
* Refine metrics in TiDB:
    - [Rename `_count` to `_num`](https://github.com/pingcap/tidb/pull/5868)
    - [Unify metrics naming](https://github.com/pingcap/tidb/pull/5863)
    - [Add a metric for pseudo estimation](https://github.com/pingcap/tidb/pull/5861)
    - [Make metrics content clearer and compacter](https://github.com/pingcap/tidb/pull/5858)
    - [Move domain metrics and add the privilege load counter](https://github.com/pingcap/tidb/pull/5855)
    - [Add metrics for DDL and the server](https://github.com/pingcap/tidb/pull/5840)
    - [Add metrics for the DDL worker](https://github.com/pingcap/tidb/pull/5823)
    - [Add metrics for expensive executors and statement nodes](https://github.com/pingcap/tidb/pull/5798)
    - [Add metrics for stats](https://github.com/pingcap/tidb/pull/5785)
    - [Fix inconsistent labels for the panic counter](https://github.com/pingcap/tidb/pull/5783)
    - [Move DDL metrics from the ddl package to the metrics package](https://github.com/pingcap/tidb/pull/5781)
    - [Refine TiKV client metrics](https://github.com/pingcap/tidb/pull/5780)
    - [Add metrics for the DDL owner](https://github.com/pingcap/tidb/pull/5779/files)
    - [Add metrics and logs for `ticlient`](https://github.com/pingcap/tidb/pull/5778)

# Weekly update in TiSpark

Last week, we landed [19 PRs](https://github.com/search?q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-02-05..2018-02-11) in the TiKV and PD repositories.

## Improved

* [Change the remote repository for the test data](https://github.com/pingcap/tispark/pull/242)
* [Add JDBC write guide usage](https://github.com/pingcap/tispark/pull/238)

## Fixed

* [Fix key range corner cases](https://github.com/pingcap/tispark/pull/240)
* [Fix the bug of `group by` without aggregates](https://github.com/pingcap/tispark/pull/237)
* [Fix the `resetFilters` method](https://github.com/pingcap/tispark/pull/236)
* [Fix the character decoding charset](https://github.com/pingcap/tispark/pull/235)

# Weekly update in TiKV and PD

Last week, we landed [19 PRs](https://github.com/search?q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-02-05..2018-02-11) in the TiKV and PD repositories.

## Added

* [Add the read pool](https://github.com/pingcap/tikv/pull/2699)
* [Introduce the label property and the label scheduler](https://github.com/pingcap/pd/pull/946)
* [Support the config label scheduler and label property](https://github.com/pingcap/pd/pull/948)

## Fixed

* [Fix the bug caused by `limit=0` or by no limit](https://github.com/pingcap/tikv/pull/2744)

## Improved

* [Add the file name and the line number for the box error](https://github.com/pingcap/tikv/pull/2741)
* [Record the leader missing information](https://github.com/pingcap/tikv/pull/2730)
* [Filter `Store` when counting the average leader and score](https://github.com/pingcap/pd/pull/949)
* [Add `stale_command` in `ASYNC_REQUESTS_COUNTER_VEC`](https://github.com/pingcap/tikv/pull/2745)
* [Check whether `range.start` < `range.end`](https://github.com/pingcap/tikv/pull/2752)
* [Change the unit of heartbeat from `ts` to `ms`](https://github.com/pingcap/pd/pull/950)
* [Limit the maximum total size of snapshot](https://github.com/pingcap/tikv/pull/2632)
* [Collect gRPC logs](https://github.com/pingcap/tikv/pull/2756)
* [Save the critical metadata in metrics](https://github.com/pingcap/pd/pull/955)
* [Use local metrics](https://github.com/pingcap/tikv/pull/2647)
* [Adjust the status of the store](https://github.com/pingcap/pd/pull/953)

# New contributor (Thanks!)

* TiDB: [Cruth kvinc](https://github.com/oiooj)