---
title: Weekly update (December 12 ~ December 18, 2016)
date: 2016-12-19
summary: Last week, we landed 32 PRs in the TiDB repositories and 11 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV']
---

# Weekly update in TiDB

Last week, we landed [32 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-12-12..2016-12-18) in the TiDB repositories.

## Added

+ [Add the `FlagIgnoreTruncate/FlagTruncateAsWarning` flag to control the behavior of truncated errors.](https://github.com/pingcap/tidb/pull/2212)

+ [Add the `prompt` text flag.](https://github.com/pingcap/tidb/pull/2227)

+ [Add the rawkv metrics](https://github.com/pingcap/tidb/pull/2228) to profile the rawkv API performance.

+ [Add a comparable varint encoding/decoding method](https://github.com/pingcap/tidb/pull/2236) to make encoded data smaller.

+ [Support the `timediff` built-in function.](https://github.com/pingcap/tidb/pull/2249)

+ [Support the following built-in functions](https://github.com/pingcap/tidb/pull/2258): ln(), log(), log2(), log10().

## Fixed

+ [A bug that ignores primary key’s unsigned attribute.](https://github.com/pingcap/tidb/pull/2222)

+ [A bug that ignores error in the `distsql` layer.](https://github.com/pingcap/tidb/pull/2226)

+ [Allow default value to be Null when the column has the `auto_increament` attribute](https://github.com/pingcap/tidb/pull/2230) to be compatible with MySQL 5.6.

+ [A bug in the `insert` statement that ignores error.](https://github.com/pingcap/tidb/pull/2241)

+ Fix bugs in the cost-based optimization framework: [#2243](https://github.com/pingcap/tidb/pull/2243)

## Improved

+ Refactor the time type related code: [#2185](https://github.com/pingcap/tidb/pull/2185), [#2190](https://github.com/pingcap/tidb/pull/2190), [#2206](https://github.com/pingcap/tidb/pull/2206), [#2233](https://github.com/pingcap/tidb/pull/2233), [#2261](https://github.com/pingcap/tidb/pull/2261)

+ [Remove the util/bytes package](https://github.com/pingcap/tidb/pull/2221) to clean up the code.

+ Refactor the code to remove the `evaluator.Eval()` method: [#2222](https://github.com/pingcap/tidb/pull/2222), 

+ [Improve test coverage for the `util/segmentmap` package.](https://github.com/pingcap/tidb/pull/2235)

+ [Recover from panics caused by malformated mysql packet](https://github.com/pingcap/tidb/pull/2267) to make tidb-server more robust.

## New contributor

+ [Bai Yang](https://github.com/hamo)

# Weekly update in TiKV

Last week, we landed [11 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2016-12-11..2016-12-17&type=Issues&ref=searchresults) in the TiKV repositories.

## Added

+ Add a configuration to [disable data sync](https://github.com/pingcap/tikv/pull/1369) to speed up loading data. 

+ Filter [the pending peers](https://github.com/pingcap/pd/pull/421) for Placement Driver (PD) scheduler. 

+ Add [`pd-ctl`](https://github.com/pingcap/pd/pull/431) to operate PD more easily.

## Fixed

+ Update [the advertise peer urls](https://github.com/pingcap/pd/pull/438) from etcd to fix [#435](https://github.com/pingcap/pd/issues/435).

## Improved

+ [Read and verify snapshot](https://github.com/pingcap/tikv/pull/1381) file in one step. 

+ Use a [smaller interval](https://github.com/pingcap/tikv/pull/1401) to make Raft tick more accurate. 

+ Clean up [the tombstone store](https://github.com/pingcap/pd/issues/428) to fix [#401](https://github.com/pingcap/pd/issues/401).

+ Use [`delete_file_in_range`](https://github.com/pingcap/tikv/pull/1409) when clean up the tombstone regions.

