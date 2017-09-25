---
layout: post
title: Weekly Update
---

## Weekly update in TiDB

2017-09-25

Last week, we landed [63 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is:pr%20is:merged%20merged:2017-09-18..2017-09-24) in the TiDB repositories.

## Added
* [Use new expression framework by default.](https://github.com/pingcap/tidb/pull/4595)
* [Support the DOT explain format.](https://github.com/pingcap/tidb/pull/4562)
* [Support the syntax for `EXPLAIN FORMAT = stringlit`](https://github.com/pingcap/tidb/pull/4554)
* [Support the TIME/TIMESTAMP literal](https://github.com/pingcap/tidb/pull/4368)

## Removed
* [Remove `expression/typeinfer.go` entirely.](https://github.com/pingcap/tidb/pull/4611)
* [Abandon the selection controller.](https://github.com/pingcap/tidb/pull/4528)

## Fixed
* [Roll back the ID allocator when a transaction fails to commit.](https://github.com/pingcap/tidb/pull/4590)
* [Fix the returned column length of all the SHOW statements.](https://github.com/pingcap/tidb/pull/4589)
* [Fix the Navicat for MySQL compatibility issue of the `SHOW CREATE TABLE` statement.](https://github.com/pingcap/tidb/pull/4567)
* [Fix a bug in GC worker.](https://github.com/pingcap/tidb/pull/4561)
* [Fix a bug of `merge JOIN`/`stream aggregation` and `ORDER BY`.](https://github.com/pingcap/tidb/pull/4552)
* [Support the aggregation function that contains an aggregation function.](https://github.com/pingcap/tidb/pull/4511)
* [Abort an unsafe transaction subject to GC command](https://github.com/pingcap/tidb/pull/4469)
* [Fix a bug in `parseDatetime`.](https://github.com/pingcap/tidb/pull/4273)

## Improved
* [Refactor the aggregation to reduce memory usage.](https://github.com/pingcap/tidb/pull/4605)
* [Use continuous-value assumption to estimate cost.](https://github.com/pingcap/tidb/pull/4601)
* [Speed up the `add index` operation.](https://github.com/pingcap/tidb/pull/4579)
* [Don't return the killed session when `SHOW PROCESSLIST`.](https://github.com/pingcap/tidb/pull/4553)
* [Refine the return type, charset and collation for the `get variable` expression.](https://github.com/pingcap/tidb/pull/4550)
* [First step to make parser to be totally compatible with MySQL.](https://github.com/pingcap/tidb/pull/4545)
* [Add real tables for global/session status in the performance schema.](https://github.com/pingcap/tidb/pull/4523)
* [Implement the `ANALYZE` columns pushing down.](https://github.com/pingcap/tidb/pull/4522)
* [Rewrite the builtin function MOD](https://github.com/pingcap/tidb/pull/4407)
* [Use the Goroutine pool to avoid `runtime.morestack`.](https://github.com/pingcap/tidb/pull/3753)
* Remove the usage of "TypeClass" in:
    - [builtin_arithmetic.go](https://github.com/pingcap/tidb/pull/4575)
    - [builtin_string.go](https://github.com/pingcap/tidb/pull/4573)
    - [expression.go](https://github.com/pingcap/tidb/pull/4571)
    - [builtin_cast.go](https://github.com/pingcap/tidb/pull/4570)
    - [builtin_math.go](https://github.com/pingcap/tidb/pull/4568)
    - [builtin_op.go](https://github.com/pingcap/tidb/pull/4547)

## Weekly update in TiSpark

## Fixed
* Fix the [Region client](https://github.com/pingcap/tikv-client-lib-java/pull/105) error in handling for store no match and leader switch 
* Fix an issue in [PD Client](https://github.com/pingcap/tikv-client-lib-java/pull/107) leader switch.

## Weekly update in TiKV

Last week, We landed [30 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-09-18..2017-09-24&type=Issues) in the TiKV repositories.

## Added

* Add [benchmarks](https://github.com/pingcap/tikv/pull/2285) for JSON binary codec.
* Implement [`fmsketch`](https://github.com/pingcap/tikv/pull/2286) for coprocessor.
* Add the [SplitRegion](https://github.com/pingcap/tikv/pull/2287) API.
* [Synchronize the Raft log](https://github.com/pingcap/tikv/pull/2289) when necessary.
* Add the [debug framework](https://github.com/pingcap/tikv/pull/2299).
* Add the [namespace checker](https://github.com/pingcap/pd/pull/755) for PD.
* Support [setting the store state](https://github.com/pingcap/pd/pull/757) for PD.
* Support initial schedulers’ name [from the config file](https://github.com/pingcap/pd/pull/758).
* Add the [table namespace classifier](https://github.com/pingcap/pd/pull/761) for PD.
* Support [scheduling based on regions’ read flow](https://github.com/pingcap/pd/pull/765) for PD.
* Support [getting region’s namespace](https://github.com/pingcap/pd/pull/766) in PD.

## Fixed

* Fix setting a [nonempty store to the tombstone](https://github.com/pingcap/pd/pull/758) state.

## Improved

* Replace `opp_neg` with [`overflowing_neg`](https://github.com/pingcap/tikv/pull/2301).
* Enhance [synchronizing the WAL log](https://github.com/pingcap/tikv/pull/2308).
* Add [metrics](https://github.com/pingcap/tikv/pull/2312) for transactions.
* Use [96MB](https://github.com/pingcap/tikv/pull/2313) as the default size for regions. 
* Use [counters instead of histogram](https://github.com/pingcap/tikv/pull/2319) when statistics scan details.
* Fix [resource downloading and extracting](https://github.com/pingcap/tikv/pull/2321) when bench JSON.
* Add [more statistics](https://github.com/pingcap/tikv/pull/2323) for RocksDB.
* Update the [futures](https://github.com/pingcap/tikv/pull/2326).
* Refactor the [cluster information](https://github.com/pingcap/pd/pull/767) for PD.

## New contributors (Thanks!)
* [David Ding](https://github.com/dantin)
* [Hu Ming](https://github.com/ming-relax)
* [OuYang Jin](https://github.com/qqsun8819)
* [Liang SHANG](https://github.com/LiangShang)
