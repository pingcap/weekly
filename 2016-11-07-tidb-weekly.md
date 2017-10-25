---
date: 2016-11-07T00:00:00Z
title: Weekly Update
url: /2016/11/07/tidb-weekly/
---

Last week, we landed [42 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-10-31..2016-11-06%20) in the TiDB repositories and [29 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2016-10-30..2016-11-05&type=Issues&ref=searchresults) in the TiKV repositories.

# New release

## [TiDB Beta 4](https://github.com/pingcap/tidb/releases/tag/beta4)

# Weekly update in TiDB

## Added

+ [The aggregation info to the explain statement.](https://github.com/pingcap/tidb/pull/1901)

+ [Support the show processlist syntax](https://github.com/pingcap/tidb/pull/1907). TiDB supports mydumper now.

+ [Support the show create database statement.](https://github.com/pingcap/tidb/pull/1911)

+ [Support the buildin function from_unixtime.](https://github.com/pingcap/tidb/pull/1929)

+ [Push down the aggregation operator to the position before join.](https://github.com/pingcap/tidb/pull/1899)

+ [Get cluster ID from Placement Driver.](https://github.com/pingcap/tidb/pull/1931)

## Fixed

+ [A bug in parser that misses the recognize identifier with leading digits.](https://github.com/pingcap/tidb/pull/1887)

+ [A bug in the `load data` command. ](https://github.com/pingcap/tidb/pull/1953)

## Improved

+ [The performance of the DropTable statement.](https://github.com/pingcap/tidb/pull/1888)

+ [The performance of the AddIndex statement.](https://github.com/pingcap/tidb/pull/1916)

+ [The query metrics.](https://github.com/pingcap/tidb/pull/1957) 

# Weekly update in TiKV

## Added

+ [Multiversion concurrency control (MVCC)](https://github.com/pingcap/tikv/pull/1196) support for `tikv-ctl`. 
+ Support `-v`/`--version` to print the [version information](https://github.com/pingcap/pd/pull/369).
+ Metrics for MVCC [key versions and deleted key versions](https://github.com/pingcap/tikv/pull/1248).
+ Use random cluster ID to bootstrap clusters to avoid wrong joining cluster by the users, with PR [370](https://github.com/pingcap/pd/pull/370), [1257](https://github.com/pingcap/tikv/pull/1257)

## Fixed

+ [Panic directly](https://github.com/pingcap/tikv/pull/1266) if the RocksDB writes fail to fix [1262](https://github.com/pingcap/tikv/issues/1262).
+ Add the [`start`](https://github.com/pingcap/pd/pull/375) time for store monitor to fix [1207](https://github.com/pingcap/tikv/issues/1207).
+ [Return the 'no leader' error](https://github.com/pingcap/pd/pull/376/files) to avoid panic when calling the GetLeader API with no leader.

## Improved

+ [Skip values](https://github.com/pingcap/tikv/pull/1218) for scan. 
+ Make cache code cleaner, with PR [365](https://github.com/pingcap/pd/pull/365), [366](https://github.com/pingcap/pd/pull/366), [367](https://github.com/pingcap/pd/pull/367).
+ Allow [liner reverse seek](https://github.com/pingcap/tikv/pull/1233) in the `lock` column family.
+ [Separate compaction](https://github.com/pingcap/tikv/pull/1242) to a different thread worker.
+ Avoid filling block cache when [scanning](https://github.com/pingcap/tikv/pull/1251).
+ Include [the snapshot size](https://github.com/pingcap/tikv/pull/1252) in the `used_size` store.
+ [Dump the RocksDB statistics](https://github.com/pingcap/tikv/pull/1254) with the SIGUSR1 signal.