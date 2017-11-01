---
title: Weekly update (August 28 ~ September 3, 2017)
date: 2017-09-04
summary: Last week, we landed 42 PRs in the TiDB repositories and 32 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV']
---

# Weekly update in TiDB

Last week, we landed [42 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-08-28..2017-09-03) in the TiDB repositories.

## Added
* [Add JSON into builtin `if` function.](https://github.com/pingcap/tidb/pull/4203)

## Fixed
* [Fix bugs when doing natural JOIN or JOIN with using clause.](https://github.com/pingcap/tidb/pull/4389)
* [Check whether date is zero and returns error when casting int as the time type.](https://github.com/pingcap/tidb/pull/4387)
* [Support date time format when parse duration.](https://github.com/pingcap/tidb/pull/4380)
* [Fix the issue that `SHOW CREATE TABLE COMMENT` is not escaped and the issue that `FieldType.CompactStr()` is escaped.](https://github.com/pingcap/tidb/pull/4372)
* [Support empty bit-value literal syntax `b''`.](https://github.com/pingcap/tidb/pull/4370)
* [Fix the `OCT()` bug when it meets a binary value.](https://github.com/pingcap/tidb/pull/4369)
* [Fix float and binary literal bugs.](https://github.com/pingcap/tidb/pull/4365)
* [Fix index join key incompatible encoded problem.](https://github.com/pingcap/tidb/pull/4363/files)
* [`EvalDuration` supports the time format in int.](https://github.com/pingcap/tidb/pull/4349)
* [Fix the batch insert bug on duplicate keys.](https://github.com/pingcap/tidb/pull/4344)
* [Fix the bug for parsing the `UTC_TIME/UTC_TIMESTAMP/CUR_TIME/CURRENT_TIME/CURRENT_TIMESTAMP` builtin](https://github.com/pingcap/tidb/pull/4306)

## Improved
* [Make `NOW()` folded in constant folding stage.](https://github.com/pingcap/tidb/pull/4385)
* [Refine the time stamp index selection.](https://github.com/pingcap/tidb/pull/4383)
* [Disable auto analyze.](https://github.com/pingcap/tidb/pull/4366)
* [Support sig pushdown in mocktikv.](https://github.com/pingcap/tidb/pull/4364)
* [Support more types when getting default FLEN and DECIMAL.](https://github.com/pingcap/tidb/pull/4236)
* Refactor the following expressions/builtin-function evaluation framework:
  - [GET_LOCK, RELEASE_LOCK](https://github.com/pingcap/tidb/pull/4398)
  - [FOUND_ROWS, DATABASE, CURRENT_USER, USER, CONNECTION_ID, VERSION](https://github.com/pingcap/tidb/pull/4395)
  - [STR_TO_DATE](https://github.com/pingcap/tidb/pull/4357/files)
  - [BIT_COUNT](https://github.com/pingcap/tidb/pull/4332)
  - [RLIKE](https://github.com/pingcap/tidb/pull/4331)
  - [MAKE_SET, QUOTE](https://github.com/pingcap/tidb/pull/4318)
  - [DATE_FORMAT](https://github.com/pingcap/tidb/pull/4312)
  - [PERIOD_ADD, PERIOD_DIFF](https://github.com/pingcap/tidb/pull/4309)
  - [UNIX_TIMESTAMP](https://github.com/pingcap/tidb/pull/4297)

# Weekly update in TiKV

Last week, We landed [32 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-08-27..2017-09-02&type=Issues) in the TiKV repositories.

## Added

* Use [`delete range`](https://github.com/pingcap/tikv/pull/1988) to destroy a replica.
* Add [`builtin_cast-III`](https://github.com/pingcap/tikv/pull/2176) for DAG/expression.
* Support [decoding Time](https://github.com/pingcap/tikv/pull/2199) from `tipb.Expr`.
* Add [statistics](https://github.com/pingcap/tikv/pull/2200) for coprocessor.
* Support [builtin `UnaryMinus*`](https://github.com/pingcap/tikv/pull/2202) for DAG.
* Add more [math functions](https://github.com/pingcap/tikv/pull/2213) for DAG.
* Implement [`eval`](https://github.com/pingcap/tikv/pull/2224) for expression.
* Support [storing weight](https://github.com/pingcap/pd/pull/713) when balancing data.
* Adjust [the decimal parsing interface](https://github.com/pingcap/tikv/pull/2232) for coprocessor
* Implement [`coalesce`] (https://github.com/pingcap/tikv/pull/2239) for corprocessor.
* Implement [`case_when`](https://github.com/pingcap/tikv/pull/2241) for DAG.

## Improved

* Refactor [`storeInfo`](https://github.com/pingcap/pd/pull/712).
* Speed up [reconnecting to PD leader](https://github.com/pingcap/tikv/pull/2207).
* Use [`FnvHashMap`](https://github.com/pingcap/tikv/pull/2211).
* [Cleanup code](https://github.com/pingcap/tikv/pull/2215) for coprocessor.
* Add [more tests](https://github.com/pingcap/tikv/pull/2218) for `exprssion/builtin_cast`.
* Use [RocksDB 5.7.3](https://github.com/pingcap/tikv/pull/2229).
* Add more [write statistics](https://github.com/pingcap/tikv/pull/2233).
* Make [error message more friendly](https://github.com/pingcap/tikv/pull/2235).
* Refactor [replica selector](https://github.com/pingcap/pd/pull/717) for PD.
