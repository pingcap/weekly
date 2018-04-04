---
title: Weekly update (March 26 ~ April 01, 2018)
date: 2018-04-02
summary: Last week, we landed 49 PRs in the TiDB repositories, 6 PRs in the TiSpark repositories, and 21 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [49 PRs](https://github.com/search?p=5&q=repo%3Apingcap%2Ftidb+is%3Apr+is%3Amerged+merged%3A2018-03-26..2018-04-01&type=Issues&utf8=%E2%9C%93) in the TiDB repositories.

## Added

- [Support `show grants for current_user();`](https://github.com/pingcap/tidb/pull/5697)
- [Add manual GC back for some KV API users](https://github.com/pingcap/tidb/pull/6123)
- [Support using decimal in `INTERNAL`](https://github.com/pingcap/tidb/pull/6143)

## Fixed

- [Fix an unsigned decimal](https://github.com/pingcap/tidb/pull/6104)
- [Fix a potential goroutine leak problem in `copIterator`](https://github.com/pingcap/tidb/pull/6140)
- [Fix the `AdminCheckTable` bug when the column is nil and has a default value](https://github.com/pingcap/tidb/pull/6142)
- [Fix type infer for the binary literal](https://github.com/pingcap/tidb/pull/6151)
- [Fix a bug that `lexer.Reset()` cannot be reset to the initial state](https://github.com/pingcap/tidb/pull/6153)
- [Handle the truncate error in `BinaryLiteral.ToInt`](https://github.com/pingcap/tidb/pull/6163)
- [Fix a bug when applying the `top-n push down` rule](https://github.com/pingcap/tidb/pull/6187)

## Improved

- [Recover a panic in adding index workers](https://github.com/pingcap/tidb/pull/6132)
- [Improve performance of `DecodeBytes` in `DecodeOneToChunk`](https://github.com/pingcap/tidb/pull/6135)
- [Use scientific notation to format float value](https://github.com/pingcap/tidb/pull/6160)
- [Check the gRPC error message before returning a critical error](https://github.com/pingcap/tidb/pull/6179)

# Weekly update in TiSpark

Last week, we landed [6 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-03-26..2018-04-01) in the TiSpark repositories.

## Fixed

- [Fix excessive dag columns](https://github.com/pingcap/tispark/pull/297/files)
- [Fix `estimatedRowCount` when the pushdown predicate is not present](https://github.com/pingcap/tispark/pull/294)

# Weekly update in TiKV and PD

Last week, we landed [21 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-03-26..2018-04-01) in the TiKV and PD repositories.

## Added

- [Add import-mode arguments to tune configurations for importing data](https://github.com/pingcap/tikv/pull/2875)
- [Add `RegionOption` for picking Region randomly](https://github.com/pingcap/pd/pull/1005)
- [Add the diagnose API](https://github.com/pingcap/pd/pull/1004)
- [Set `eval_warnings` in `SelectResponse.warnings` or `StreamResponse.warnings`](https://github.com/pingcap/tikv/pull/2858)
- [Clean up obsoleted SST files periodically](https://github.com/pingcap/tikv/pull/2839)
- [Initiate the half split Region](https://github.com/pingcap/tikv/pull/2790)
- [Support `admin` splitting Region](https://github.com/pingcap/pd/pull/947)

## Fixed

- [Remove redundant configuration](https://github.com/pingcap/tikv/pull/2884)
- [Fix the bug of `ThreadSafeCache Get` method lock](https://github.com/pingcap/pd/pull/1008)
- [Fix metrics of the replica checker](https://github.com/pingcap/pd/pull/1007)
- [Fix a bug of `config show all`](https://github.com/pingcap/pd/pull/1006)

## Improved

- [Relax the abnormal leader missing check](https://github.com/pingcap/tikv/pull/2867)
- [Make sending snapshots asynchronous in a `CpuPool`](https://github.com/pingcap/tikv/pull/2850)
- [Avoid passing `CpuPool` into `OnResponse`](https://github.com/pingcap/tikv/pull/2841)

# New contributors (Thanks!)

TiDB:

- [chenyangyang](https://github.com/chenyang8094)
- [何晨](https://github.com/hechen0)
- [康晓宁](https://github.com/kangxiaoning)

TiKV:

- [MatthiasSchuster](https://github.com/ShalokShalom)
