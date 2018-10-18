---
title: Weekly update (June 19 ~ June 25, 2017)
date: 2017-06-26
summary: Last week, we landed 35 PRs in the TiDB repositories and 24 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV']
---

# Weekly update in TiDB

Last week, we landed [35 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-06-19..2017-06-25%20) in the TiDB repositories.

## Added
* JSON type:
  - [Tiny cleanup.](https://github.com/pingcap/tidb/pull/3486)
  - [Fix a bug in JSON path_expr.](https://github.com/pingcap/tidb/pull/3504)
  - [Fix a bug in `unquote`.](https://github.com/pingcap/tidb/pull/3507)
  - [Make `json_unquote` compatiable with MySQL](https://github.com/pingcap/tidb/pull/3521)
  - [Code cleanup.](https://github.com/pingcap/tidb/pull/3524)

## Fixed
* [Fix failed test cases on the ppc64le platform](https://github.com/pingcap/tidb/pull/3477)
* [Fix a bug when naming table with the `auto_increment` column.](https://github.com/pingcap/tidb/pull/3494)
* [Use UTC time to compose index key for timestamp column.](https://github.com/pingcap/tidb/pull/3497)
* [Consider fsp for MySQLDuration type in some scenarios.](https://github.com/pingcap/tidb/pull/3499)
* [Reset transaction when error occurs during retrying.](https://github.com/pingcap/tidb/pull/3503)
* [Fix a bug about adding index after adding column with default value.](https://github.com/pingcap/tidb/pull/3510)
* [Suport time format 'YY-MM-DD HH:MM'.](https://github.com/pingcap/tidb/pull/3511)
* [Fix the issue of parsing datetime `00-00-00`.](https://github.com/pingcap/tidb/pull/3536)

## Improved
* Refactor the expression evaluation:
  - [Rewrite concat with new expression framework.](https://github.com/pingcap/tidb/pull/3479)
  - [Remove the `inferType` inerface of functionClass.](https://github.com/pingcap/tidb/pull/3518)
  - [Rewrite the `length` built-in function with the new expression framework.](https://github.com/pingcap/tidb/pull/3519)
  - [Wrap arguments when building new built-in functions.](https://github.com/pingcap/tidb/pull/3520)
  - [Rewrite the `makedate` built-in function with the new expression framework.](https://github.com/pingcap/tidb/pull/3533)
* [Change the result format of the aggregation operator.](https://github.com/pingcap/tidb/pull/3483)
* Refactor range related code: [#3489](https://github.com/pingcap/tidb/pull/3489), [#3496](https://github.com/pingcap/tidb/pull/3496) 
* Code style cleanup:[#3502](https://github.com/pingcap/tidb/pull/3502), [#3505](https://github.com/pingcap/tidb/pull/3505)
* [Handle out-of-range data in the `load local file` command.](https://github.com/pingcap/tidb/pull/3508)
* [Remove the `TiDBSkipDDLWait` variable.](https://github.com/pingcap/tidb/pull/3527)

## New contributor

[dreamquster](https://github.com/dreamquster)


# Weekly update in TiKV

Last week, We landed [24 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-06-18..2017-06-24&type=Issues) in the TiKV repositories.

## Added

* Use [individual thread](https://github.com/pingcap/tikv/pull/1930) to handle high priority command.
* Support [JSON](https://github.com/pingcap/tikv/pull/1932) type.
* Support the [`json_type`](https://github.com/pingcap/tikv/pull/1937), [`unquote`](https://github.com/pingcap/tikv/pull/1948), [`extract`](https://github.com/pingcap/tikv/pull/1949), [`json_merge`](https://github.com/pingcap/tikv/pull/1951) functions for JSON.
* Add the [`TOPN`](https://github.com/pingcap/tikv/pull/1939), [`limit`](https://github.com/pingcap/tikv/pull/1952) executors for coprocessor.

## Fixed

* Handling [GC command](https://github.com/pingcap/tikv/pull/1934) in tombstone tests. 
* Print [readable message](https://github.com/pingcap/tikv/pull/1957) if the RocksDB configuration parsing fails.

## Improved

* Split different [JSON modules](https://github.com/pingcap/tikv/pull/1936) into independent files.
* Revise [leader lease](https://github.com/pingcap/tikv/pull/1945) time log.
* Remove sever thread and [directly send Raft messages](https://github.com/pingcap/tikv/pull/1882) to the gRPC thread.
* Remove unnecessary [`read_quorum`](https://github.com/pingcap/tikv/pull/1947) and [`uuid`](https://github.com/pingcap/tikv/pull/1953) fields.
