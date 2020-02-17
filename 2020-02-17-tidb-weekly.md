---
title: Weekly update (February 10 ~ February 16, 2020)
date: 2020-02-17
summary: Last week, we landed 74 PRs in the TiDB repository, 1 PR in the TiSpark repository, and 72 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog posts

Nick Cameron, a PingCAP member, has been working remotely for nearly ten years. Last week, we published two posts in which he introduces why you might benefit from remote work and some of the things that make remote work successful.

The full posts are here:

* [Remote Work - Part 1](https://pingcap.com/blog/remote-work-part-1/)
* [Remote Work - Part 2](https://pingcap.com/blog/remote-work-part-2/)

## Community

### New contributors

parser:

* [zhang555](https://github.com/zhang555)

tidb-binlog:

* [dixingxing0](https://github.com/dixingxing0)

chaos-mesh:

* [yujunz](https://github.com/yujunz)
* [LaumiH](https://github.com/LaumiH)

## Call for participation

* [Issues to solve for TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)
* [Issues to solve for TiKV](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

Last week, we landed [74 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2020-02-10..2020-02-16+) in the TiDB repository, [1 PR](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2020-02-10..2020-02-16) in the TiSpark repository, and [72 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2020-02-10..2020-02-16&type=Issues) in the TiKV and PD repositories.

### Critical PRs

TiDB:

* [Properly support the status port over TLS](https://github.com/pingcap/tidb/pull/14785)
* [Reduce the allocation of requests and responses](https://github.com/pingcap/tidb/pull/14771)
* [Support `leader-and-follower` for `tidb_replica_read`](https://github.com/pingcap/tidb/pull/14761)
* [Set `partitionID` to `tableID` in the DAG request](https://github.com/pingcap/tidb/pull/14745)
* [Add a diagnosis rule to detect critical errors in the cluster](https://github.com/pingcap/tidb/pull/14743)
* [Support the partitioned table in TiFlash](https://github.com/pingcap/tidb/pull/14735)
* [Make `BatchPointGet` support `SELECT` for `UPDATE`](https://github.com/pingcap/tidb/pull/14724)
* [Support loading Regions in batches with the given key range](https://github.com/pingcap/tidb/pull/14716)
* [Add `sync progress` of the TiFlash replica](https://github.com/pingcap/tidb/pull/14713)
* [Add the collation interface](https://github.com/pingcap/tidb/pull/14698)
* [Implement the inline projection for `Joiner` and enable it in `HashJoin`](https://github.com/pingcap/tidb/pull/14682)
* [Support the default expression value for `sequence`](https://github.com/pingcap/tidb/pull/14589)
* [Add the `EliminateOuterJoinBelowAggregation` transformation rule](https://github.com/pingcap/tidb/pull/14465)
* [Introduce a configuration client to support loading configurations from PD online](https://github.com/pingcap/tidb/pull/14303)

TiSpark:

* [Fix the `CHblock` decoding bug for the `int8` or `uint8` type](https://github.com/pingcap/tispark/pull/1383)

TiKV and PD:

* [Fix a panic in `ReadIndexQueue`](https://github.com/tikv/tikv/pull/6609)
* [Make `learner` load the merge target and fix a bug in the network recovery](https://github.com/tikv/tikv/pull/6598)
* [Add the `unified-read-pool` configurations to the configuration template](https://github.com/tikv/tikv/pull/6585)
* [Make `pre-transfer-leader` use `log term` instead of `term`](https://github.com/tikv/tikv/pull/6573)
* [Fix the missing logs by using the `OverflowStrategy::Block` strategy](https://github.com/tikv/tikv/pull/6547)
* [Change the path of the Region Merge flow to fix bugs](https://github.com/tikv/tikv/pull/6481)
* [Speed up the configuration change by sending more heartbeats](https://github.com/tikv/tikv/pull/6432)
* [Remove `pd-web` and `keyvisualService`](https://github.com/pingcap/pd/pull/2121)
