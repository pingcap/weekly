---
layout: post
title: Weekly Update
---
## Weekly update in TiDB
2017-06-18
Last week, we landed [30 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-06-12..2017-06-18%20) in the TiDB repositories.

## Added
* Refactor the optimizer:
  - [Refactor ranger/statistic](https://github.com/pingcap/tidb/pull/3370): calculate the range and row count of non pk column.
* JSON type:
  - Support generated column:](https://github.com/pingcap/tidb/pull/3431)
  - [Support the JSON type in the `cast` expression.](https://github.com/pingcap/tidb/pull/3395)
* Generated column:
  - [Support basic generated column.](https://github.com/pingcap/tidb/pull/3431)
  - [Prevent modifying generated column.](https://github.com/pingcap/tidb/pull/3434)
  - [Add GeneratedExpr in ColumnInfo.](https://github.com/pingcap/tidb/pull/3487)
* [Support `using` clause in join statement.](https://github.com/pingcap/tidb/pull/3372)
* [Use GetTSAsync api from pd-client.](https://github.com/pingcap/tidb/pull/3459)
* [Support SubTime.](https://github.com/pingcap/tidb/pull/3464)

## Fixed
* [Fix a bug in alter table statement.](https://github.com/pingcap/tidb/pull/3456)
* [Fix a bug in `cast`.](https://github.com/pingcap/tidb/pull/3462)
* [Fix a bug about parsing Duration literal.](https://github.com/pingcap/tidb/pull/3468)
* [Fix a divide zero bug in statistic.](https://github.com/pingcap/tidb/pull/3481)
* [Fix a protobuf unmarshal related bug in coprocessor.](https://github.com/pingcap/tidb/pull/3482)
* [Fix a bug about auto_increment column conflict after renaming table.](https://github.com/pingcap/tidb/pull/3493)

## Improved
* [Add some columns in `mysql.user`:](https://github.com/pingcap/tidb/pull/3445) compatiable with MySQL.
* [Use multiple grpc connnections for each store:](https://github.com/pingcap/tidb/pull/3453) improve performance.
* Refactor expression evaluation:
  - [Consider unsigned flag in cast expression.](https://github.com/pingcap/tidb/pull/3457)
* Speed up DDL process: 
  - [Revoke the etcd-session when ddl worker is closed.](https://github.com/pingcap/tidb/pull/3461)

## Weekly update in TiKV  

Last week, We landed [14 PRs](https://github.com/search?p=1&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-06-11..2017-06-17&type=Issues&utf8=%E2%9C%93) in the TiKV repositories.

## Added

* Coprocessor supports [index scan](https://github.com/pingcap/tikv/pull/1817) executor.
* Add MySQL [JSON](https://github.com/pingcap/tikv/pull/1874) type.
* Support [comparison](https://github.com/pingcap/tikv/pull/1893) for mySQL JSON type.
*

## Fixed

* Fix a [bug caused by GC](https://github.com/pingcap/tikv/pull/1916) with stale command.

## Improved

* Increase initialized [window size](https://github.com/pingcap/tikv/pull/1909) to 2MB for gRPC stream. 
* Using `prefix_same_as_start` to optimize [seek](https://github.com/pingcap/tikv/pull/1917) for Write CF.
* Use [multiple connections](https://github.com/pingcap/tikv/pull/1921) to speed up Raft message sending.
* Update Dockerfile, see [1915](https://github.com/pingcap/tikv/pull/1915) and [1919](https://github.com/pingcap/tikv/pull/1919).

## New contributor

* [AkihiroSuda](https://github.com/AkihiroSuda)