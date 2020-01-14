---
title: Weekly update (January 06 ~ January 12, 2020)
date: 2020-01-14
summary: Last week, we landed 31 PRs in the TiDB repository, 8 PRs in the TiSpark repository, and 54 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog post

Last week, we published a post that introduces in detail how TiKV handles read and write operations. The post also explores how TiKV, as a distributed database, stores the data contained in a write request and how it retrieves the corresponding data with consistency guaranteed.

The full post is here:

[How TiKV Reads and Writes](https://pingcap.com/blog/how-tikv-reads-and-writes/)

## Community

### New contributors

tidb:

* [SeaRise](https://github.com/SeaRise)
* [ffutop](https://github.com/ffutop)
* [githubFZX](https://github.com/githubFZX)

tikv:

* [yeya24](https://github.com/yeya24)

docs:

* [kana112233](https://github.com/kana112233)

docs-cn:

* [n0vad3v](https://github.com/n0vad3v)

## Call for participation

* [Issues to solve for TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)
* [Issues to solve for TiKV](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

Last week, we landed [31 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2020-01-09..2020-01-12+) in the TiDB repository, [8 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2020-01-06..2020-01-12) in the TiSpark repository, and [54 PRs](https://github.com/search?p=5&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2020-01-06..2020-01-12&type=Issues) in the TiKV and PD repositories.

### Critical PRs

TiDB:

* [Add the transformation rule `TransformLimitToTableDual` in the cascades planner](https://github.com/pingcap/tidb/pull/14430)
* [Support `stream` when reading the cluster memory table](https://github.com/pingcap/tidb/pull/14344)
* [Fill data in `information.tidb_hot_table` for partitioned tables](https://github.com/pingcap/tidb/pull/14331)
* [Support `PointGetPlan` on the hash partitioned table](https://github.com/pingcap/tidb/pull/14318)
* [Implement the restore function for `KindMysqlDuration` and `KindMysqlTime`](https://github.com/pingcap/tidb/pull/13242)

TiSpark:

* [Support partition pruning on range columns partition](https://github.com/pingcap/tispark/pull/1337)

TiKV and PD:

* [Reserve the disk space before creating the database engine](https://github.com/tikv/tikv/pull/6321)
* [Improve the store-load-based scheduler](https://github.com/pingcap/pd/pull/2053)
* [Speed up the configuration change](https://github.com/tikv/tikv/pull/6421)
* [Add the vectorized `random_bytes`](https://github.com/tikv/tikv/pull/6287)
* [Support changing the GC worker configuration online](https://github.com/tikv/tikv/pull/6359)
* [Support changing the RocksDB configuration online](https://github.com/tikv/tikv/pull/6377)
* [Fix the error handling of the RocksDB iterator](https://github.com/tikv/tikv/pull/6327)
* [Fix `get_valid_int_prefix` in the `SELECT` statement context](https://github.com/tikv/tikv/pull/6425)
* [Fix the issue that the result is inconsistent with TiDB when converting `STRING` to `REAL` using the `CAST` function](https://github.com/tikv/tikv/pull/6390)
* [Retry requests of the pending read index on followers](https://github.com/tikv/tikv/pull/6348)
* [Handle configuration changes with Snapshot correctly](https://github.com/tikv/tikv/pull/6352)
* [Fix the issue that the `log_2args` RPN function is inconsistent with TiDB](https://github.com/tikv/tikv/pull/6424)
* [Fix the issue that a string is parsed to the `yymmddhhmm` time format](https://github.com/tikv/tikv/pull/6440)
* [Fix the issue that the `00:00:00` string is parsed to `2000-00-00 00:00:00`](https://github.com/tikv/tikv/pull/6461)
* [Fix the issue that the integer is converted to the duration](https://github.com/tikv/tikv/pull/6459)
* [Fix the issue that the `RealPlus` overflow is inconsistent with TiDB](https://github.com/tikv/tikv/pull/6458)
