---
title: Weekly update (May 1 ~ May 7, 2017)
date: 2017-05-08
summary: Last week, we landed 33 PRs in the TiDB repositories and 13 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV']
---

# Weekly update in TiDB

Last week, we landed [33 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-05-01..2017-05-07%20) in the TiDB repositories.

## Added

* Add builtin function [`is_ipv4_mapped`](https://github.com/pingcap/tidb/pull/3193), [`makedate`](https://github.com/pingcap/tidb/pull/3102), [`utc_time`](https://github.com/pingcap/tidb/pull/3145)

* [Enable privilege checking by default.](https://github.com/pingcap/tidb/pull/2995) You could also disable privilege checking through `--privilege=false`.

* [Support `Analyze Index` statement:](https://github.com/pingcap/tidb/pull/3156) after adding an index, we could run this statement to analyze the newly added index.

* [Add `Trigger_priv` column in `mysql.user` system table.](https://github.com/pingcap/tidb/pull/3143)

* [Add `coveralls` in CI.](https://github.com/pingcap/tidb/pull/3150)

## Fixed

* [Fix incompatible issue in found_rows().](https://github.com/pingcap/tidb/pull/3134)

* [Fix a few panic when infering type for some functions without argument.](https://github.com/pingcap/tidb/pull/3137)

* [Fix a data race in Join operator.](https://github.com/pingcap/tidb/pull/3159)

* [Fix parse time_zone `-6:00`.](https://github.com/pingcap/tidb/pull/3165)

* [Fix a bug in checking duplicate column.](https://github.com/pingcap/tidb/pull/3174)

* [Check ignored errors.](https://github.com/pingcap/tidb/pull/3178)

* [Fix comment warning in executor package.](https://github.com/pingcap/tidb/pull/3187)

* [Fix a bug about converting string to bit.](https://github.com/pingcap/tidb/pull/3188)

* [Recognize `uuid()` as a dynamic function.](https://github.com/pingcap/tidb/pull/3207)

* [Fix a bug in `rand()` with seed.](https://github.com/pingcap/tidb/pull/3213)


## Improved

* [Enlarge the stack size to save the `runtime.morestack` cost.](https://github.com/pingcap/tidb/pull/3054) 

* [Parallelly prewrite primary and secondary lock.](https://github.com/pingcap/tidb/pull/3148)

* New planner framework: [`SortMergeJoin`](https://github.com/pingcap/tidb/pull/3153), [`IndexReader`](https://github.com/pingcap/tidb/pull/3175)

* Refactor expression evaluation framework: [Rewrite compare operator.](https://github.com/pingcap/tidb/pull/3155) [Implement the new Eval interface for ColumnExpr and ConstExpr.](https://github.com/pingcap/tidb/pull/3128) [Decide the return type of ColumnExpr and ConstExpr during planning.](https://github.com/pingcap/tidb/pull/3201)

# Weekly update in TiKV

Last week, We landed [13 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-04-30..2017-05-06&type=Issues) in the TiKV repositories.

## Added

* [Apply the Raft logs of multiply regions in batches.](https://github.com/pingcap/tikv/pull/1763)

* Add [hotspot](https://github.com/pingcap/pd/pull/631) command in `pd-ctl`: detect and show hotspot regions.

* Add [sub-compaction](https://github.com/pingcap/tikv/pull/1811), [ base-background-compactions](https://github.com/pingcap/tikv/pull/1814) and [writable-file-max-buffer-size](https://github.com/pingcap/tikv/pull/1815) for RocksDB.

* Let manual compaction run [concurrently](https://github.com/pingcap/tikv/pull/1813) with background compaction.

## Fixed

* Create [column family orderly](https://github.com/pingcap/tikv/pull/1798).

* [Remove CRC32 checksum](https://github.com/pingcap/tikv/pull/1805) when initializing snapshot in RaftStore thread. 

* Get the [correct position](https://github.com/pingcap/tikv/pull/1810) in the pending vote queue. 

* Remove old operator [limiter](https://github.com/pingcap/pd/pull/632) when adding new PriorityKind operator.

## Improved

* Use [channel](https://github.com/pingcap/tikv/pull/1801) to reduce lock contention when pushing task to thread pool. 

* Make [scheduler more smooth](https://github.com/pingcap/pd/pull/628) when starting PD.
