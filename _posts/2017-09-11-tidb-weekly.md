---
layout: post
title: Weekly Update
---

## Weekly update in TiDB

2017-09-11

Last week, we landed [49 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-09-04..2017-09-10%20) in the TiDB repositories.

## Added
* [Add the column size limit when creating table.](https://github.com/pingcap/tidb/pull/4464)
* [Add the syntax for `admin show ddl jobs`.](https://github.com/pingcap/tidb/pull/4316)
* [SSL/TLS support.](https://github.com/pingcap/tidb/pull/3716)

## Fixed
* [Fix an `ORDER BY` bug.](https://github.com/pingcap/tidb/pull/4470)
* [Add entry limit for transactions when doing DDL job.](https://github.com/pingcap/tidb/pull/4458)
* [Fix a bug during the limit operator pushdown.](https://github.com/pingcap/tidb/pull/4449)
* [Check the default value of the `column` option in the `CREATE TABLE` statement.](https://github.com/pingcap/tidb/pull/4430)
* [Fix the DEFAULT output in `SHOW CREATE TABLE`.](https://github.com/pingcap/tidb/pull/4427)
* [Fix a bug during the TopN operator pushdown.](https://github.com/pingcap/tidb/pull/4420)
* [Fix an OOM issue when analyzing tables in some cases.](https://github.com/pingcap/tidb/pull/4399)


## Improved
* [Do some prework before pushing down the `analyze table` statement.](https://github.com/pingcap/tidb/pull/4471)
* [Rewrite `fieldTp2EvalTp()` to use `mysql.TypeXXX` instead of `TypeClass`.](https://github.com/pingcap/tidb/pull/4467/files)
* [Add timezone for `CastAsTime`.](https://github.com/pingcap/tidb/pull/4465)
* [Rewrite `hashCode()` for `requireProp`.](https://github.com/pingcap/tidb/pull/4460)
* [Use temporary session in gc_worker instead of global singleton.](https://github.com/pingcap/tidb/pull/4453)
* [Change the log package to `logrus`.](https://github.com/pingcap/tidb/pull/4452)
* [Let `allocID()` return int to be more efficient.](https://github.com/pingcap/tidb/pull/4441)
* [Rewrite hex and bit literals implementation.](https://github.com/pingcap/tidb/pull/4415)
* [Support client specified collation.](https://github.com/pingcap/tidb/pull/4409)
* [Refactor `IndexLookUpExecutor`.](https://github.com/pingcap/tidb/pull/4305)
* [Update the `time Add()` implementation.](https://github.com/pingcap/tidb/pull/4267)
* Refactor the following expression/builtin-function evaluation framework:
    - [FROM_UNIXTIME](https://github.com/pingcap/tidb/pull/4454)
    - [EXTRACT](https://github.com/pingcap/tidb/pull/4456)
    - [EXPORT_SET](https://github.com/pingcap/tidb/pull/4434)
    - [GET_FORMAT](https://github.com/pingcap/tidb/pull/4422)
    - [INTERVAL](https://github.com/pingcap/tidb/pull/4421)
    - [FIELD](https://github.com/pingcap/tidb/pull/4419)
    - [CONVERT](https://github.com/pingcap/tidb/pull/4417)
    - [FORMAT](https://github.com/pingcap/tidb/pull/4416)
    - [INSERT](https://github.com/pingcap/tidb/pull/4414)
    - [Builtin abot JSON](https://github.com/pingcap/tidb/pull/4367)
    - [CURRENT_TIME](https://github.com/pingcap/tidb/pull/4360)
    - [TIME_TO_SEC, SEC_TO_TIME](https://github.com/pingcap/tidb/pull/4342)
    - [INTDIV](https://github.com/pingcap/tidb/pull/4213)

## New Contributor (Thanks!)
* [Wang Guoliang](https://github.com/wgliang)

## Weekly update in TiKV

Last week, We landed [32 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-09-04..2017-09-10&type=Issues) in the TiKV repositories.

## Added

* Implement [`div_real` and `div_decimal`](https://github.com/pingcap/tikv/pull/2243) for expression.
* Add [JSON functions](https://github.com/pingcap/tikv/pull/2246) for DAG.
* Add the [LIKE signature](https://github.com/pingcap/tikv/pull/2247) for DAG.
* Add the [short name for raftdb](https://github.com/pingcap/tikv/pull/2249) in tikv-ctl.
* Implement the [bit operation](https://github.com/pingcap/tikv/pull/2252) for expression.
* Implement the [`int_as_true` and `decimal/real_as_false`](https://github.com/pingcap/tikv/pull/2255) for expression.
* Add [the `IfJson`, `IfNullJson` signature and some flags](https://github.com/pingcap/tikv/pull/2264) for DAG.

## Fixed

* Fixed [capacity parsing](https://github.com/pingcap/tikv/pull/2251).
* Fixed an [unwrapping panic](https://github.com/pingcap/tikv/pull/2253) in scheduler.
* Drop the [delete-range feature](https://github.com/pingcap/tikv/pull/2258) temporarily.

## Improved

* Add more tests for [config structs](https://github.com/pingcap/tikv/pull/2230).
* Refactor [1](https://github.com/pingcap/pd/pull/719), [2](https://github.com/pingcap/pd/pull/720), [3](https://github.com/pingcap/pd/pull/722), [4](https://github.com/pingcap/pd/pull/724), [5](https://github.com/pingcap/pd/pull/725), [6](https://github.com/pingcap/pd/pull/727), [7](https://github.com/pingcap/pd/pull/728), [8](https://github.com/pingcap/pd/pull/729), [9](https://github.com/pingcap/pd/pull/730), [10](https://github.com/pingcap/pd/pull/731), [11](https://github.com/pingcap/pd/pull/733), [12](https://github.com/pingcap/pd/pull/737), [13](https://github.com/pingcap/pd/pull/740) on PD.
* Cleanup the [threadpool](https://github.com/pingcap/tikv/pull/2250).
* Add the [panic detail information](https://github.com/pingcap/tikv/pull/2259).
* Optimize [merging array elements](https://github.com/pingcap/pd/pull/735).
* Use [`time.Since`](https://github.com/pingcap/pd/pull/736) instead of `time.Now().Sub`.
* Check if the [log is initialized](https://github.com/pingcap/tikv/pull/2263) when starting up.

## New contributors
* https://github.com/wgliang