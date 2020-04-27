---
title: Weekly update (April 20 ~ April 26, 2020)
date: 2020-04-27
summary: Last week, we landed 183 PRs in the TiDB repository, 6 PRs in the TiUP repository, 40 PRs in the TiDB Dashboard repository, 5 PRs in the TiSpark repository, and 78 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiUP', 'TiDB Dashboard', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog posts

Last week, we published a post describes how we hacked through different approaches of [clock skew](https://en.wikipedia.org/wiki/Clock_skew#On_a_network) and how TimeChaos in [Chaos Mesh](https://github.com/pingcap/chaos-mesh) enables time to swing freely in containers.

This full post is here:

[Simulating Clock Skew in K8s Without Affecting Other Containers on the Node](https://pingcap.com/blog/simulating-clock-skew-in-k8s-without-affecting-other-containers-on-node/)

Inspired by Google's Key Visualizer, we have implemented Key Visualizer (KeyViz) in TiDB, a distributed, relational, NewSQL database. Key Visualizer displays system status graphically, which helps database administrators (DBAs) quickly troubleshoot database performance issues and enables users to gain deep insights into their applications.

Last week, we published another post that does a deep dive on what Key Visualizer is, how it works, how it can help you, and which scenarios it applies to. If you're a DBA or database developer, we hope you can take this knowledge and apply it to your own work. For example, if you're a developer, you could adopt TiDB and Key Visualizer for your own applications, or even design a similar tool to troubleshoot your system.

The full article is here:

[Key Visualizer: Observe Distributed Databases to Discover the Unknowns](https://pingcap.com/blog/observe-distributed-databases-to-discover-unknowns/)

## Community

### New contributors

tikv:

* [de-sh](https://github.com/de-sh)

docs:

* [terror](https://github.com/terror)

chaos-mesh:

* [wuurrd](https://github.com/wuurrd)
* [rbtcollins](https://github.com/rbtcollins)

## Call for participation

### TiDB

* [To fix the issue that the incorrect result is returned when comparing `NULL` in the integer type column with the float type](https://github.com/pingcap/tidb/issues/16788)
* [To address the issue that the `show grants` statement should contain the privilege information for creating bindings](https://github.com/pingcap/tidb/issues/16749)
* [All help-wanted issues in TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aopen+is%3Aissue+label%3Ahelp-wanted)

### TiKV

* [To always enable the pessimistic transaction](https://github.com/tikv/tikv/issues/7652)
* [To fix the unexpected escape characters in `schedulers-payload`](https://github.com/pingcap/pd/issues/2367)
* [All help-wanted issues in TiKV](https://github.com/tikv/tikv/issues?q=is%3Aopen+is%3Aissue+label%3Astatus%2Fhelp-wanted)
* [All help-wanted issues in PD](https://github.com/pingcap/pd/issues?q=is%3Aissue+is%3Aopen+label%3Astatus%2Fhelp-wanted)

### TiDB Change Data Capture (CDC)

* [All help-wanted issues in TiDB Change Data Capture](https://github.com/pingcap/ticdc/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)

## Updates of the week

### Progress

Last week, we landed [183 PRs](https://github.com/pingcap/tidb/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-04-20..2020-04-26+) in the TiDB repository, [6 PRs](https://github.com/pingcap-incubator/tiup/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-04-20..2020-04-26+) in the TiUP repository, [40 PRs](https://github.com/pingcap-incubator/tidb-dashboard/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-04-20..2020-04-26) in the TiDB Dashboard repository, [5 PRs](https://github.com/pingcap/tispark/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-04-20..2020-04-26+) in the TiSpark repository, and [78 PRs](https://github.com/tikv/tikv/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-04-20..2020-04-26+) in the TiKV and PD repositories.

#### TiDB

* [Fix the issue that an incorrect Region is returned when getting a Region by ID](https://github.com/pingcap/tidb/pull/16793)
* [Enable `update` if the update list does not contain the `view`](https://github.com/pingcap/tidb/pull/16787)
* [Make the `get` function return the `NotExist` error if the key is not found](https://github.com/pingcap/tidb/pull/16771)
* [Fix duplicated lock keys that cause data inconsistency](https://github.com/pingcap/tidb/pull/16752)
* [Support the `auto_random` table option](https://github.com/pingcap/tidb/pull/16750)
* [Add TiFlash in the `cluster_info` table](https://github.com/pingcap/tidb/pull/16684)
* [Fix the issue that two rows are inserted successfully with the same primary key](https://github.com/pingcap/tidb/pull/16672)
* [Fix the potential HTTP connection leak](https://github.com/pingcap/tidb/pull/16656)
* [Build the right range when the `where` clause only has the string column](https://github.com/pingcap/tidb/pull/16645)
* [Fix the privilege check for loading data](https://github.com/pingcap/tidb/pull/16607)
* [Implement the adaptive GC `safePoint`](https://github.com/pingcap/tidb/pull/16550)

#### TiDB Dashboard

* [Support the dynamic configuration in the TiDB Dashboard](https://github.com/pingcap-incubator/tidb-dashboard/pull/377)
* [Show the recent slow queries](https://github.com/pingcap-incubator/tidb-dashboard/pull/424)
* [Add the TiFlash panel](https://github.com/pingcap-incubator/tidb-dashboard/pull/407)
* [Add more columns for statements](https://github.com/pingcap-incubator/tidb-dashboard/pull/399)
* [Add the slow query list and the detail page](https://github.com/pingcap-incubator/tidb-dashboard/pull/398)

#### TiUP

* [Port the static checks used in TiDB](https://github.com/pingcap-incubator/tiup/pull/178)
* [Support upgrading TiFlash](https://github.com/pingcap-incubator/tiup-cluster/pull/330)
* [Add the CDC component](https://github.com/pingcap-incubator/tiup-cluster/pull/320)
* [Support the upgrade from nightly to latest nightly](https://github.com/pingcap-incubator/tiup-cluster/pull/306)

#### TiKV

* [Use the batch split for `auto-split`](https://github.com/tikv/tikv/pull/7654)
* [Check the state after resuming `apply fsm`](https://github.com/tikv/tikv/pull/7612)
* [Write the configuration change to the configuration file](https://github.com/tikv/tikv/pull/7596)
* [Consider the wake-up message when checking stale messages in peer `fsm`](https://github.com/tikv/tikv/pull/7592)
* [Support controlling the replication mode](https://github.com/tikv/tikv/pull/7586)
* [Do not push `min_commit_ts` if `caller_start_ts` is `max u64`](https://github.com/tikv/tikv/pull/7639)

#### PD

* [Unify the HTTP client](https://github.com/pingcap/pd/pull/2368)

#### TiSpark

* [Update the primary key TTL](https://github.com/pingcap/tispark/pull/1409)

## On-going TiDB event

[TiDB Usability Challenge Program](https://pingcap.com/community/tidb-usability-challenge/)
