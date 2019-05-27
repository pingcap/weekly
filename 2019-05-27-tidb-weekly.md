---
title: Weekly update (May 20 ~ May 26, 2019)
date: 2019-05-27
summary: Last week, we landed 44 PRs in the TiDB repository, 17 PRs in the TiSpark repository, and 45 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [44 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-05-20..2019-05-26) in the TiDB repository.

## Added

- [Support the `tidb_txn_mode` session variable](https://github.com/pingcap/tidb/pull/10574)
- [Support `dump`/`load` correlation of statistics histograms](https://github.com/pingcap/tidb/pull/10573)
- [Add a `make ddltest` target to generate `ddltest` binary data](https://github.com/pingcap/tidb/pull/10542)
- [Add the `tidb_low_resolution_tso` session variable for reading data with low resolution TSO]((https://github.com/pingcap/tidb/pull/10428))
- [Support `View` related privileges in `mysql.tables_priv`](https://github.com/pingcap/tidb/pull/9894)
- [Support `LOAD DATA...IGNORE/REPLACE` in the syntax](https://github.com/pingcap/tidb/pull/10336)

## Improved

- [Make pessimistic lock `TTL` easier to set and validate the value](https://github.com/pingcap/tidb/pull/10578)
- [Refine the error message in latches](https://github.com/pingcap/tidb/pull/10566)
- [Enhance index join for more scenarios](https://github.com/pingcap/tidb/pull/10540)
- [Update `2019-04-11-indexmerge.md` with some edits](https://github.com/pingcap/tidb/pull/10530)
- [Fix a potential goroutine leak in `distSQL`](https://github.com/pingcap/tidb/pull/10557)
- [Add a flag to indicate that the TiDB server is closing](https://github.com/pingcap/tidb/pull/10511)
- [Validate table information before doing DDL jobs to avoid potential loading `infoschema` errors](https://github.com/pingcap/tidb/pull/10464)
- [Merge Window functions with the same specification name](https://github.com/pingcap/tidb/pull/9866)
- [Only retry needed Regions when getting Region row count during fast `Analyze`](https://github.com/pingcap/tidb/pull/10429)
- [Cache the vendor to speed up Docker building](https://github.com/pingcap/tidb/pull/10296)

## Fixed

- [Correct the behavior of the `IndexJoin` hint for `SemiJoin`](https://github.com/pingcap/tidb/pull/10583)
- [Fix `notLeader` in the Region cache](https://github.com/pingcap/tidb/pull/10572)
- [Fix the `show grants` result for RBAC](https://github.com/pingcap/tidb/pull/10571)
- [Fix the issue that the OOM panic is not recovered currently in the distSQL layer](https://github.com/pingcap/tidb/pull/10544)
- [Fix a bug in the `AlterSchema` job and add more tests](https://github.com/pingcap/tidb/pull/10529)
- [Check the table name for columns in the partition expression](https://github.com/pingcap/tidb/pull/10499)
- [Fix the issue that `ByItem` does not filter `NULL` out](https://github.com/pingcap/tidb/pull/10488)
- [Fix the issue that canceling range tasks might not return errors](https://github.com/pingcap/tidb/pull/10519)
- [Fix a `GetPartition` function bug when adding indexes](https://github.com/pingcap/tidb/pull/10475)
- [Fix the issue that the maximum value of UINT64 is returned when `-1` is used for `point-get`](https://github.com/pingcap/tidb/pull/10113)
- [Fix the issue that TiDB cannot be used for a long time under extreme conditions if relying only on the information in PD](https://github.com/pingcap/tidb/pull/10256)

# Weekly update in TiSpark

Last week, we landed [17 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-05-20..2019-05-26+) in the TiSpark repository.

## Fixed

- [Fix index scans on partition tables](https://github.com/pingcap/tispark/pull/735)
- [Fix the issue that `RegionVerId` missed to implement `equals()`](https://github.com/pingcap/tispark/pull/739)
- [Fix the issue that the default value of `Integer` is not parsed to `Long`](https://github.com/pingcap/tispark/pull/741)
- [Fix the issue that `FromSparkType()` incorrectly transforms `Integer` to `Long`](https://github.com/pingcap/tispark/pull/752)
- [Fix the issue that `KeyNotInRegion` might occur when retrieving rows by handles](https://github.com/pingcap/tispark/pull/755)
- [Fix the issue of `encodeValue` with unsigned comparison](https://github.com/pingcap/tispark/pull/761)

# Weekly update in TiKV and PD

Last week, we landed [45 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-05-20..2019-05-26&type=Issues) in the TiKV and PD repositories.

## Added

- [Add the statistics of the store flow](https://github.com/pingcap/pd/pull/1548)
- [Add `BatchSlowHashAggregationExecutor`](https://github.com/tikv/tikv/pull/4752)
- [Add configuration items and enable `pessimistic-txn` by default](https://github.com/tikv/tikv/pull/4741)
- Add RPN functions
	- [`Int`, `Real` and `Decimal`](https://github.com/tikv/tikv/pull/4727)
	- [`IsNull`, `IsTrue` and `IsFalse`](https://github.com/tikv/tikv/pull/4720)
- [Support pessimistic transactions (experimental feature)](https://github.com/tikv/tikv/pull/4698)
- [Add the `ReadIndex` service](https://github.com/tikv/tikv/pull/4672)
- [Add hibernate Regions](https://github.com/tikv/tikv/pull/4591)
- [Add operator limit for stores](https://github.com/pingcap/pd/pull/1474)

## Improved

- [Remove the local reader thread](https://github.com/tikv/tikv/pull/4558)
- [Retry to connect PD for infinity, and log periodically](https://github.com/tikv/tikv/pull/4502)
- [Remove the scheduler thread](https://github.com/tikv/tikv/pull/4098)

## Fixed

- [Fix the issue that snapshots might lose some applied results](https://github.com/tikv/tikv/pull/4716)

# New contributors (Thanks!)

tidb:

- [sundl123](https://github.com/sundl123)
- [sunxiaoguang](https://github.com/sunxiaoguang)

tikv:

- [wjhuang2016](https://github.com/wjhuang2016)

parser:

- [sundl123](https://github.com/sundl123)
