---
layout: post
title: Weekly Update
---
## Weekly update in TiDB

2017-08-28

Last week, we landed [55 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-08-21..2017-08-27%20) in the TiDB repositories.

## Added
* [Support the 'SHOW PLUGINS' syntax with dummy implementation.](https://github.com/pingcap/tidb/pull/4278)
* [Add a system variable to split to-be-deleted data into batches autmatically.](https://github.com/pingcap/tidb/pull/4256)
* [Add the `date` literal.](https://github.com/pingcap/tidb/pull/4046)
* [Add the framework of the X protocol, and commond line arguments.](https://github.com/pingcap/tidb/pull/3618)

## Fixed
* [Fix a panic when the `set` statement meets a subquery.](https://github.com/pingcap/tidb/pull/4326)
* [Set charset and collation for the union's result.](https://github.com/pingcap/tidb/pull/4322/files)
* [Fix `show column comment`, `show create table auto-increment`.](https://github.com/pingcap/tidb/pull/4303)
* [Fix the bug in Date comparison.](https://github.com/pingcap/tidb/pull/4294)
* [Fix the bug in index selection.](https://github.com/pingcap/tidb/pull/4286)
* [Rewrite the index join plan generation to correct wrong index selection.](https://github.com/pingcap/tidb/pull/4274)
* [Avoid 'binary BINARY' for a special field type.](https://github.com/pingcap/tidb/pull/4272)
* [Correct overflow check on the MINUS function.](https://github.com/pingcap/tidb/pull/4266/files)
* [Fix a bug when casting JSON to other types.](https://github.com/pingcap/tidb/pull/4265)
* [Concatenates string literals which placed each other.](https://github.com/pingcap/tidb/pull/4252)
* [Fix an issue that the flags of the 'IFNULL' Builtin function result is not consistent with MySQL.](https://github.com/pingcap/tidb/pull/4158)

## Improved
* [Enlarge the batch size from 128M to 256M to reduce the network round-trip.](https://github.com/pingcap/tidb/pull/4315)
* [Suport `coalesce` pushdown.](https://github.com/pingcap/tidb/pull/4288)
* [Make auto analyze more conservative.](https://github.com/pingcap/tidb/pull/4284)
* [Support `isnull` pushdown.](https://github.com/pingcap/tidb/pull/4260)
* [Implement the `MVCCStore` interface using the leveldb backend.](https://github.com/pingcap/tidb/pull/3970)
* [Calculate generated columns in CRUD.](https://github.com/pingcap/tidb/pull/3951)
* Refactor the following expression/builtin-function evaluation framework:
  - [TIMESTAMP](https://github.com/pingcap/tidb/pull/4327)
  - [DAYNAME](https://github.com/pingcap/tidb/pull/4317)
  - [DATE](https://github.com/pingcap/tidb/pull/4314)
  - [UTC_TIME](https://github.com/pingcap/tidb/pull/4304)
  - [MONTHNAME](https://github.com/pingcap/tidb/pull/4300)
  - [WEEKDAY, FROM_DAYS, QURTER](https://github.com/pingcap/tidb/pull/4298)
  - [LAST_DAY](https://github.com/pingcap/tidb/pull/4290)
  - [DAYOFWEEK, DAYOFMONTH, DAYOFYEAR](https://github.com/pingcap/tidb/pull/4283)
  - [FIND_IN_SET](https://github.com/pingcap/tidb/pull/4247)
  - [DATEDIFF](https://github.com/pingcap/tidb/pull/4212)
  - [CURDATE, SYSDATE, YEARWEEK](https://github.com/pingcap/tidb/pull/4211)
  - [YEAR, MONTH](https://github.com/pingcap/tidb/pull/4210)
  - [WEEK, WEEKOFYEAR](https://github.com/pingcap/tidb/pull/4208)
  - [NOW, UTC_TIMESTAMP, UTC_DATE](https://github.com/pingcap/tidb/pull/4206)
  - [TIMESTAMPDIFF](https://github.com/pingcap/tidb/pull/4184)
  - [COALESCE](https://github.com/pingcap/tidb/pull/4157)

## New Contributor (Thanks!)
* [David Ding](https://github.com/dantin)
* [xiaojian Cai](https://github.com/mccxj)
* [bailaohe](https://github.com/bailaohe)

## Weekly update in TiKV

Last week, We landed [21 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-08-20..2017-08-26&type=Issues) in the TiKV repositories.

## Added

* Use [dedicated Rocksdb instance](https://github.com/pingcap/tikv/pull/2054) to store Raft log.
* Add [builtin_cast-II](https://github.com/pingcap/tikv/pull/2172) for DAG/expression.
* Add [builtin scalar function operator](https://github.com/pingcap/tikv/pull/2188) for DAG.
* Add [arithmetic operations](https://github.com/pingcap/tikv/pull/2189) for DAG.
* Add [builtin conditions](https://github.com/pingcap/tikv/pull/2198) for DAG.
* Add more RocksDB [metrics](https://github.com/pingcap/tikv/pull/2201).
* Support [negative operator](https://github.com/pingcap/tikv/pull/2210) for decimal.

## Fixed

* Fix a [data race](https://github.com/pingcap/pd/pull/706) for PD.
* Fix a [heartbeat stream bug](https://github.com/pingcap/pd/pull/709) for PD.
* Fix a bug with [reverse scan](https://github.com/pingcap/tikv/pull/2204).

## Improved

* Refactor the [Coprocessor thread pool](https://github.com/pingcap/tikv/pull/2152) to pass contexts.
* Improve [tests](https://github.com/pingcap/pd/pull/707).
* Add [`timeout`](https://github.com/pingcap/pd/pull/710) for RPC calls.
* Remove [`timeout`](https://github.com/pingcap/pd/pull/711) for streaming calls.
* Make [max tasks](https://github.com/pingcap/tikv/pull/2203) configurable for the Coprocessor.
* Move the [heartbeat approximate size](https://github.com/pingcap/tikv/pull/2205) to PD worker.