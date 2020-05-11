---
title: Weekly update (May 04 ~ May 10, 2020)
date: 2020-05-11
summary: Last week, we landed 63 PRs in the TiDB repository, 2 PRs in the TiUP repository, 18 PRs in the TiDB Dashboard repository, 7 PRs in the TiSpark repository, and 16 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiUP', 'TiDB Dashboard', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog post

Last week, we published an article that goes over how to build and run your own TiDB or TiKV, and how to run some benchmarks on those databases. The full article is here:

[Building, Running, and Benchmarking TiKV and TiDB](https://pingcap.com/blog/building-running-and-benchmarking-tikv-and-tidb/)

TiDB 4.0 introduces SQL Plan Management (SPM), a mechanism that narrows down the optimizer's searching space to execution plans that are proven to perform well. SPM avoids performance degradation caused by unanticipated plan changes, and you don't have to change the application code.

Last week, we published an article that gives an overview of SPM and use an example to demonstrate how SPM helps the optimizer automatically select efficient execution plans.

The full article is here:

[SQL Plan Management: Never Worry About Slow Queries Again](https://pingcap.com/blog/sql-plan-management-never-worry-about-slow-queries-again/)

## Community

### New contributors

docs:

* [Hangzhi](https://github.com/Hangzhi)

docs-cn:

* [glkappe](https://github.com/glkappe)

tidb-operator:

* [PengJi](https://github.com/PengJi)

## Call for participation

### TiDB

* [To remove the default `asc` order in `explain` result](https://github.com/pingcap/tidb/issues/16974)
* [To fix the issue that the `table not exist` error code in release-3.0 is not the same as that in master](https://github.com/pingcap/tidb/issues/16980)
* [To fix the issue that the `TestBuiltin` unit test fails in different timezones](https://github.com/pingcap/tidb/issues/17013)
* [To print SQL statements for the Out Of Memory (OOM) quota](https://github.com/pingcap/tidb/issues/17043)
* [To evaluate aggregate functions in parallel with `distinct` in `hashAgg`](https://github.com/pingcap/tidb/issues/17075)
* [All help-wanted issues in TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aopen+is%3Aissue+label%3Ahelp-wanted)

### TiKV

* [All help-wanted issues in TiKV](https://github.com/tikv/tikv/issues?q=is%3Aopen+is%3Aissue+label%3Astatus%2Fhelp-wanted)
* [All help-wanted issues in PD](https://github.com/pingcap/pd/issues?q=is%3Aissue+is%3Aopen+label%3Astatus%2Fhelp-wanted)

### TiDB Change Data Capture (CDC)

* [All help-wanted issues in TiDB Change Data Capture](https://github.com/pingcap/ticdc/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)

## Updates of the week

### Progress

Last week, we landed [63 PRs](https://github.com/pingcap/tidb/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-05-04..2020-05-10) in the TiDB repository, [2 PRs](https://github.com/pingcap-incubator/tiup/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-05-04..2020-05-10+) in the TiUP repository, [18 PRs](https://github.com/pingcap-incubator/tidb-dashboard/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-05-04..2020-05-10+) in the TiDB Dashboard repository, [7 PRs](https://github.com/pingcap/tispark/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-05-04..2020-05-10+) in the TiSpark repository, and [16 PRs](https://github.com/tikv/tikv/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-05-04..2020-05-10+) in the TiKV and PD repositories.

#### TiDB

* [Fix the issue that the bootstrap SQL statements are not treated as internal queries in the statement summary](https://github.com/pingcap/tidb/pull/17024)
* [Add a proposal document for the clustered index feature](https://github.com/pingcap/tidb/pull/17044)
* [Fix the wrong plan type for the `dataReaderBuilder` error](https://github.com/pingcap/tidb/pull/17028)
* [Fix the case of `stmt_type` in the statement summary](https://github.com/pingcap/tidb/pull/17005)

#### TiDB Dashboard

* [Support the TiFlash disk information](https://github.com/pingcap-incubator/tidb-dashboard/pull/445)
* [Support the case-insensitive log searching](https://github.com/pingcap-incubator/tidb-dashboard/pull/453)
* [Refine UIs](https://github.com/pingcap-incubator/tidb-dashboard/pull/465)

#### TiUP

* [Fix the panic caused by the mirror error](https://github.com/pingcap-incubator/tiup/pull/195)
* [Add the stack trace for `check-configuration` error](https://github.com/pingcap-incubator/tiup-cluster/pull/370)

#### TiKV

* [Fix the issue that restoring a backup archive from GCS does not work](https://github.com/tikv/tikv/pull/7734)
* [Use the key-only support of Titan for the raw key-value pair scan](https://github.com/tikv/tikv/pull/7673)
* [Support batching multiple requests into a Raft entry](https://github.com/tikv/tikv/pull/6683)

#### PD

* [Fix the `404` problem when using the `region key` command in pd-ctl](https://github.com/pingcap/pd/pull/2399)

#### TiSpark

* [Fix a TiSpark decoding error when using the `Chunk` encoding type](https://github.com/pingcap/tispark/pull/1425)
* [Fix the split index](https://github.com/pingcap/tispark/pull/1422)
* [Use `snapshot.batchGet` instead of `snapshot.get`](https://github.com/pingcap/tispark/pull/1424)

## On-going TiDB event

[TiDB Usability Challenge Program](https://pingcap.com/community/tidb-usability-challenge/)
