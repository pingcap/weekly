---
title: Weekly update (January 13 ~ January 19, 2020)
date: 2020-01-20
summary: Last week, we landed 43 PRs in the TiDB repository, 11 PRs in the TiSpark repository, and 24 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog post

In the world of distributed computing, faults can happen to your clusters unpredictably any time, anywhere. Therefore, we present to you Chaos Mesh, a cloud-native Chaos Engineering platform that orchestrates chaos experiments on Kubernetes environments. Last week, we published a post that introduces what Chaos Mesh is, how we design and implement it, and finally how you can use it in your environment.

The full post is here:

[Chaos Mesh - Your Chaos Engineering Solution for System Resiliency on Kubernetes](https://pingcap.com/blog/chaos-mesh-your-chaos-engineering-solution-for-system-resiliency-on-kubernetes/)

## Community

### New contributors

docs-cn:

* [ran-huang](https://github.com/ran-huang)

tidb-operator:

* [longfangsong](https://github.com/longfangsong)

parser:

* [zhaox1n](https://github.com/zhaox1n)
* [hg2990656](https://github.com/hg2990656)

tidb-binlog:

* [freemindLi](https://github.com/freemindLi)

## Call for participation

* [Issues to solve for TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)
* [Issues to solve for TiKV](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

Last week, we landed [43 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2020-01-13..2020-01-19+) in the TiDB repository, [11 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2020-01-13..2020-01-19+) in the TiSpark repository, and [24 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2020-01-13..2020-01-19&type=Issues) in the TiKV and PD repositories.

### Critical PRs

TiDB:

* [Add the data accessibility check for `point get`](https://github.com/pingcap/tidb/pull/14459)
* [Add `ImplementationRule` for `MergeJoin` in the cascades planner](https://github.com/pingcap/tidb/pull/14450)
* [Add a server-level configuration to control `IsolationRead`](https://github.com/pingcap/tidb/pull/14440)
* [Support limiting the number of client connections](https://github.com/pingcap/tidb/pull/14409)
* [Fix the bug occurred when inserting partitioned tables caused by the timezone change](https://github.com/pingcap/tidb/pull/14370)
* [Improve the performance of `WindowExec` by using the multi-thread hash grouping](https://github.com/pingcap/tidb/pull/14238)

TiSpark:

* [Fix the issue that the partitioned table is not shown in `ShowCommand`](https://github.com/pingcap/tispark/pull/1354)

TiKV and PD:

* [Fix the inconsistency with TiDB when the `CAST` function converts the binary string to `int`](https://github.com/tikv/tikv/pull/6463)
* [Support getting the configuration in use through the status server](https://github.com/tikv/tikv/pull/6480)
* [Fix the inconsistency with TiDB when parsing `Duration` from a string](https://github.com/tikv/tikv/pull/6474)
* [Integrate the dashboard into PD](https://github.com/pingcap/pd/pull/2086)
* [Fix the issue that `enable-placement-rules` cannot be set twice](https://github.com/pingcap/pd/pull/2102)
* [Do not build the dashboard UI on Windows](https://github.com/pingcap/pd/pull/2105)
