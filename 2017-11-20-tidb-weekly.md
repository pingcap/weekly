---
title: Weekly update (November 13 ~ November 19, 2017)
date: 2017-11-20
summary: Last week, we landed 48 PRs in the TiDB repositories, 3 PRs in the TiSpark repositories, and 23 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [48 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is:pr%20is:merged%20merged:2017-11-13..2017-11-19) in the TiDB repositories.

## Removed

* [Remove redundant `ResolveIndices`.](https://github.com/pingcap/tidb/pull/5089)
* [Remove useless error return.](https://github.com/pingcap/tidb/pull/5085)

## Fixed

* [Fix the index recognized as prefix index when the column length is enlarged.](https://github.com/pingcap/tidb/pull/5139)
* [Check the `MaxInt64` and `MinInt64` to avoid range error.](https://github.com/pingcap/tidb/pull/5136)
* [Fix the estimation in `betweenRowCount`.](https://github.com/pingcap/tidb/pull/5135)
* [Refine sql_mode `no_backslash_escapes`.](https://github.com/pingcap/tidb/pull/5108)
* [Add deep copies for the update operation.](https://github.com/pingcap/tidb/pull/5098)
* [Refine projection elimination when projection is the inner child of an outer `join`.](https://github.com/pingcap/tidb/pull/5086)
* [Fix a data race in `dataReaderBuilder`.](https://github.com/pingcap/tidb/pull/5067)
* [Support `not in` and correct the behavior.](https://github.com/pingcap/tidb/pull/5057)

## Improved

* [Remove returned value `isNull` in `Row` methods.](https://github.com/pingcap/tidb/pull/5131)
* [Replace `*ast.Row` with `types.Row` and prepare to use Chunk.](https://github.com/pingcap/tidb/pull/5124)
* [Increase the batch size slowly for double read, which benefits small queries.](https://github.com/pingcap/tidb/pull/5123)
* [Remove `unionscan` schema and add `LogicalUnionScan`.](https://github.com/pingcap/tidb/pull/5119)
* [Build the logical plan to check the column name validation when `doPrepare`.](https://github.com/pingcap/tidb/pull/5116)
* [Covert `max/min` to `Limit + Sort` operators.](https://github.com/pingcap/tidb/pull/5105)
* [Support adding columns with parentheses.](https://github.com/pingcap/tidb/pull/5103)
* [Prealloced space.](https://github.com/pingcap/tidb/pull/5094)
* [Ignore the DDL statement for query duration metrics.](https://github.com/pingcap/tidb/pull/5093)
* [Refine the use of `idAllocator`.](https://github.com/pingcap/tidb/pull/5088)
* [Use `baseExecutor` for all `Executors`.](https://github.com/pingcap/tidb/pull/5087)
* [Support decoding data to Chunk.](https://github.com/pingcap/tidb/pull/5066)
* [Make `tokenLimit` configurable.](https://github.com/pingcap/tidb/pull/4973)

## New contributors (Thanks!)

* [liubo](https://github.com/liubo0127)
* [ZhengQian](https://github.com/buggithubs)
* [Zhengwanbo](https://github.com/zhengwanbo)

# Weekly update in TiSpark

Last week, we landed [3 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-11-13..2017-11-19%20) in the TiSpark repositories.

## Fixed

* [Fix the unsupported expression error of not being pushed back](https://github.com/pingcap/tikv-client-lib-java/pull/144).
* [Fix the thread pool error of not closing properly.](https://github.com/pingcap/tikv-client-lib-java/pull/139)
* [Fix the Bit type being pushed down.](https://github.com/pingcap/tispark/pull/83)

# Weekly update in TiKV

Last week, we landed [23 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-11-13..2017-11-20) in the TiKV repositories.

## Added

* [Add more observers.](https://github.com/pingcap/tikv/pull/2423)
* [Support configuring namespaces.](https://github.com/pingcap/pd/pull/858)

## Fixed

* [Fix a range check in debugging API.](https://github.com/pingcap/tikv/pull/2464)
* [Fix CI execution.](https://github.com/pingcap/tikv/pull/2472)
* [Make the progresses stored in Raft leader never false positive.](https://github.com/pingcap/tikv/pull/2474)
* [Fix the Chunk size of coprocessor response.](https://github.com/pingcap/tikv/pull/2476)
* [Fix a potential dead lock when resolving address.](https://github.com/pingcap/tikv/pull/2477)
* [Return the correct leader when the `NotLeader` error occurs.](https://github.com/pingcap/tikv/pull/2479)
* [Fix wrong log info.](https://github.com/pingcap/pd/pull/857)

## Improved

* [As a part of introducing streaming, remove `lifetime` in the transaction layer.](https://github.com/pingcap/tikv/pull/2423)
* Code cleanup.
   - [Move mod debug from `raftstore` into `server`](https://github.com/pingcap/tikv/pull/2470)
   - [Fix typos](https://github.com/pingcap/tikv/pull/2482)
   - [Move `opt` into `clusterInfo`](https://github.com/pingcap/pd/pull/850)
   - [Clean up `scheduelr`](https://github.com/pingcap/pd/pull/852)
   - [Move server methods to `server.go`](https://github.com/pingcap/pd/pull/861)
* [Use `git describe` to assign `PDReleaseVersion`.](https://github.com/pingcap/pd/pull/847)
* [Prealloc pre-makes space.](https://github.com/pingcap/pd/pull/849)
* [Use `CGO\_ENABLED` instead of `ENABLE\_CGO`.](https://github.com/pingcap/pd/pull/855)
* [Add the log signal before exit.](https://github.com/pingcap/pd/pull/860)
* [Limit the duration metric buckets of gRPC messages.](https://github.com/pingcap/tikv/pull/2488)
* [Shorten `write guard lifetime` when sending the snapshot.](https://github.com/pingcap/tikv/pull/2490)

## New contributors (Thanks!)

* [Drogon](https://github.com/JackDrogon)
