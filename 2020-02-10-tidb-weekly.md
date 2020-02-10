---
title: Weekly update (February 03 ~ February 09, 2020)
date: 2020-02-10
summary: Last week, we landed 64 PRs in the TiDB repository, 3 PRs in the TiSpark repository, and 33 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog post

In [TiDB 3.1 Beta](https://pingcap.com/docs/v3.1/releases/3.1.0-beta/) released on Dec 20, 2019, TiDB introduced Follower Read, a highlight open-source feature that lets any follower replica in a Region serve a read request under the premise of strongly consistent reads. This feature improves the throughput of the TiDB cluster and reduces the load on the Raft leader.

Last week, we published a post that guides you through why we introduced Follower Read, how we implement it, and our future plans for it.

The full post is here:

[Doubling System Read Throughput with Only 26 Lines of Code](https://pingcap.com/blog/doubling-system-read-throughput-with-only-26-lines-of-code/)

## Community

### New contributors

tidb:

* [hg2990656](https://github.com/hg2990656)

tikv:

* [xinhua5](https://github.com/xinhua5)

## Call for participation

* [Issues to solve for TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)
* [Issues to solve for TiKV](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

Last week, we landed [64 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2020-02-03..2020-02-09+) in the TiDB repository, [3 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2020-02-03..2020-02-09) in the TiSpark repository, and [33 PRs](https://github.com/search?p=1&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2020-02-03..2020-02-09&type=Issues) in the TiKV and PD repositories.

### Critical PRs

TiDB:

* [Fully Enable the `CAST` push-down switcher](https://github.com/pingcap/tidb/pull/14672)
* [Cache the `point get` result](https://github.com/pingcap/tidb/pull/14669)
* [Fix the issue that `lower()`/`upper()` does not work if a string contains the `utf8` character](https://github.com/pingcap/tidb/pull/14667)
* [Merge overlapped ranges when building key ranges for `indexJoin`](https://github.com/pingcap/tidb/pull/14596)
* [Support recording the rejected connection attempts in the audit log](https://github.com/pingcap/tidb/pull/14594)
* [Update `information_schema`.`tables` to support `AUTO_RANDOM`](https://github.com/pingcap/tidb/pull/14583)
* [Add the implementation rule for `LogicalMemTable` in the cascades planner](https://github.com/pingcap/tidb/pull/14577)
* [Add TiKV metric tables](https://github.com/pingcap/tidb/pull/14498)
* [Improve the concurrency of statement summary](https://github.com/pingcap/tidb/pull/14490)
* [Count the number of Hash table collisions and build `Elapse` during `Hash Join`](https://github.com/pingcap/tidb/pull/14423)
* [Improve the performance of `WindowExec` by using the sliding window](https://github.com/pingcap/tidb/pull/14294)
* [Add the built-in `json_objectagg` aggregate function](https://github.com/pingcap/tidb/pull/11154)

TiSpark:

* [Fix the `CHblock` decoding bug](https://github.com/pingcap/tispark/pull/1382)
* [Enable the key ranges for the TiFlash dag request](https://github.com/pingcap/tispark/pull/1381)
* [Fix the TiFlash Region cache](https://github.com/pingcap/tispark/pull/1380)

TiKV and PD:

* [Fix builds on macOS](https://github.com/tikv/tikv/pull/6510)
* [Fix the issue that the `yyyy-mm-dd HH:MM:SS` format cannot be parsed to `Duration`](https://github.com/tikv/tikv/pull/6492)
* [Introduce the Pre-transfer Leader feature](https://github.com/tikv/tikv/pull/6539)
* [Support `Yield` for `apply`](https://github.com/tikv/tikv/pull/6487)
* [Add a benchmark for the batch system](https://github.com/tikv/tikv/pull/6477)
* [Add the CDC delegate](https://github.com/tikv/tikv/pull/6522)
* [Implement `Initializer` of CDC's `Endpoint`](https://github.com/tikv/tikv/pull/6490)
* [Optimize `ChunkEncoder`](https://github.com/tikv/tikv/pull/6341)
* [Support backing up the raw key-value pairs](https://github.com/tikv/tikv/pull/6308)
* [Store the placement rules in separated key-values pairs](https://github.com/pingcap/pd/pull/2098)
* [Add `operator Influence` when sorting stores](https://github.com/pingcap/pd/pull/2090)
* [Make the original HTTP API compatible with the configuration manager](https://github.com/pingcap/pd/pull/2080)

## Upcoming TiDB event

Infra Meetup No.124 (online)

Date: February 15th, 2020
