---
title: Weekly update (December 16 ~ December 22, 2019)
date: 2019-12-23
summary: Last week, we landed 85 PRs in the TiDB repository, 4 PRs in the TiSpark repository, and 67 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog post

Don't wanna spend forever trying to locate bugs in massive code? Take a look at a bot built at TiDB Hackathon 2019 - it can automatically find faults in the code!

The full article is here:

[Squashed Bugs, Served Hot and Fresh with Failure Rate Heatmaps](https://pingcap.com/blog/squashed-bugs-served-hot-and-fresh-with-failure-rate-heatmaps/)

## Community

### New contributors

tidb:

* [Aloxaf](https://github.com/Aloxaf)
* [jiangyuzhao](https://github.com/jiangyuzhao)

tikv:

* [zhangmoon](https://github.com/zhangmoon)
* [chacha923](https://github.com/chacha923)
* [zhang555](https://github.com/zhang555)

tidb-operator:

* [mikechengwei](https://github.com/mikechengwei)

## Call for participation

* Coprocessor SIG:
    * [Improve the performance of Chunk Encoder](https://github.com/tikv/tikv/issues/5729)
    * [Implement more UDFs](https://github.com/tikv/tikv/issues/5727)
    * [Implement the new row format](https://github.com/tikv/tikv/issues/5726)
    * [Port `BinaryJSON`](https://github.com/tikv/tikv/issues/5715)
    * [Tracing](https://github.com/tikv/tikv/issues/5714)
    * [The maximum execution time of Per-request](https://github.com/tikv/tikv/issues/5712)

* [More issues to solve for TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)
* [More issues to solve for TiKV](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

Last week, we landed [85 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-12-16..2019-12-22+) in the TiDB repository, [4 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-12-16..2019-12-22+) in the TiSpark repository, and [67 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-12-16..2019-12-22&type=Issues) in the TiKV and PD repositories.

### Critical PRs

TiDB:

* [Add three fields to the statement summary table in `Infoschema`](https://github.com/pingcap/tidb/pull/14096)
* [Add `ImplementationRule` for `Window` in the cascades planner](https://github.com/pingcap/tidb/pull/14085)
* [Add the index progress metrics in the DDL operation](https://github.com/pingcap/tidb/pull/14055)
* [Check the foreign key constraint when dropping, modifying, and changing columns](https://github.com/pingcap/tidb/pull/14043)
* [Support enabling or disabling the slow log by variables](https://github.com/pingcap/tidb/pull/14016)
* [Trace the memory usage of `projection` executors](https://github.com/pingcap/tidb/pull/13914)
* [Add the basic support for hidden columns](https://github.com/pingcap/tidb/pull/13908)

TiSpark:

* [Fix the `DESC` temp view](https://github.com/pingcap/tispark/pull/1323)
* [Rewrite the `get` decimal from `Chunk`](https://github.com/pingcap/tispark/pull/1318)

TiKV and PD:

* [Fix the issue that the `load` cluster does not remove overlapping Regions](https://github.com/pingcap/pd/pull/2022)
* [Fix the panic caused by removing the tombstone](https://github.com/pingcap/pd/pull/2015)
* [Support adding gRPC dial options](https://github.com/pingcap/pd/pull/2035)
* [Add the diagnostics service](https://github.com/pingcap/pd/pull/2024)
* [Add the pluggable PD scheduler](https://github.com/pingcap/pd/pull/1799)
* [Support the incremental backup](https://github.com/tikv/tikv/pull/6222)

## Upcoming TiDB events

* [Infra Meetup No.122 (in Chinese)](https://github.com/pingcap/meetup/)

    Date: December 28th, 2019

* [Infra Meetup No.123 (in Chinese)](https://github.com/pingcap/meetup/)

    Date: December 28th, 2019
