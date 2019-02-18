---
title: Weekly update (February 11 ~ February 17, 2019)
date: 2019-02-18
summary: Last week, we landed 50 PRs in the TiDB repository, 2 PRs in the TiSpark repository, and 16 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [50 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-02-11..2019-02-17+) in the TiDB repository.

## Added

- [Support the `BENCHMARK()` built-in function](https://github.com/pingcap/tidb/pull/9252)
- [Add count metrics for statistics feedback indicating estimation inaccuracy](https://github.com/pingcap/tidb/pull/9209)
- [Propose the design for skyline pruning](https://github.com/pingcap/tidb/pull/9184)
- [Add the privilege check for querying `View`](https://github.com/pingcap/tidb/pull/9194)
- [Add the privilege check for creating `View`](https://github.com/pingcap/tidb/pull/9153)
- [Add metrics reflecting QPS at the database level](https://github.com/pingcap/tidb/pull/9151)
- [Add benchmarks utilities for aggregation](https://github.com/pingcap/tidb/pull/8998)
- [Add the `JSON_QUOTE()` built-in function](https://github.com/pingcap/tidb/pull/7832/files)

## Improved

- [Improve the compatibility of the error code with MySQL](https://github.com/pingcap/tidb/pull/9294)
- [Improve the compatibility of the error message with MySQL](https://github.com/pingcap/tidb/pull/9291)
- [Handle `DNF` expressions when computing selectivity](https://github.com/pingcap/tidb/pull/9282)
- [Reduce the memory usage when inserting many rows in one transaction](https://github.com/pingcap/tidb/pull/9272)
- [Refine the `Explain` output for `Window` functions](https://github.com/pingcap/tidb/pull/9270)
- [Improve the compatibility of `SHOW CREATE TABLE` with MySQL](https://github.com/pingcap/tidb/pull/9229)
- [Handle the `enum` type in the `VALUES()` built-in function](https://github.com/pingcap/tidb/pull/9225)
- [Extract the `Scalar` function to a Projection operator for computing](https://github.com/pingcap/tidb/pull/9197)
- [Make the batch gRPC strategy self-adaptable](https://github.com/pingcap/tidb/pull/9169)
- [Improve the compatibility of `DATA_ADD` with MySQL](https://github.com/pingcap/tidb/pull/8988)

## Fixed

- [Fix the wrong result when converting "0000" to the `year` type](https://github.com/pingcap/tidb/pull/9250)
- [Fix precision of default values of the `time` type](https://github.com/pingcap/tidb/pull/9249)
- [Make the `hach.String()` function safe](https://github.com/pingcap/tidb/pull/9230)
- [Handle errors when adding an index to a generated column](https://github.com/pingcap/tidb/pull/9216)
- [Back off when the requested Region epoch is ahead of the Region meta returned from TiKV](https://github.com/pingcap/tidb/pull/9181)
- [Fix the panic when the `Equal` condition of `Join` contains the `Scalar` function](https://github.com/pingcap/tidb/pull/9066)

# Weekly update in TiSpark

Last week, we landed [2 PRs](https://github.com/pingcap/tispark/pulls?utf8=✓&q=is%3Apr+is%3Amerged+merged%3A2019-02-11..2019-02-17+) in the TiSpark repository.

## Fixed

- [Fix the reading data bug when using an index on the partition table](https://github.com/pingcap/tispark/pull/566)

# Weekly update in TiKV and PD

Last week, we landed [16 PRs](https://github.com/search?p=2&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-02-11..2019-02-17&type=Issues) in the TiKV and PD repositories.

## Added

* [Add `checked_add` and `check_sub` Coprocessor pushdown functions](https://github.com/pingcap/tikv/pull/4147)
* [Add the `sub_duration_and_duration` Coprocessor pushdown function](https://github.com/pingcap/tikv/pull/4187)
* [Add code of conduct for contributors](https://github.com/pingcap/tikv/pull/4216)

## Improved

* [Enable auto compactions in the import mode](https://github.com/pingcap/tikv/pull/4086)

# New contributors (Thanks!)

tidb:

- [haplone](https://github.com/haplone)
- [overbool](https://github.com/overbool)
- [u5surf](https://github.com/u5surf)
- [wuudjac](https://github.com/wuudjac)

tikv:

- [caohe](https://github.com/caohe)

parser:

- [eiantee](https://github.com/eiantee)

docs-cn:

- [bigzuo](https://github.com/bigzuo)