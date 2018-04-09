---
title: Weekly update (Apr. 02 ~ Apr. 08, 2018)
date: 2018-04-09
summary: Last week, we landed 28 PRs in the TiDB repositories, 1 PR in the TiSpark repositories, and 9 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [28 PRs](https://github.com/search?p=1&q=repo%3Apingcap%2Ftidb+is%3Apr+is%3Amerged+merged%3A2018-04-02..2018-04-08&type=Issues&utf8=%E2%9C%93) in the TiDB repositories.

## Added

- [Support `AdminCleanupIndex` to clean up the dangling index](https://github.com/pingcap/tidb/pull/6102)
- [Support `AlterTableComment`](https://github.com/pingcap/tidb/pull/6127)
- [Add `RawDeleteRange` API](https://github.com/pingcap/tidb/pull/6157)
- [Make `session transaction isolation level` take effect only once](https://github.com/pingcap/tidb/pull/6175)-

## Fixed

- [Fix row estimation for the pseudo unique key](https://github.com/pingcap/tidb/pull/6199)
- [Fix row count estimation for the column with null values](https://github.com/pingcap/tidb/pull/6203)
- [Fix the result of `cast (0x10 as binary(2))`](https://github.com/pingcap/tidb/pull/6211)
- [Fix zero value issue for binary type](https://github.com/pingcap/tidb/pull/6213)
- [Merge `BatchGet` results to fix `InsertIgnore` in a transaction block](https://github.com/pingcap/tidb/pull/6215)-

## Improved

- [Track memory usage for `NestedLoopApply`](https://github.com/pingcap/tidb/pull/6171)
- [Delete ranges when rolling back `add index`](https://github.com/pingcap/tidb/pull/6188)
- [Optimize the insert executor on duplicate key update](https://github.com/pingcap/tidb/pull/6194)
- [Upgrade mysql.db user column length to 32](https://github.com/pingcap/tidb/pull/6209)

# Weekly update in TiSpark

Last week, we landed [1 PR](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-04-02..2018-04-08) in the TiSpark repositories.

## Added

- [Fix single read for count(1) case](https://github.com/pingcap/tispark/pull/304)

# Weekly update in TiKV and PD

Last week, we landed [9 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-04-02..2018-04-08) in the TiKV and PD repositories.

## Added

- [Support `compact_region` by `tikv-ctl`](https://github.com/pingcap/tikv/pull/2889)
- [Add `ImportKVService`](https://github.com/pingcap/tikv/pull/2881)
- [Add raw batch `put`/`get`/`delete`/`scan`](https://github.com/pingcap/tikv/pull/2854)

## Fixed

- [Fix OOM when receiving too many snapshots](https://github.com/pingcap/tikv/pull/2879)

## Improved

- [Update MVCC debug structure](https://github.com/pingcap/tikv/pull/2894)

# New contributors (Thanks!)

TiKV:

- [Xiaoguang Sun](https://github.com/sunxiaoguang)
- [Matt Friedman](https://github.com/friedm)

Docs:

- [Valerian Pereira](https://github.com/valerianpereira)