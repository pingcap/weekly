---
title: Weekly update (December 30 ~ January 05, 2020)
date: 2020-01-06
summary: Last week, we landed 36 PRs in the TiDB repository, 14 PRs in the TiSpark repository, and 42 PRs in the TiKV and PD repositories.
aliases: ['/weekly/2020-01-06/']
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## Community

### New contributor

tidb:

* [yuanjize](https://github.com/yuanjize)

## Call for participation

* Coprocessor SIG:
    * [Improve the performance of Chunk Encoder](https://github.com/tikv/tikv/issues/5729)
    * [Port `BinaryJSON`](https://github.com/tikv/tikv/issues/5715)
    * [Tracing](https://github.com/tikv/tikv/issues/5714)
    * [The maximum execution time of Per-request](https://github.com/tikv/tikv/issues/5712)

* [More issues to solve for TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)
* [More issues to solve for TiKV](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

Last week, we landed [36 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-12-30..2020-01-05+) in the TiDB repository, [14 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-12-30..2020-01-05) in the TiSpark repository, and [42 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-12-30..2020-01-05&type=Issues) in the TiKV and PD repositories.

### Critical PRs

TiDB:

* [Support the `sql` tag in the `pprof` result](https://github.com/pingcap/tidb/pull/14312)
* [Add a metric for `ttlManager` to record the lifetime reach events](https://github.com/pingcap/tidb/pull/14298)
* [Support renaming columns in DDL operations](https://github.com/pingcap/tidb/pull/14281)
* [Support the partitioned table for the `/mvcc/*` HTTP API](https://github.com/pingcap/tidb/pull/14197)
* [Add the memory tracker for `InsertExec` and `ReplaceExec`](https://github.com/pingcap/tidb/pull/14179)
* [Open the push-down switcher for a part of the `CAST` functions](https://github.com/pingcap/tidb/pull/13837)
* [Support caching Coprocessor responses](https://github.com/pingcap/tidb/pull/13824)
* [Add the fast access path for the hash partition](https://github.com/pingcap/tidb/pull/13772)
* [Support `IndexMergeReaderExecutor`](https://github.com/pingcap/tidb/pull/12305)

TiSpark:

* [Refactor the expression system](https://github.com/pingcap/tispark/pull/1327)
* [Fix the current breakage against TiKV](https://github.com/pingcap/tispark/pull/1349)

TiKV and PD:

* [Change the default write buffer size of `LockCF` to 32MB](https://github.com/tikv/tikv/pull/6393)
* [Add the exclusive label](https://github.com/pingcap/pd/pull/2074)
* [Fix the panic when enabling placement rules](https://github.com/pingcap/pd/pull/2070)
* [Fix the issue that `MvccProperties` is not generated when TiKV restores data](https://github.com/tikv/tikv/pull/6378)
* [Upgrade etcd to v3.4.3](https://github.com/pingcap/pd/pull/2063)
* [Support specifying keys to split Regions](https://github.com/tikv/tikv/pull/6372)
* [Add `resolved_ts`](https://github.com/tikv/tikv/pull/6371)
* [Use `commit` to clean up pessimistic locks](https://github.com/tikv/tikv/pull/6355)
* [Enable the gRPC `keepalive` feature on TiKV servers](https://github.com/tikv/tikv/pull/6342)
* [Filter the write `CF SST` by `commit ts` in the incremental backup](https://github.com/tikv/tikv/pull/6339)
* [Check `need_gc` before getting the snapshot](https://github.com/tikv/tikv/pull/6333)
* [Add the feature of changing the online configuration](https://github.com/tikv/tikv/pull/6331)
* [Add the pd-backup tool](https://github.com/pingcap/pd/pull/2048)
* [Improve the waiter manager](https://github.com/tikv/tikv/pull/6298)
* [Add the configuration gRPC service](https://github.com/pingcap/pd/pull/2033)
* [Remove `jemalloc` from the default feature of `tikv-alloc`](https://github.com/tikv/tikv/pull/6211)
* [Adjust the store limit dynamically according to the cluster state](https://github.com/pingcap/pd/pull/1902)
