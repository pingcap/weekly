---
title: Weekly update (April 27 ~ May 03, 2020)
date: 2020-05-06
summary: Last week, we landed 84 PRs in the TiDB repository, 2 PRs in the TiUP repository, 11 PRs in the TiDB Dashboard repository, 3 PRs in the TiSpark repository, and 53 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiUP', 'TiDB Dashboard', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog posts

Last week, we published an article that goes over how to build and run your own TiDB or TiKV, and how to run some benchmarks on those databases. The full article is here:

[Building, Running, and Benchmarking TiKV and TiDB](https://pingcap.com/blog/building-running-and-benchmarking-tikv-and-tidb/)

Last week, we also published an article that introduces TiUP, a component manager introduced in TiDB v4.0 that streamlines installing and configuring a TiDB cluster into a few easy commands. With TiUP, you can get your cluster up in just one minute. The full article is here:

[Get a TiDB Cluster Up in Only One Minute](https://pingcap.com/blog/get-tidb-cluster-up-in-only-one-minute/)

## Community

### New contributors

tikv:

* [crodjer](https://github.com/crodjer)

## Call for participation

### TiDB

* [To fix the issue that the `table not exist` error code in the release-3.0 branch is not the same as that in the master branch](https://github.com/pingcap/tidb/issues/16980)
* [Remove the default `asc` order in the `explain` result](https://github.com/pingcap/tidb/issues/16974)
* [All help-wanted issues in TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aopen+is%3Aissue+label%3Ahelp-wanted)

### TiKV

* [Add metrics for channels of `peer fsm` and `apply fsm`](https://github.com/tikv/tikv/issues/7686)
* [All help-wanted issues in TiKV](https://github.com/tikv/tikv/issues?q=is%3Aopen+is%3Aissue+label%3Astatus%2Fhelp-wanted)
* [All help-wanted issues in PD](https://github.com/pingcap/pd/issues?q=is%3Aissue+is%3Aopen+label%3Astatus%2Fhelp-wanted)

### TiDB Change Data Capture (CDC)

* [All help-wanted issues in TiDB Change Data Capture](https://github.com/pingcap/ticdc/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)

## Updates of the week

### Progress

Last week, we landed [84 PRs](https://github.com/pingcap/tidb/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-04-27..2020-05-03) in the TiDB repository, [2 PRs](https://github.com/pingcap-incubator/tiup/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-04-27..2020-05-03+) in the TiUP repository, [11 PRs](https://github.com/pingcap-incubator/tidb-dashboard/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-04-27..2020-05-03+) in the TiDB Dashboard repository, [3 PRs](https://github.com/pingcap/tispark/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-04-27..2020-05-03+) in the TiSpark repository, and [53 PRs](https://github.com/tikv/tikv/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-04-27..2020-05-03+) in the TiKV and PD repositories.

#### TiDB

* [Fix the panic issue that occurs when executing the `PointGet` query after the `delete` operation](https://github.com/pingcap/tidb/pull/16965)
* [Support the `BACKUP` and `RESTORE` statements in RFC](https://github.com/pingcap/tidb/pull/15274)
* [Pre-split Regions during 2PC to avoid the hotspot problem](https://github.com/pingcap/tidb/pull/16920)
* [Prevent the subquery expression in the `values` clause from referencing the upper scope to parse the column name when the table name is not specified for `insert` statements](https://github.com/pingcap/tidb/pull/16872)
* [Compare locks by keys and timestamps](https://github.com/pingcap/tidb/pull/16536)
* [Generalize `SHOW TABLE t NEXT_ROW_ID` for `auto_random` and sequences](https://github.com/pingcap/tidb/pull/16821)
* [Collapse the duplicate resolved locks in Region requests](https://github.com/pingcap/tidb/pull/16838)
* [Add the brief RFC about TiDB sequence](https://github.com/pingcap/tidb/pull/16682)

#### TiDB Dashboard

* [Support auto-collection](https://github.com/pingcap-incubator/tidb-dashboard/pull/439)
* [Add the support for searching TiKV slow logs](https://github.com/pingcap-incubator/tidb-dashboard/pull/392)
* [Integrate statements and slow queries](https://github.com/pingcap-incubator/tidb-dashboard/pull/437)
* [Support TiFlash](https://github.com/pingcap-incubator/tidb-dashboard/pull/434)

#### TiUP

* [Add translated user documents](https://github.com/pingcap-incubator/tiup/pull/185)

#### TiKV

* [Fix the `multi-batch-write` bug](https://github.com/tikv/tikv/pull/7640)
* [Enable the hard link check on all Unix systems](https://github.com/tikv/tikv/pull/7696/files)

#### PD

* [Update `kvproto` to `#605` which changes the `binary` path to the `deploy` path](https://github.com/pingcap/pd/pull/2383)

#### TiSpark

* [Fix the bug that the table is not found](https://github.com/pingcap/tispark/pull/1416)

## On-going TiDB event

[TiDB Usability Challenge Program](https://pingcap.com/community/tidb-usability-challenge/)
