---
title: Weekly update (September 24 ~ October 14, 2018)
date: 2018-10-15
summary: Last three weeks, we landed 74 PRs in the TiDB repository, 4 PRs in the TiSpark repository, and 42 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last three weeks, we landed [74 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-09-24..2018-10-14+) in the TiDB repository.

## Added

* [Add a session variable `tidb_enable_cascades_planner`](https://github.com/pingcap/tidb/pull/7879)
* [Make `explain` support `explain analyze`](https://github.com/pingcap/tidb/pull/7827)
* [Calculate radix bit number before building a hash table](https://github.com/pingcap/tidb/pull/7816)
* [Add a benchmark test case of a complex query for the parser](https://github.com/pingcap/tidb/pull/7815)
* [Support `autoAnalyze` for partitioned tables](https://github.com/pingcap/tidb/pull/7789)
* [Add a `force-priority` option to the configuration file](https://github.com/pingcap/tidb/pull/7777)
* [Add metrics for slow query logs](https://github.com/pingcap/tidb/pull/7759)
* [Add a built-in function `json_length`](https://github.com/pingcap/tidb/pull/7739)
* [Redesign the latch scheduler](https://github.com/pingcap/tidb/pull/7711)
* [Add the `admin show slow` command](https://github.com/pingcap/tidb/pull/7785)

## Improved

* [Support `IndexJoin` over `UnionScan`](https://github.com/pingcap/tidb/pull/7877)
* [Improve the precision for the `Avg` aggregation function](https://github.com/pingcap/tidb/pull/7860)
* [Refine `chunk.SwapColumn` to rebuild the column reference](https://github.com/pingcap/tidb/pull/7848)
* [Build the `anti semi join` plan for `NOT EXISTS`](https://github.com/pingcap/tidb/pull/7842)
* [Refine `chunk.SwapColumn` to rebuild the column reference](https://github.com/pingcap/tidb/pull/7841)
* [Make the `sysdate` built-in function unfoldable](https://github.com/pingcap/tidb/pull/7838)
* [Improve the `INFORMATION_SCHEMA.ENGINES` table compatibility](https://github.com/pingcap/tidb/pull/7831)
* [Improve the warning and error information for the `group_concat()` built-in function](https://github.com/pingcap/tidb/pull/7799)
* [Change the default value of the `performance_schema` session variable to `OFF`](https://github.com/pingcap/tidb/pull/7788)
* [Support `show create table` with the Compression option](https://github.com/pingcap/tidb/pull/7782)
* [Optimize `regionErr`, `notLeader`, and `staleEpoch` error handling](https://github.com/pingcap/tidb/pull/7775)
* [Speed up the recovery when the PD leader is down](https://github.com/pingcap/tidb/pull/7774)
* [Support building TiDB on Windows operation system](https://github.com/pingcap/tidb/pull/7773)
* [Allow `alter table` to append values to an enum typed column](https://github.com/pingcap/tidb/pull/7767)
* [Return a `table dual` logical plan when the filter is `false` or `null`](https://github.com/pingcap/tidb/pull/7756)
* [Refine the handle check to use the `point get` plan for a prepared statement](https://github.com/pingcap/tidb/pull/7732)
* [Change `FLUSH TABLES WITH READ LOCK` to produce an error](https://github.com/pingcap/tidb/pull/7712)
* [Remove some useless code and avoid some redundancy check](https://github.com/pingcap/tidb/pull/7639)
* [Use the chunk `grow` for a simple executor](https://github.com/pingcap/tidb/pull/7540)

## Fixed

* [Fix a parser bug that an empty string in the `ESCAPED BY` subclause of `FIELDS` causes a panic](https://github.com/pingcap/tidb/pull/7880)
* [Fix the statistics updating bug when there is no `stats worker`](https://github.com/pingcap/tidb/pull/7871)
* [Fix the memory leak issue in statistics](https://github.com/pingcap/tidb/pull/7864)
* [Check the privilege for `show processlist`](https://github.com/pingcap/tidb/pull/7858)
* [Fix the log format for `gc worker`](https://github.com/pingcap/tidb/pull/7852)
* [Fix a panic by avoiding the Send operation on the closed slow query channel](https://github.com/pingcap/tidb/pull/7847)
* [Fix the results of the `Command` and `Time` fields in `show processlist`](https://github.com/pingcap/tidb/pull/7844)
* [Fix the issue that the float type does not take effect in `AddDate` and `SubDate` built-in functions](https://github.com/pingcap/tidb/pull/7840)
* [Exclude `IsNull` from the constant propagation](https://github.com/pingcap/tidb/pull/7835)
* [Fix a bug in `admin check table`](https://github.com/pingcap/tidb/pull/7818)
* [Return an error when the argument of the `VALUES()` function is not a column](https://github.com/pingcap/tidb/pull/7817)
* [Fix the combined index low-bound check in statistics](https://github.com/pingcap/tidb/pull/7814)
* [Fix a panic in the `substring_index` built-in function](https://github.com/pingcap/tidb/pull/7806)
* [Fix the `show create table` result when the table has a Compression option](https://github.com/pingcap/tidb/pull/7793)
* [Fix an issue of casting an unsigned integer to a decimal](https://github.com/pingcap/tidb/pull/7792)
* [Fix a panic when the values for the `PointGet` operator are all null](https://github.com/pingcap/tidb/pull/7790)
* [Fix the compatibility issue that updating the subquery table should be forbidden](https://github.com/pingcap/tidb/pull/7783)
* [Fix some corner cases when parsing a string to a datetime](https://github.com/pingcap/tidb/pull/7701)
* [Fix `alter table add index` on a virtual column bug](https://github.com/pingcap/tidb/pull/7575)

# Weekly update in TiSpark

Last three weeks, we landed [4 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftispark+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-09-24..2018-10-14&type=Issues) in the TiSpark repository.

## Added

- [Update Spark support to Spark 2.3](https://github.com/pingcap/tispark/pull/360)

## Fixed

- [Fix the date timezone in tests](https://github.com/pingcap/tispark/pull/421)
- [Fix an issue that Explain statements do not work in Spark 2.3](https://github.com/pingcap/tispark/pull/456)

# Weekly update in TiKV and PD

Last three weeks, we landed [42 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-09-24..2018-10-14&type=Issues) in the TiKV and PD repositories.

## Added

- Support more functions in Coprocessor:
    
    * [`InetAton`](https://github.com/tikv/tikv/pull/3659)
    * [`InetNtoa`](https://github.com/tikv/tikv/pull/3659)
    * [`Concat`](https://github.com/tikv/tikv/pull/3654)
    * [`Right`](https://github.com/tikv/tikv/pull/3653)
    * [`Sha2`](https://github.com/tikv/tikv/pull/3649)
    * [`TruncateDecimal`](https://github.com/tikv/tikv/pull/3637)
    * [`TruncateReal`](https://github.com/tikv/tikv/pull/3633)
    * [`Year`](https://github.com/tikv/tikv/pull/3622)
    * [`RouldReal`](https://github.com/tikv/tikv/pull/3621)
    * [`RoundDec`](https://github.com/tikv/tikv/pull/3621)
    * [`RoundWithFracDec`](https://github.com/tikv/tikv/pull/3621)
    * [`RoundWithFracInt`](https://github.com/tikv/tikv/pull/3621)
    * [`RoundWithFracReal`](https://github.com/tikv/tikv/pull/3621)
    * [`TruncateInt`](https://github.com/tikv/tikv/pull/3532)
- [Fuzz `codec::number`](https://github.com/tikv/tikv/pull/3668)
- [Add `RegionChangeObserver`](https://github.com/tikv/tikv/pull/3634)
- [Get Regions with the top size](https://github.com/pingcap/pd/pull/1254)

## Fixed

- [Fix the hanging problem when etcd fails to start](https://github.com/pingcap/pd/pull/1267)
- [Fix an issue of parsing a datetime from a string](https://github.com/tikv/tikv/pull/3589)

## Improved

- [Improve the performance of Coprocessors `md5` and `sha1`](https://github.com/tikv/tikv/pull/3644)
- [Unify the PD logger](https://github.com/pingcap/pd/pull/1257)
- [Check the level 0 files before ingesting](https://github.com/tikv/tikv/pull/3606)
- [Integrate the error code with `pkg`/errors to provide error tracing](https://github.com/pingcap/pd/pull/1200)
- [Upgrade Golang gRPC to 1.12.2](https://github.com/pingcap/pd/pull/1265)
- [Upgrade Rust gRPC to 0.4.0](https://github.com/tikv/tikv/pull/3650)

# New contributors (Thanks!)

tikv:

- [Kingwl](https://github.com/Kingwl)
- [colinback](https://github.com/colinback)

docs-cn:

- [mccxj](https://github.com/mccxj)
- [sweetIan](https://github.com/sweetIan)