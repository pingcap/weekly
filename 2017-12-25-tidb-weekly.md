---
title: Weekly update (December 18 ~ December 24, 2017)
date: 2017-12-25
summary: Last week, we landed 48 PRs in the TiDB repositories, 10 PRs in the TiSpark repositories, and 13 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [48 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is:pr%20is:merged%20merged:2017-12-18..2017-12-24) in the TiDB repositories.

## Added

* [Support the builtin aggregation function `bit_or`.](https://github.com/pingcap/tidb/pull/5145)

## Removed

* [Remove the old JSON type.](https://github.com/pingcap/tidb/pull/5468)
* [Remove the `HashSemiJoin` plan and executor.](https://github.com/pingcap/tidb/pull/5467)

## Fixed

* [Support showing the current `auto_increment` id in the result of `show create table`.](https://github.com/pingcap/tidb/pull/5470)
* [Fix a bug of `NewIndexLookUpJoin's Next()`.](https://github.com/pingcap/tidb/pull/5455)
* [Fix the trigger condition for `AutoAnalyze`.](https://github.com/pingcap/tidb/pull/5446)
* [Only rebuild the range when using prepared cache.](https://github.com/pingcap/tidb/pull/5442)

## Improved

* [Merge `ApplyExec` and `NestedLoopJoin` into `NestedLoopApply`.](https://github.com/pingcap/tidb/pull/5471)
* [Refine the `UnionAll` plan building.](https://github.com/pingcap/tidb/pull/5464/files)
* [Metrics: record details of the RPC type and store id.](https://github.com/pingcap/tidb/pull/5461)
* [Replace `JSON` with `BinaryJSON`.](https://github.com/pingcap/tidb/pull/5460)
* [Collect and store the query feedback.](https://github.com/pingcap/tidb/pull/5438)
* [Make the function `ExtractColumns` more efficient.](https://github.com/pingcap/tidb/pull/5435)
* [Add `BinaryJSON` functions.](https://github.com/pingcap/tidb/pull/5428)
* [Enhance the index join, making it can be used for more scenarios.](https://github.com/pingcap/tidb/pull/5425)
* [Graceful shutdown will wait clients to close.](https://github.com/pingcap/tidb/pull/5375)
* Support `Chunk` in executors: 
  - [`LoadData`](https://github.com/pingcap/tidb/pull/5465)
  - [`GrantExec`](https://github.com/pingcap/tidb/pull/5459)
  - [`RevokeExec`](https://github.com/pingcap/tidb/pull/5458)
  - [`DeallocateExec`](https://github.com/pingcap/tidb/pull/5457)
  - [`SimpleExec`](https://github.com/pingcap/tidb/pull/5453)
  - [`AnalyzeExec`](https://github.com/pingcap/tidb/pull/5452)
  - [`TableScanExec`](https://github.com/pingcap/tidb/pull/5443)
  - [`ShowDDLjobsExec`](https://github.com/pingcap/tidb/pull/5412)
  - [`TableDualExec`](https://github.com/pingcap/tidb/pull/5395)
  - [`ReplaceExec`](https://github.com/pingcap/tidb/pull/5370)
  - [`DeleteExec`](https://github.com/pingcap/tidb/pull/5368)
  - [`MergeJoinExec`](https://github.com/pingcap/tidb/pull/5312)

# Weekly update in TiSpark

Last week, we landed [10 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2017-12-18..2017-12-24) in the TiSpark repositories.

## Added

* [Add counting single column tests.](https://github.com/pingcap/tispark/pull/155)
* [Add `request.timezone.offset` config.](https://github.com/pingcap/tispark/pull/149)
* [Add the test framework for each issue.](https://github.com/pingcap/tispark/pull/141)
* [Add index related integration tests.](https://github.com/pingcap/tispark/pull/139)
* [Add debug utils.](https://github.com/pingcap/tispark/pull/136)
* [Add null data for DAG test cases.](https://github.com/pingcap/tispark/pull/126)

## Removed

* [Remove timezone in the `TisparkTest.sql` file.](https://github.com/pingcap/tispark/pull/147)

## Fixed

* [Fix the Load tests problem.](https://github.com/pingcap/tispark/pull/154)
* [Fix the test framework concerning null tests.](https://github.com/pingcap/tispark/pull/151)

# Weekly update in TiKV and PD

Last week, we landed [13 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-12-17..2017-12-23&type=Issues) in the TiKV and PD repositories.

## Added

* [Support Raft Learner.](https://github.com/pingcap/tikv/pull/2491)
* [Add transaction tests with `fail-rs`.](https://github.com/pingcap/tikv/pull/2592)
* [Add more configurations for the RocksDB column family.](https://github.com/pingcap/tikv/pull/2599)
* [Add more complex configurations for the PD simulator.](https://github.com/pingcap/pd/pull/893)
* [Coprocessor: collect output counts for each executor.](https://github.com/pingcap/tikv/pull/2607)

## Fixed

* [PD: support `join` without scheme.](https://github.com/pingcap/pd/pull/892) 
* [Return the stale epoch error for retry.](https://github.com/pingcap/tikv/pull/2595)
* [Add the `require` option to the `addr` command flag.](https://github.com/pingcap/tikv/pull/2602)
* [Update `rustc_serialize` to pass newer Rust version compilation.](https://github.com/pingcap/tikv/pull/2604)

## Improved

* [Coprocessor: speed up the CM sketch test.](https://github.com/pingcap/tikv/pull/2577)
* [Add `key_only` to avoid fetching the data value.](https://github.com/pingcap/tikv/pull/2580)
* [Avoid calling Raft status to reduce allocation.](https://github.com/pingcap/tikv/pull/2601)

# New contributors (Thanks!)

TiKV:

- [Jiahao Huang](https://github.com/july2993)
- [Andrew Hobden](https://github.com/hoverbear)

