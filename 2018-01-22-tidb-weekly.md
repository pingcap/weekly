---
title: Weekly update (January 15 ~ January 21, 2018)
date: 2018-01-22
summary: Last week, we landed 43 PRs in the TiDB repositories, 13 PRs in the TiSpark repositories, and 18 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [43 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is:pr+is:merged+merged:2018-01-15..2018-01-21) in the TiDB repositories.

## Added

* [Add an interface for `Chunk` to count the memory usage](https://github.com/pingcap/tidb/pull/5645)
* [Add a session variable to log the query string](https://github.com/pingcap/tidb/pull/5633)

## Removed

* [Remove the old, never used `IndexLookUpJoin`](https://github.com/pingcap/tidb/pull/5649)

## Fixed

* [`group_concat` should not modify the argument during execution](https://github.com/pingcap/tidb/pull/5664)
* [Correct the unsigned `pk`'s behavior](https://github.com/pingcap/tidb/pull/5641)

## Improved

* [Optimize the `com_field_list` command and make `Use Database` faster](https://github.com/pingcap/tidb/pull/5677)
* [Improve the sort efficiency on `lookupTableTask.rows`](https://github.com/pingcap/tidb/pull/5675)
* [Enlarge the default `distsql_scan_concurrency`](https://github.com/pingcap/tidb/pull/5670)
* [Log a warning when the memory usage of `HashJoinExec` exceeds threshhold](https://github.com/pingcap/tidb/pull/5658)
* [Refine the behavior when updating `StatsDelta`](https://github.com/pingcap/tidb/pull/5647)
* [Split the presentation and evaluation layers of aggregation functions](https://github.com/pingcap/tidb/pull/5635)
* [Use `BatchGet` to speed up `LOAD DATA`](https://github.com/pingcap/tidb/pull/5632)

# Weekly update in TiSpark

Last week, we landed [13 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-01-15..2018-01-21) in the TiSpark repositories.

## Improved

* [Refactor the type and expression systems totally](https://github.com/pingcap/tispark/pull/197)
  * Reorganize the type and expressions
  * Use the visitor instead of raw expressions when processing traversal
  * Fixed `type infer` logics
  * Refactor predicates processing logic according to the visitor pattern
  * Fixed index encoding
* [Change `CodecDataInput` to use non-synchronized `ByteArrayInputStream`](https://github.com/pingcap/tispark/pull/214)
* [Add TiKV, PD, and TiDB's config files for Docker test environment](https://github.com/pingcap/tispark/pull/216)

# Weekly update in TiKV and PD

Last week, we landed [18 PRs](https://github.com/search?q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-01-15..2018-01-21) in the TiKV and PD repositories.

## Added

* [simulator: add hot region cases](https://github.com/pingcap/pd/pull/909)

## Fixed

* [proto: compatible with proto3](https://github.com/pingcap/pd/pull/919)
* [heartbeat: rebind the stream](https://github.com/pingcap/pd/pull/918)
* [server: delete overlap from etcd](https://github.com/pingcap/pd/pull/925)

## Improved

* [Refactor the raftstore Callback API](https://github.com/pingcap/tikv/pull/2625)
* [Remove the unused `rocksdb.backup_dir`](https://github.com/pingcap/tikv/pull/2697)
* [Adjust Scheduler metrics](https://github.com/pingcap/tikv/pull/2700)
* [`impl Runnable` for Scheduler](https://github.com/pingcap/tikv/pull/2672)