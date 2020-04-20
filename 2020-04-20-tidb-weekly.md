---
title: Weekly update (April 13 ~ April 19, 2020)
date: 2020-04-20
summary: Last week, we landed 163 PRs in the TiDB repository, 14 PRs in the TiSpark repository, and 35 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog post

Last week, we published a post that shares how we use [Backup & Restore (BR)](https://github.com/pingcap/br), a distributed backup and restore tool (that offers high backup and restore speeds—1 GB/s or more for 10 TB of data) to improve backup and restore speeds for large-scale TiDB clusters. If you specialize in database development, this post might inspire your backup and restore design work. If your application deals with huge amounts of data and you also attach great importance to data security and the efficiency of backup and restore, you can try TiDB with BR.

The full article is here:

[How to Back Up and Restore a 10-TB Cluster at 1+ GB/s](https://pingcap.com/blog/back-up-and-restore-a-10-tb-cluster-at-1-gb-per-second/)

## Community

### New contributors

tidb:

* [wangming1993](https://github.com/wangming1993)

pd:

* [AndrewDi](https://github.com/AndrewDi)

docs:

* [sumens](https://github.com/sumens)
* [ChristianLeow](https://github.com/ChristianLeow)

tidb-operator:

* [knightXun](https://github.com/knightXun)

binlog:

* [tsthght](https://github.com/tsthght)

parser:

* [hsqlu](https://github.com/hsqlu)

chaos-mesh:

* [iDube](https://github.com/iDube)

## Call for participation

### TiDB

* [All help-wanted issues in TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aopen+is%3Aissue+label%3Ahelp-wanted)

### TiKV

* [All help-wanted issues in TiKV](https://github.com/tikv/tikv/issues?q=is%3Aopen+is%3Aissue+label%3Astatus%2Fhelp-wanted)
* [All help-wanted issues in PD](https://github.com/pingcap/pd/issues?q=is%3Aissue+is%3Aopen+label%3Astatus%2Fhelp-wanted)

### TiDB Change Data Capture (CDC)

* [All help-wanted issues in TiDB Change Data Capture](https://github.com/pingcap/ticdc/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)

## Updates of the week

### Progress

Last week, we landed [163 PRs](https://github.com/pingcap/tidb/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-04-13..2020-04-19+) in the TiDB repository, [14 PRs](https://github.com/pingcap/tispark/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-04-13..2020-04-19+) in the TiSpark repository, and [35 PRs](https://github.com/tikv/tikv/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-04-13..2020-04-19) in the TiKV and PD repositories.

#### TiDB

* [Set length and frac when changing `0` to the decimal type](https://github.com/pingcap/tidb/pull/16518)
* [Support the partition pruning for the `floor(unix_timestamp())` partition expression](https://github.com/pingcap/tidb/pull/16402)
* [Modify fields related to cop-tasks in the statement summary](https://github.com/pingcap/tidb/pull/16503)
* [Use the single flight to load global variables](https://github.com/pingcap/tidb/pull/16489)
* [Fix the infinite retry when the key-value Region continues to return the `StaleCommand` error](https://github.com/pingcap/tidb/pull/16481)
* [Add `sum_errors` and `sum_warnings` to statement summary tables](https://github.com/pingcap/tidb/pull/16456)
* [Do not eliminate the innermost `NOT` when pushing down `NOT`](https://github.com/pingcap/tidb/pull/16451)
* [Fix the issue that the outer join cannot be simplified if a predicate just refers to the outer table](https://github.com/pingcap/tidb/pull/16444)
* [Fix the issue that the default value of a sequence causes the `not-null` error in the primary key](https://github.com/pingcap/tidb/pull/16437)
* [Unify the style for storage quota configuration names](https://github.com/pingcap/tidb/pull/16431)
* [Fix the issue that generated columns might cause a server crash](https://github.com/pingcap/tidb/pull/16376)
* [Fix the issue that the GC Worker stops working after a GC failure](https://github.com/pingcap/tidb/pull/16372)
* [Fix the `group by` resolver for multiple items with the parameter marker](https://github.com/pingcap/tidb/pull/16363)
* [Remove the `enable-dynamic-config` configuration item](https://github.com/pingcap/tidb/pull/16358)
* [Push `avg` and `distinct` functions across unions](https://github.com/pingcap/tidb/pull/16344)
* [Add the check for the expression evaluation in some executors](https://github.com/pingcap/tidb/pull/16339)
* [Forbid truncating the view](https://github.com/pingcap/tidb/pull/16251)
* [Refactor the code for multiple statements in one query](https://github.com/pingcap/tidb/pull/16056)
* [Add the `EnableCollectExecutionInfo` configuration item](https://github.com/pingcap/tidb/pull/15493)

#### TiDB Dashboard

* [Fix the incorrect Placement Driver (PD) TSO duration in the report](https://github.com/pingcap-incubator/tidb-dashboard/pull/343)
* [Filter statements by SQL types](https://github.com/pingcap-incubator/tidb-dashboard/pull/354)
* [Refine the page head of statements](https://github.com/pingcap-incubator/tidb-dashboard/pull/353)
* [Add more node information and reorder the time consumption item](https://github.com/pingcap-incubator/tidb-dashboard/pull/365)

#### TiUP

* The tiup-cluster v0.4.9 is released.

#### TiKV

* [Fix the batch empty request deadlock](https://github.com/tikv/tikv/pull/7535)
* [Fix `make docker`](https://github.com/tikv/tikv/pull/7498)
* [Check the state after resuming applying `fsm`](https://github.com/tikv/tikv/pull/7444)
* [Fix the wrong key being read on ingested files with global `seqno` and delta encoding](https://github.com/tikv/tikv/pull/7420)
* [Consider waking up messages when checking stale messages](https://github.com/tikv/tikv/pull/7416)
* [Support the encryption in snapshots](https://github.com/tikv/tikv/pull/7403)

#### PD

* [Fix the panic in the hot Region scheduler](https://github.com/pingcap/pd/pull/2353)
* [Re-implement the dynamic configuration](https://github.com/pingcap/pd/pull/2349)

#### TiSpark

* [Support TiDB 4.0](https://github.com/pingcap/tispark/pull/1391)

## On-going TiDB event

[TiDB Usability Challenge Program](https://pingcap.com/community/tidb-usability-challenge/)
