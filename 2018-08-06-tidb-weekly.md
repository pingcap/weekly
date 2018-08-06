---
title: Weekly update (July 30 ~ August 05, 2018)
date: 2018-08-06
summary: Last week, we landed 68 PRs in the TiDB repositories and 30 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [68 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-07-30..2018-08-05+) in the TiDB repositories. 

## Added

- [Support the `Delete` operation for table partition](https://github.com/pingcap/tidb/pull/7147)
- [Support analyzing the partition table](https://github.com/pingcap/tidb/pull/7190)

## Fixed

- [Fix the union result when mixing signed and unsigned columns](https://github.com/pingcap/tidb/pull/7112)
- [Add `BatchPut` for `RawKV`](https://github.com/pingcap/tidb/pull/7135)
- [Fix a bug about wrong copying in index join](https://github.com/pingcap/tidb/pull/7150)
- [Fix a panic caused by the local feedback](https://github.com/pingcap/tidb/pull/7152)
- [Fix a bug in decimal multiplication](https://github.com/pingcap/tidb/pull/7208)
- [Sort user records in the privilege cache](https://github.com/pingcap/tidb/pull/7211)
- [Fix `TruncateTo`](https://github.com/pingcap/tidb/pull/7234)
- [Fix a bug of update with an outer join](https://github.com/pingcap/tidb/pull/7177)
- [Fix `admin cleanup index` for non-unique handles in a unique index](https://github.com/pingcap/tidb/pull/7248)
- [Fix a bug when eliminating a projection](https://github.com/pingcap/tidb/pull/7257/files)
- [Skip inner rows when the join keys contain `NULL`](https://github.com/pingcap/tidb/pull/7255)

## Improved

- [Support fast path point select](https://github.com/pingcap/tidb/pull/6937)
- [Always choose the smaller child as the outer table for `IndexJoin`](https://github.com/pingcap/tidb/pull/7019)
- [Remove `FromID` from `expression.Column`](https://github.com/pingcap/tidb/pull/7157)
- [Add default value check of the primary key when creating a table](https://github.com/pingcap/tidb/pull/7169)
- [Use the revive linter](https://github.com/pingcap/tidb/pull/7197)

# Weekly update in TiKV and PD

Last week, we landed [30 PRs](https://github.com/search?p=2&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-07-30..2018-08-05&type=Issues) in the TiKV and PD repositories.

## Added

- [Support specifying the time zone by name](https://github.com/pingcap/tikv/pull/3281)
- [Add etcd Raft state metrics](https://github.com/pingcap/pd/pull/1172)
- [Add hierarchy in the error code](https://github.com/pingcap/pd/pull/1156)

## Fixed

- [Fix the issue that the operator kind is not set correctly](https://github.com/pingcap/pd/pull/1176)
- [Fix a bug in `from_bytes`](https://github.com/pingcap/tikv/pull/3377)
- [Perform GC on stale peers which send pre-vote messages](https://github.com/pingcap/tikv/pull/3369)

## Improved

- [Use `RangeProperties` instead of `SizeProperties`](https://github.com/pingcap/tikv/pull/3322)
- [Optimize `scan_lock`](https://github.com/pingcap/tikv/pull/3350)
- [Refactor Row in the executor](https://github.com/pingcap/tikv/pull/3359)
- [Avoid reading etcd if possible](https://github.com/pingcap/pd/pull/1164)
- [Reduce `Key` related `memcpy`](https://github.com/pingcap/tikv/pull/3372)
- [Export the `seek_region` interface](https://github.com/pingcap/tikv/pull/3107)

# New contributors (Thanks!)

TiDB:

- [hhxcc](https://github.com/hhxcc)

TiKV:

- [TennyZhuang](https://github.com/TennyZhuang)
- [lerencao](https://github.com/lerencao)

TiSpark:

- [ariesdevil](https://github.com/ariesdevil)

docs-cn:

- [motian](https://github.com/motian)