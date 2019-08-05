---
title: Weekly update (July 29 ~ August 04, 2019)
date: 2019-08-05
summary: Last week, we landed 83 PRs in the TiDB repository, 19 PRs in the TiSpark repository, and 31 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [83 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-07-29..2019-08-04+) in the TiDB repository.

## Added

- [Add the vectorized evaluation methods to `Expression`](https://github.com/pingcap/tidb/pull/11530)
- [Support `CAST as float`](https://github.com/pingcap/tidb/pull/11519)

## Improved

- [Add `Region-ID` when getting the MVCC by `Handle`](https://github.com/pingcap/tidb/pull/11436)
- [Move the log operation out of the lock scope](https://github.com/pingcap/tidb/pull/11536)
- [Add `split-region-max-num` in `config` to control the maximum number of split Regions](https://github.com/pingcap/tidb/pull/11427)
- [Speed up the operation of `admin check table`](https://github.com/pingcap/tidb/pull/8572)

## Fixed

- [Fix the bug of loading the dropped database schema and the `db-table` API error](https://github.com/pingcap/tidb/pull/11573)
- [Fix the issue that `baseExecutor`'s children might not be closed](https://github.com/pingcap/tidb/pull/11570)
- [Fix the data race of `admin check table`](https://github.com/pingcap/tidb/pull/11568)
- [Invalidate a store's Regions after the store is removed in KV](https://github.com/pingcap/tidb/pull/11567)
- [Fix a bug that window functions do not check `IGNORE NULLS`](https://github.com/pingcap/tidb/pull/11554)
- [Fix the wrong estimation for the time values](https://github.com/pingcap/tidb/pull/11511)
- [Fix a compatibility bug for the window function](https://github.com/pingcap/tidb/pull/11488)
- [Fix the display of `on update` in `CURRENT_TIMESTAMP` with decimal](https://github.com/pingcap/tidb/pull/11480)
- [Make `grant all privileges` work right](https://github.com/pingcap/tidb/pull/11449)
- [Fix a bug that an error occurs when the range partition is added and the value is negative](https://github.com/pingcap/tidb/pull/11407)

# Weekly update in TiSpark

Last week, we landed [19 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-07-29..2019-08-04+) in the TiSpark repository.

## Fixed

- [Fix the issue that `view` cannot be parsed](https://github.com/pingcap/tispark/pull/953)
- [Fix the issue that the Range Partition might throw `UnsupportedSyntaxException` when the unsupported partition function is used](https://github.com/pingcap/tispark/pull/960)
- [Enable TiSpark to read data from a hash partition table](https://github.com/pingcap/tispark/pull/966)
- [Fix `java.lang.IncompatibleClassChangeError` when submitting with `spark-2.4.3`](https://github.com/pingcap/tispark/pull/972)
- [Fix the cost model in the table scan](https://github.com/pingcap/tispark/pull/977)
- [Fix the error message when encountering `UninitializedType` such as `TypeDecimal`](https://github.com/pingcap/tispark/pull/979)

# Weekly update in TiKV and PD

Last week, we landed [31 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-07-29..2019-08-04&type=Issues) in the TiKV and PD repositories.

## Added

- [Add `evaluate_ctx` which returns `EvalContext`](https://github.com/tikv/tikv/pull/5177)
- [Add `DecimalDivide` to the `RPN` expression framework](https://github.com/tikv/tikv/pull/5171)
- [Add a `convert` trait and implement `ConvertTo<Decimal>`](https://github.com/tikv/tikv/pull/5167)
- [Add the multiplication arithmetic for the `RPN` function framework](https://github.com/tikv/tikv/pull/5107)
- [Enable `libressl` by default](https://github.com/tikv/tikv/pull/5140)
- [Collect the CPU usage and the I/O rates of threads in disks](https://github.com/tikv/tikv/pull/5144)
- [Add a `convert` trait and implement the `ConvertTo<u64>` string](https://github.com/tikv/tikv/pull/5146)
- [Add `CONTROL` functions](https://github.com/tikv/tikv/pull/5154)

## Improved

- [Optimize the metrics of the local reader](https://github.com/tikv/tikv/pull/5183)
- [Clean up the statistics of read flow](https://github.com/tikv/tikv/pull/5175)
- [Speed up `test_many_tombstones`](https://github.com/tikv/tikv/pull/5173)
- [Add an `INFO` log for the `bootstrap cluster`](https://github.com/tikv/tikv/pull/5172)
- [Improve the arithmetic operation with `ctx`](https://github.com/tikv/tikv/pull/5166)
- [Make several `INFO` logs `DEBUG` and refine some log messages](https://github.com/tikv/tikv/pull/4768)
- [Re-organize the schedule package](https://github.com/pingcap/pd/pull/1638)
- [Implement the lazy expiration of `DetectTable`](https://github.com/tikv/tikv/pull/5108)
- [Use trait to re-organize `CONVERT` to the `INT`/`UINT` functions](https://github.com/tikv/tikv/pull/5141)
- [Make the Coprocessor DAG independent of `tikv::storage`](https://github.com/tikv/tikv/pull/5143)
- [Add the document information with the note on the document migration](https://github.com/tikv/tikv/pull/5150)
- [Assign a structure for the `KeyIsLocked` content](https://github.com/tikv/tikv/pull/5152)
- [Move the raftkv from `storage` to `server`](https://github.com/tikv/tikv/pull/5153)
- [Extract the Coprocessor DAG](https://github.com/tikv/tikv/pull/5155)
- [Remove the expire-timer](https://github.com/tikv/tikv/pull/5156)
- [Eliminate `CleanUpWaitFor` when the waiter timeouts](https://github.com/tikv/tikv/pull/5157)
- [Pass `Config` when creating `WaiterManager` and `Detector`](https://github.com/tikv/tikv/pull/5162)

## Fixed

- [Fix the filter of the replica checker](https://github.com/pingcap/pd/pull/1660)
- [Update the `rust-rocksdb` dependency and fix the compilation error on `gcc9.1`](https://github.com/tikv/tikv/pull/5164)
- [Fix the issue that `merge` might crash in extreme conditions](https://github.com/tikv/tikv/pull/4595)
- [Remove the unexpected `fmt.Sprintf`](https://github.com/pingcap/pd/pull/1651)

# New contributors (Thanks!)

tikv:

* [jiyingtk](https://github.com/jiyingtk)

tidb-operator:

* [yeya24](https://github.com/yeya24)

parser:

* [imtsuki](https://github.com/imtsuki)
* [leiysky](https://github.com/leiysky)

docs:

* [wolfstudy](https://github.com/wolfstudy)
