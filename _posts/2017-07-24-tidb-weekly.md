---
layout: post
title: Weekly Update
---
## Weekly update in TiDB
2017-07-24

Last week, we landed [60 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-07-17..2017-07-23%20) in the TiDB repositories.

## Added
* [Add a `tidb_version` function to get the `tidb-server` version information.](https://github.com/pingcap/tidb/pull/3592)
* [Support the `READ COMMITTED` isolation level.](https://github.com/pingcap/tidb/pull/3619)
* [Support the `ENCLOSED BY` clause in the `Load Data` statement.](https://github.com/pingcap/tidb/pull/3759)
* [Support creating index using type and comment.](https://github.com/pingcap/tidb/pull/3814)

## Fixed
* [Fix a bug when in `json_unquote`.](https://github.com/pingcap/tidb/pull/3764)
* [Fix field name with comment.](https://github.com/pingcap/tidb/pull/3767)
- [Fix the wrong offset when using the Primary Key column as the handle.](https://github.com/pingcap/tidb/pull/3820)

## Improved
* Refactor the optimizer:
  - [Refactoring projection elimination.](https://github.com/pingcap/tidb/pull/3687)
* Refactor the builtin function evaluation framework:
  - [substring_index](https://github.com/pingcap/tidb/pull/3760)
  - [log](https://github.com/pingcap/tidb/pull/3763)
  - [asin](https://github.com/pingcap/tidb/pull/3765)
  - [atan](https://github.com/pingcap/tidb/pull/3788)
  - [acos](https://github.com/pingcap/tidb/pull/3789)
  - [floor](https://github.com/pingcap/tidb/pull/3791)
  - [hex](https://github.com/pingcap/tidb/pull/3794)
  - [ceil](https://github.com/pingcap/tidb/pull/3819)
  - [unhex](https://github.com/pingcap/tidb/pull/3830)
* Improve the unit test coverage:
  - [`table` package](https://github.com/pingcap/tidb/pull/3770)
  - [`schema.go`](https://github.com/pingcap/tidb/pull/3779)
  - [`kv` package](https://github.com/pingcap/tidb/pull/3790)
  - [`builtin_compare.go`](https://github.com/pingcap/tidb/pull/3792)
  - [`datum.go`](https://github.com/pingcap/tidb/pull/3795)
  - [`distsql` package](https://github.com/pingcap/tidb/pull/3806)
  - [`column.go`](https://github.com/pingcap/tidb/pull/3822)
  - [`expression.go`](https://github.com/pingcap/tidb/pull/3828)
  - [`scalar_function.go`](https://github.com/pingcap/tidb/pull/3840)
* [Fix a bug of using undefined user variable.](https://github.com/pingcap/tidb/pull/3776)

## Weekly update in TiKV

Last week, We landed [19 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-07-16..2017-07-22&type=Issues) in the TiKV repositories.

## Added

* Add [DAG](https://github.com/pingcap/tikv/pull/1975) executor for coprocessor.
* Add [`json_object` and `json_array`](https://github.com/pingcap/tikv/pull/2025) for coprocessor.
* Add the [`abs`](https://github.com/pingcap/tikv/pull/2033) function for the coprocessor.
* Add the [`u64`](https://github.com/pingcap/tikv/pull/2044) support for JSON type.
* Add the [`max_compaction_bytes`](https://github.com/pingcap/tikv/pull/2047) support for RocksDB.
* Add the [TSO](https://github.com/pingcap/pd/pull/683) warning metrics for PD.

## Fixed

* Enlarge gRPC [send message length](https://github.com/pingcap/tikv/pull/2040).
* [Remove the unix socket](https://github.com/pingcap/pd/pull/684) from PD test.
* Fix [a bug](https://github.com/pingcap/tikv/pull/2065) when shrinking buffer.

## Improved

* Use [collected properties](https://github.com/pingcap/tikv/pull/1971) to optimize GC. 
* Get RocksDB snapshot [lazily](https://github.com/pingcap/tikv/pull/2045).
* [Introduce rate limit](https://github.com/pingcap/tikv/pull/2050) to make QPS more stable.
* Send [the apply proposals](https://github.com/pingcap/tikv/pull/2051) in batches.
* Stop supporting [the old V1](https://github.com/pingcap/tikv/pull/2053) snapshot format any more and support using [V2](https://github.com/pingcap/tikv/pull/2057) only.