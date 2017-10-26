---
date: 2017-07-31T00:00:00Z
title: Weekly Update
---

## Weekly update in TiDB
2017-07-31

Last week, we landed [50 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-07-24..2017-07-30%20) in the TiDB repositories.

## Added
* [Add a debugging tool for transaction inspection.](https://github.com/pingcap/tidb/pull/3787)
* [Support two JSON syntactic sugars.](https://github.com/pingcap/tidb/pull/3854)
* [Support renaming multiple tables in a single statement.](https://github.com/pingcap/tidb/pull/3892)

## Fixed
* [Fix a bug in the `update` statement when doing the `alter table after` statement.](https://github.com/pingcap/tidb/pull/3754)
* [Fix signed integer overflow in the `minus unary scalar` function.](https://github.com/pingcap/tidb/pull/3780)
* [Fix the content in the information_schema for unsigned columns.](https://github.com/pingcap/tidb/pull/3818)
* [Fix inserting zero length data into a column with zero field length.](https://github.com/pingcap/tidb/pull/3849)
* [Check the field length limitation in the `alter table` statement.](https://github.com/pingcap/tidb/pull/3859)
* [Add the field length limitation for the index columns.](https://github.com/pingcap/tidb/pull/3864)
* [The `password` builtin function should return empty string when meeting null argument.](https://github.com/pingcap/tidb/pull/3880)
* [Check the table name with white space in the end.](https://github.com/pingcap/tidb/pull/3927)

## Improved
* [Add more DDL test cases.](https://github.com/pingcap/tidb/pull/3804)
* [Refactor the `explain` statement.](https://github.com/pingcap/tidb/pull/3809)
* Refactor the following expression/builtin-function evaluation framework:
  - [pi](https://github.com/pingcap/tidb/pull/3846)
  - [logicalAnd](https://github.com/pingcap/tidb/pull/3853)
  - [cot](https://github.com/pingcap/tidb/pull/3856)
  - [exp](https://github.com/pingcap/tidb/pull/3871)
  - [logicalXor](https://github.com/pingcap/tidb/pull/3899)
  - [bitAnd](https://github.com/pingcap/tidb/pull/3901)
  - [logicalOr](https://github.com/pingcap/tidb/pull/3903)
  - [bitOr](https://github.com/pingcap/tidb/pull/3904)
  - [bitXor](https://github.com/pingcap/tidb/pull/3905)
  - [leftShift](https://github.com/pingcap/tidb/pull/3906)
  - [rightShift](https://github.com/pingcap/tidb/pull/3907)
  - [bitNeg](https://github.com/pingcap/tidb/pull/3937)
* [Extract configuration related code to the `config` package.](https://github.com/pingcap/tidb/pull/3919)
* Improve the unit test coverage:
  - [`ast` package](https://github.com/pingcap/tidb/pull/3870)
* [Fix a bug of using undefined user variable.](https://github.com/pingcap/tidb/pull/3776)
* [Make `go vet` happy.](https://github.com/pingcap/tidb/pull/3872)

## New Contributor (Thanks!)
* [Jiaxing Liang](https://github.com/liangjiaxing)
* [Hu Ming](https://github.com/ming-relax)
* [Wei Fu](https://github.com/0x04C2)
* [Liao Qiang](https://github.com/CodeRushing)

## Weekly update in TiKV

Last week, We landed [27 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-07-23..2017-07-29&type=Issues) in the TiKV repositories.

## Added

* Add the [transaction debugging](https://github.com/pingcap/tikv/pull/2012) gRPC API.
* Add the [`ceil`](https://github.com/pingcap/tikv/pull/2060), [`abs`](https://github.com/pingcap/tikv/pull/2063) functions for coprocessor.
* Add [the compaction priority](https://github.com/pingcap/tikv/pull/2062) for RocksDB.
* Handle the[null datum](https://github.com/pingcap/tikv/pull/2072) for coprocessor.

## Fixed

* Decrease the [load limit](%20https://github.com/pingcap/pd/pull/688) to 10000. 
* Fix a bug when using [offset in expressions](https://github.com/pingcap/tikv/pull/2064) for coprocessor. 
* Fix [`trace_size`](https://github.com/pingcap/tikv/pull/2069) computing. 
* Let Travis decide which [compiler](https://github.com/pingcap/tikv/pull/2074) to use automatically.
* Fix a [message delay](https://github.com/pingcap/tikv/pull/2093) bug. 
* Avoid [unnecessary clones](https://github.com/pingcap/tikv/pull/2098) when sending Raft messages.

## Improved

* Log more [detailed error](https://github.com/pingcap/tikv/pull/2068) when transaction fails.
* Refactor RocksDB [options](https://github.com/pingcap/tikv/pull/2071).
* Implement [`serde`](https://github.com/pingcap/tikv/pull/2073) for enum and readable types. 
* Use the [FIFO](https://github.com/pingcap/tikv/pull/2076) queue for coprocessor work queue. 
* Decrease default `leader-schedule-limit` to [64](https://github.com/pingcap/pd/pull/690).
* Update [distinct score](https://github.com/pingcap/pd/pull/691) calculation for different stores. 
* Enhance the PD [`join`](https://github.com/pingcap/pd/pull/693) function.

## New contributors

* [ariesdevil](https://github.com/ariesdevil)
* [bailaohe](https://github.com/bailaohe)
* [dantin](https://github.com/dantin)