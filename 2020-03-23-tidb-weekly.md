---
title: Weekly update (March 16 ~ March 22, 2020)
date: 2020-03-23
summary: Last week, we landed 85 PRs in the TiDB repository and 66 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog post

[Chaos Mesh](https://github.com/pingcap/chaos-mesh) is an easy-to-use, open-source, cloud-native Chaos Engineering platform that orchestrates chaos in Kubernetes environments. Last week, we published a 10-minute tutorial that will help you quickly get started with Chaos Engineering and run your first chaos experiment with Chaos Mesh.

The full article is here:

[Run Your First Chaos Experiment in 10 Minutes](https://pingcap.com/blog/run-first-chaos-experiment-in-ten-minutes/)

## Community

### New contributors

tidb:

* [LindaSummer](https://github.com/LindaSummer)
* [stoksc](https://github.com/stoksc)

pd:

* [Sullivan12138](https://github.com/Sullivan12138)

docs-cn:

* [SE-Bin](https://github.com/SE-Bin)

## Call for participation

### TiDB

* [Control the concurrency of all types of executors in one session variable](https://github.com/pingcap/tidb/issues/15428)
* [Use <kbd>space</kbd> instead of <kbd>Tab</kbd> in the `events_statements_summary_by_digest.plan` field](https://github.com/pingcap/tidb/issues/15502)

### TiKV

* [Support the slow query log searching](https://github.com/tikv/tikv/issues/7069)
* [Optimize the performance of Coprocessor Analyze](https://github.com/tikv/tikv/issues/7039)
* [All help-wanted issues in TiKV](https://github.com/tikv/tikv/issues?q=is%3Aopen+is%3Aissue+label%3Astatus%2Fhelp-wanted)

### TiDB Dashboard

* [Add a refresh button in the statement overview page](https://github.com/pingcap-incubator/tidb-dashboard/issues/273)
* [Improve build packages](https://github.com/pingcap-incubator/tidb-dashboard/issues/269)
* [Update to React Router v6](https://github.com/pingcap-incubator/tidb-dashboard/issues/249)
* [Try to switch to react-spring](https://github.com/pingcap-incubator/tidb-dashboard/issues/234)
* [Refine log searching models](https://github.com/pingcap-incubator/tidb-dashboard/issues/228)
* [Avoid the screen flash when the session times out](https://github.com/pingcap-incubator/tidb-dashboard/issues/227)
* [Support overriding the TiDB node to the request](https://github.com/pingcap-incubator/tidb-dashboard/issues/224)

### TiDB Backup & Restore (BR)

* [Add the backup retry when some TiKV nodes get down](https://github.com/pingcap/br/issues/192)
* [All help-wanted issues in TiDB Backup & Restore](https://github.com/pingcap/br/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)

### TiDB Change Data Capture (CDC)

* [Refine the log and the standard output (stdout) of the CDC `cli` tool](https://github.com/pingcap/ticdc/issues/343)
* [All help-wanted issues in TiDB Change Data Capture](https://github.com/pingcap/ticdc/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)

## Updates of the week

### Progress

Last week, we landed [85 PRs](https://github.com/pingcap/tidb/search?q=is%3Apr+is%3Amerged+merged%3A2020-03-16..2020-03-22&unscoped_q=is%3Apr+is%3Amerged+merged%3A2020-03-16..2020-03-22&type=Issues) in the TiDB repository and [66 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2020-03-16..2020-03-22&type=Issues) in the TiKV and PD repositories.

#### TiDB

* [Forbid changing the column collation in some cases](https://github.com/pingcap/tidb/pull/15562)
* [Add the `explain` information for `ClusterLogTableExtractor`](https://github.com/pingcap/tidb/pull/15542)
* [Add a switch to decide whether to capture internal queries](https://github.com/pingcap/tidb/pull/15461)

#### TiDB Dashboard

* [Fix the issue that the log searching component selector is too short](https://github.com/pingcap-incubator/tidb-dashboard/pulls?q=is%3Apr+is%3Aclosed)
* [Fix a `select` and `zoom` bug in Key Visualizer](https://github.com/pingcap-incubator/tidb-dashboard/pull/246)

#### TiUP

* [Support specifying `GOOS` and `GOARCH`](https://github.com/pingcap-incubator/tiup/pull/75)
* [Refactor the TiUP API and make its reuse easier by the external component](https://github.com/pingcap-incubator/tiup/pull/72)
* Progress of New TiOPS development: 35% completed

#### TiKV

* [Support `apply` on Raftstore](https://github.com/tikv/tikv/pull/6154)
* [Support TLS for the status server](https://github.com/tikv/tikv/pull/5393)
* [Fix a panic of read index during the leader transfer](https://github.com/tikv/tikv/pull/7101)
* [Abstract more Raftstore over `engine_traits`](https://github.com/tikv/tikv/pull/7032)
* [Optimize the batch system for the better pipeline work](https://github.com/tikv/tikv/pull/6991)
* [Support the encryption at rest](https://github.com/tikv/tikv/pull/6990)
* [Use multi-batch-write for `apply`](https://github.com/tikv/tikv/pull/7111)

#### PD

* Fix the race and panic bugs on Syncer [#2236](https://github.com/pingcap/pd/pull/2236) [#2256](https://github.com/pingcap/pd/pull/2256)
* [Parameterize the hotspot scheduling and adjust the hot cache](https://github.com/pingcap/pd/pull/2239)

## On-going TiDB event

[TiDB Usability Challenge Program](https://pingcap.com/community/tidb-usability-challenge/)
