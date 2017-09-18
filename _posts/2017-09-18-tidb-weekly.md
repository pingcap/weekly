---
layout: post
title: Weekly Update
---

# Weekly update in TiDB

2017-09-18

Last week, we landed [46 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-09-11..2017-09-17%20) in the TiDB repositories.

## Added
* [Add required tables of MySQLX .](https://github.com/pingcap/tidb/pull/4521)
* [Add TOML configuration file support.](https://github.com/pingcap/tidb/pull/4509)

## Removed
* [Remove the performance schema instrumentation.](https://github.com/pingcap/tidb/pull/4516)

## Fixed
* [Fix `show create table` with foreign key.](https://github.com/pingcap/tidb/pull/4537)
* [Cast values only for modified columns in the `update` statement to avoid unnecessary check.](https://github.com/pingcap/tidb/pull/4517)
* [Fix an OOM issue when analyzing table.](https://github.com/pingcap/tidb/pull/4515)
* [Fix a `cast (date as datetime)` error.](https://github.com/pingcap/tidb/pull/4484)
* [Fix a bug about the `DATE` literal.](https://github.com/pingcap/tidb/pull/4362)

## Improved
* [Change the `FMSketch` hash function from "fnv" to "murmur".](https://github.com/pingcap/tidb/pull/4541)
* [Add the `PARTITION BY KEY` grammar support.](https://github.com/pingcap/tidb/pull/4539)
* [Refine setting/getting the `SQL_MODE` variable.](https://github.com/pingcap/tidb/pull/4530)
* [Support the `NVARCHAR` syntax.](https://github.com/pingcap/tidb/pull/4500)
* [Refine the parser of `localtime` and `localtimestamp`.](https://github.com/pingcap/tidb/pull/4503)
* [Push down the `ANALYZE INDEX` statement.](https://github.com/pingcap/tidb/pull/4489)
* [Support stream aggregation in the new optimization plan.](https://github.com/pingcap/tidb/pull/4481)
* [Hide the security information in `SHOW PROCESSLIST`.](https://github.com/pingcap/tidb/pull/4451)
* [Add a goroutine pool package utility.](https://github.com/pingcap/tidb/pull/3752)
* Refactor the following expression/builtin-function evaluation framework:
    - [ADDDATE, SUBDATE](https://github.com/pingcap/tidb/pull/4504)
    - [TIMEDIFF](https://github.com/pingcap/tidb/pull/4496)
    - [VALUES](https://github.com/pingcap/tidb/pull/4491)
    - [ROW](https://github.com/pingcap/tidb/pull/4480)
    - [SETVAR, GETVAR](https://github.com/pingcap/tidb/pull/4479)
    - [GREATEST, LEAST](https://github.com/pingcap/tidb/pull/4476)
    - [CONVERT_TZ](https://github.com/pingcap/tidb/pull/4463)
    - [MAKETIME](https://github.com/pingcap/tidb/pull/4396)
    - [ADDTIME, SUBTIME](https://github.com/pingcap/tidb/pull/4333)

# Weekly update in TiSpark

## Added
* Add the [JDBC Thrift Server / spark-sql support](https://github.com/pingcap/tispark/pull/36)
* Add the [back-off retry policy](https://github.com/pingcap/tikv-client-lib-java/pull/104)
* Add the [Meta table prefix support](https://github.com/pingcap/tispark/pull/43)

## Fixed
* Fix the [Null decoding error.](https://github.com/pingcap/tikv-client-lib-java/pull/100)
* Fixed some [Styling issues](https://github.com/pingcap/tispark/pull/38)

## Improved
* Added the [Integration test framework](https://github.com/pingcap/tispark/pull/32)

## New contributors (Thanks!)
* https://github.com/liancheng


# Weekly update in TiKV

Last week, We landed [34 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-09-11..2017-09-17&type=Issues) in the TiKV repositories.

## Added

* Balance regions [based on the read flow](https://github.com/pingcap/pd/pull/708).
* Make [the Raft tick configurable](https://github.com/pingcap/pd/pull/743) for PD.
* Add a [classifier interface](https://github.com/pingcap/pd/pull/745) for namespace.
* [Balance by the namespace](https://github.com/pingcap/pd/pull/754).

## Fixed

* Fix [a race condition for threadpool](https://github.com/pingcap/tikv/pull/2266).
* Fix the active [region statistics](https://github.com/pingcap/pd/pull/744).
* Fix [cleaning up data](https://github.com/pingcap/tikv/pull/2273) between regions.
* [Stop the threadpool](https://github.com/pingcap/tikv/pull/2275) before quitting the scheduler.
* Fix the [marshal operator](https://github.com/pingcap/pd/pull/746).
* Fix [the timeout operator](https://github.com/pingcap/pd/pull/749).
* Fix [a but in `cast_str_as_int`](https://github.com/pingcap/tikv/pull/2296).
* [Wrap `InitLogger`](https://github.com/pingcap/pd/pull/753) in `sync.Once` for thread safety.
* Fix [a compiling error](https://github.com/pingcap/tikv/pull/2304).


## Improved

* Add tests for the [gRPC services](https://github.com/pingcap/tikv/pull/2244).
* Add [two queues cache](https://github.com/pingcap/pd/pull/741) for PD.
* Cache elf sections for [backtrace](https://github.com/pingcap/tikv/pull/2265).
* [Optimize JSON](https://github.com/pingcap/tikv/pull/2267).
* Skip checking [region 0](https://github.com/pingcap/tikv/pull/2276).
* Adjust [metrics](https://github.com/pingcap/tikv/pull/2280) for the coprocessor.
* [Remove the stale peers](https://github.com/pingcap/tikv/pull/2281) as soon as possible.
* [Enable `pin_l0_filter_and_index`](https://github.com/pingcap/tikv/pull/2288) by default.
* Enhance [metrics](https://github.com/pingcap/tikv/pull/2291) for the scheduler.
* Optimize [the `LIKE` expression](https://github.com/pingcap/tikv/pull/2293).
* [Check the leader request](https://github.com/pingcap/tikv/pull/2294) when becoming a follower after receiving message with higher term.
* Use [`util::time::instant`](https://github.com/pingcap/tikv/pull/2295) instead of `std::time::instant`.
* Add [metrics for compression ratio](https://github.com/pingcap/tikv/pull/2297) at different levels.
* Remove the [statistics that may overflow](https://github.com/pingcap/tikv/pull/2304).

## New contributors  (Thanks!)
* https://github.com/blacktear23
* https://github.com/qqsun8819