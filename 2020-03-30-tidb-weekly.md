---
title: Weekly update (March 23 ~ March 29, 2020)
date: 2020-03-30
summary: Last week, we landed 100 PRs in the TiDB repository and 39 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog post

Last week, we published an article that introduces how we use [pprof](https://golang.org/pkg/net/http/pprof/) to visualize TiKV's profiling data to help quickly locate TiKV's performance bottlenecks online. If you also write Rust programs, you can introduce [pprof-rs](https://github.com/tikv/pprof-rs) into your projects to help analyze your programs' performance online.

The full article is here:

[Quickly Find Rust Program Bottlenecks Online Using a Go Tool](https://pingcap.com/blog/quickly-find-rust-program-bottlenecks-online-using-a-go-tool/)

## Community

### New contributors

tidb:

* [wq1019](https://github.com/wq1019)
* [clark1013](https://github.com/clark1013)

tikv:

* [SSebo](https://github.com/SSebo)

pd:

* [wq1019](https://github.com/wq1019)

docs-cn:

* [sumens](https://github.com/sumens)

tidb-operator:

* [tfulcrand](https://github.com/tfulcrand)

tidb-ansible:

* [SSebo](https://github.com/SSebo)

chaos-mesh:

* [vincent178](https://github.com/vincent178)
* [at15](https://github.com/at15)
* [STRRL](https://github.com/STRRL)

## Call for participation

### TiDB

* [To fix an unexpected panic in `mocktikv`](https://github.com/pingcap/tidb/issues/15662)
* [To fix the issue that the SQL statements from `show create table` have the collation binary parsing error](https://github.com/pingcap/tidb/issues/15633)

### TiKV

* [To add the metric for the Raft entries cache](https://github.com/tikv/tikv/issues/7222)
* [To automatically dismiss "Import mode"](https://github.com/tikv/tikv/issues/7223)
* [All help-wanted issues in TiKV](https://github.com/tikv/tikv/issues?q=is%3Aopen+is%3Aissue+label%3Astatus%2Fhelp-wanted)

### TiDB Dashboard

* [To test the search result of downloaded logs](https://github.com/pingcap-incubator/tidb-dashboard/issues/292)
* [To utilize `useClientRequest` in the log search](https://github.com/pingcap-incubator/tidb-dashboard/issues/290)

### TiDB Backup & Restore (BR)

* [All help-wanted issues in TiDB Backup & Restore](https://github.com/pingcap/br/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)

### TiDB Change Data Capture (CDC)

* [All help-wanted issues in TiDB Change Data Capture](https://github.com/pingcap/ticdc/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)

## Updates of the week

### Progress

Last week, we landed [100 PRs](https://github.com/pingcap/tidb/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-03-23..2020-03-29+) in the TiDB repository and [39 PRs](https://github.com/tikv/tikv/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-03-23..2020-03-29+) in the TiKV and PD repositories.

#### TiDB

* [Check `null` values when comparing different groups during `streamAgg`](https://github.com/pingcap/tidb/pull/15742)
* [Support `ADMIN RELOAD BINDINGS` to refresh the binding cache](https://github.com/pingcap/tidb/pull/15732)
* [Use `UnionRanges` to build the index key-value range for `INLJ`](https://github.com/pingcap/tidb/pull/15727)
* [Fix the TiFlash compatibility issue with the binding and the SQL plan management](https://github.com/pingcap/tidb/pull/15719)
* [Do not cache the plan for queries on range partition tables](https://github.com/pingcap/tidb/pull/15697)

#### TiDB Dashboard

* [Customize the diagnosis duration](https://github.com/pingcap-incubator/tidb-dashboard/pull/300)
* [Replace `sql-formatter` with `sql-formatter-plus`](https://github.com/pingcap-incubator/tidb-dashboard/pull/297)
* [Use `DetailsTable` in `FabricUI`](https://github.com/pingcap-incubator/tidb-dashboard/pull/293)
* [Support highlighting the code and formatting the SQL statements automatically](https://github.com/pingcap-incubator/tidb-dashboard/pull/283)

#### TiUP

* [Add `-C` for the package component and support multiple targets](https://github.com/pingcap-incubator/tiup/pull/88)
* [Specify the component binary path](https://github.com/pingcap-incubator/tiup/pull/82)
* [Support specifying the configuration file of TiDB, TiKV, or PD when starting the playground](https://github.com/pingcap-incubator/tiup/pull/80)

### TiDB Change Data Capture (CDC)

* [Add metrics in the mounter and the blackhole sink](https://github.com/pingcap/ticdc/pull/397)
* [Add more metrics of the `chan` size](https://github.com/pingcap/ticdc/pull/394)
* [Add a retry to the client getter of the gRPC stream](https://github.com/pingcap/ticdc/pull/390)
* [Fix the block when the `run` function of `owner` returns an error](https://github.com/pingcap/ticdc/pull/381)
* [Fix the lower-case schema name](https://github.com/pingcap/ticdc/pull/379)

#### TiKV

* [Add Fu Chen as TiKV Maintainer](https://github.com/tikv/tikv/pull/7259)
* [Apply read requests after the snapshot](https://github.com/tikv/tikv/pull/7230)
* [Support `group by` as a constant](https://github.com/tikv/tikv/pull/7238)
* [Add Daobing Li as TiKV Maintainer](https://github.com/tikv/tikv/pull/7237)
* [Do not use the unified pool to handle storage requests by default](https://github.com/tikv/tikv/pull/7234)
* [Do not check invalid dates when using the `Chunk` format](https://github.com/tikv/tikv/pull/7218)
* [Add Titan-related configurations](https://github.com/tikv/tikv/pull/7207)

#### PD

* [Add load expectations for hot schedulers](https://github.com/pingcap/pd/pull/2297)
* [Add some metrics for hot Regions](https://github.com/pingcap/pd/pull/2295)
* [Add a moving average to filter out the high-frequency noise](https://github.com/pingcap/pd/pull/2286)
* [Add the `replicate-mode` configuration](https://github.com/pingcap/pd/pull/2277)

## On-going TiDB event

[TiDB Usability Challenge Program](https://pingcap.com/community/tidb-usability-challenge/)
