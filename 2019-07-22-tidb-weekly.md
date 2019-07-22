---
title: Weekly update (July 15 ~ July 21, 2019)
date: 2019-07-22
summary: Last week, we landed 68 PRs in the TiDB repository, 9 PRs in the TiSpark repository, and 39 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [68 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-07-15..2019-07-21+) in the TiDB repository.

## Added

- [Add the `SHOW TABLE REGIONS` syntax](https://github.com/pingcap/tidb/pull/10612)
- [Add support for `MAX_EXECUTION_TIME`](https://github.com/pingcap/tidb/pull/11026)

## Improved

- [Add `TiKVTxnCmdCounter` to metrics](https://github.com/pingcap/tidb/pull/11292)
- [Refine the multi-query response of the text protocol](https://github.com/pingcap/tidb/pull/11263)
- [Refine the output format for the tidb-specific variables of boolean type](https://github.com/pingcap/tidb/pull/11239)
- [Parse and ignore `PARTITION BY LIST`](https://github.com/pingcap/tidb/pull/11236)
- [Improve the calculation of column size](https://github.com/pingcap/tidb/pull/11091)
- [Avoid sending a signal to the `w.done` channel everywhere in the `runGCJob` function](https://github.com/pingcap/tidb/pull/11032)

## Fixed

- [Fix the error that occurs when executing two DDL operations in parallel](https://github.com/pingcap/tidb/pull/11341)
- [Fix `getIntervalFromDecimal` in `DATE_ADD()`](https://github.com/pingcap/tidb/pull/11297)
- [Fix the microseconds behavior in `DATE_ADD()`](https://github.com/pingcap/tidb/pull/11280)
- [Fix the error that occurs when converting string to float or integer](https://github.com/pingcap/tidb/pull/10861)
- [Fix the issue that `SUBTIME ADDTIME` returns `NULL` with a warning](https://github.com/pingcap/tidb/pull/11262)
- [Fix the issue that the `Mod(%)`, `Multiple(*)` and `Minus(-)` operators meet inconsistent `0` results](https://github.com/pingcap/tidb/pull/11251)
- [Disable the projection elimination for the `Select` plan of `Update`](https://github.com/pingcap/tidb/pull/10962)
- [Fix the error in the `NAME_CONST` function](https://github.com/pingcap/tidb/pull/11241)
- [Change the order of error judgement](https://github.com/pingcap/tidb/pull/11237)
- [Fix the overflow check of `types/convert.go::floatStrToIntStr`](https://github.com/pingcap/tidb/pull/11114)

# Weekly update in TiSpark

Last week, we landed [9 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-07-15..2019-07-21+) in the TiSpark repository.

## Fixed

- [Fix an improper response with the Region error](https://github.com/pingcap/tispark/pull/922)

## Added

- [Add the support for splitting index Regions if the schema has any index](https://github.com/pingcap/tispark/pull/909)

# Weekly update in TiKV and PD

Last week, we landed [39 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-07-15..2019-07-21&type=Issues) in the TiKV and PD repositories.

## Improved

- [Make a tiny refactor for `prewrite`](https://github.com/tikv/tikv/pull/5100)
- [Improve the performance of `detect`](https://github.com/tikv/tikv/pull/5079)
- [Support `follower_read`](https://github.com/tikv/tikv/pull/5051)
- [Return `RegionError` when TiKV is closing](https://github.com/tikv/tikv/pull/4818)
- [Refactor the `convert to uint` functions](https://github.com/tikv/tikv/pull/4987)

## Added

- [Add the `to_numeric_string` method for `Duration`/`DateTime`](https://github.com/tikv/tikv/pull/5006)
- [Add benchmarks for `rollback`](https://github.com/tikv/tikv/pull/4459)
- [Add the `cast * as int` RPN functions](https://github.com/tikv/tikv/pull/5099)
- [Add the `in_union` utility method for `RpnFnCallExtra/ScalarFunc`](https://github.com/tikv/tikv/pull/5090)

## Fixed

- [Fix the problem of double running nodes](https://github.com/tikv/tikv/pull/5080)
- [Fix the format for the Region meta key](https://github.com/pingcap/pd/pull/1627)
- [Remove the `cfg` setting which causes failure in `make test`](https://github.com/tikv/tikv/pull/5102)

# New contributors (Thanks!)

tidb:

- [unknwon](https://github.com/unknwon)
- [wty4427300](https://github.com/wty4427300)

tikv:

- [lucab](https://github.com/lucab)

parser:

- [gleonid](https://github.com/gleonid)
