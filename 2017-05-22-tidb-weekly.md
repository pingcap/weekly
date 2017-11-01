---
title: Weekly update (May 15 ~ May 21, 2017)
date: 2017-05-22
summary: Last week, we landed 31 PRs in the TiDB repositories and 16 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV']
---

# Weekly update in TiDB

Last week, we landed [31 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-05-15..2017-05-21%20) in the TiDB repositories.

## Added

* [Use `etcd` to elect DDL job leader.](https://github.com/pingcap/tidb/pull/3158) 

* [Support `Load Data` with specified column list.](https://github.com/pingcap/tidb/pull/3240)

* Add the following builtin functions:
	- [`umcompress` and `uncompressdlength`](https://github.com/pingcap/tidb/pull/3136)
	- [`convert_tz`](https://github.com/pingcap/tidb/pull/3222)
	- [`period-diff`](https://github.com/pingcap/tidb/pull/3237)

* [Support the `Json` type and `Json` data encoding/decoding.](https://github.com/pingcap/tidb/pull/3248)

* [Add a `Jenkins CI` in Pull Request.](https://github.com/pingcap/tidb/pull/3249)

* [Add the `EvalDuration` and `EvalTime` interface for expressions.](https://github.com/pingcap/tidb/pull/3278)

* [Support `Index Lookup Join` in new planner.](https://github.com/pingcap/tidb/pull/3281)


## Fixed

* [Add default value for the Password Validation system variables.](https://github.com/pingcap/tidb/pull/3251)

* [Fix the issue of retrying with no limitation when committing primary key failed.](https://github.com/pingcap/tidb/pull/3258)

* [Fix the issue of context cancellation triggering onSendFail and dropping cache:](https://github.com/pingcap/tidb/pull/3259) context cancel doesn't mean cache out of data.

* [Fix a bug in `Sort Merge Join`.](https://github.com/pingcap/tidb/pull/3262)

* [Correct comment mistakes.](https://github.com/pingcap/tidb/pull/3272)

* [Reprocess SQL statement when meeting the infoschema change error.](https://github.com/pingcap/tidb/pull/3270)

* [Update an error code to MySQL standard error code.](https://github.com/pingcap/tidb/pull/3276)

* [Consider schema changing when retrying prepared statement.](https://github.com/pingcap/tidb/pull/3297)

## Improved

* [Refator range calculation related code.](https://github.com/pingcap/tidb/pull/3208)

* [Consider task type when building the physical plan:](https://github.com/pingcap/tidb/pull/3257) to make cost more precise.

* [Support more SQL grammar for `Lock Options`.](https://github.com/pingcap/tidb/pull/3260)

* [Rename `SupportRequestType` to `IsRequestTypeSupported` to improve readability.](https://github.com/pingcap/tidb/pull/3263)

* [Support more SQL grammar for `Compress Options` in the `AlterTable` statement.](https://github.com/pingcap/tidb/pull/3293)

* [Change the schema of statistic table.](https://github.com/pingcap/tidb/pull/3295)

# Weekly update in TiKV

Last week, We landed [16 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-05-14..2017-05-20&type=Issues) in the TiKV repositories.

## Added

* Support [table scan](https://github.com/pingcap/tikv/pull/1786) with DAG in coprocessor.
* Add Jenkins support, see [643](https://github.com/pingcap/pd/pull/643), [644](https://github.com/pingcap/pd/pull/644), [1835](https://github.com/pingcap/tikv/pull/1835), [1836](https://github.com/pingcap/tikv/pull/1836).
* Write [Raft log synchronously](https://github.com/pingcap/tikv/pull/1840) to ensure data safety.

## Fixed

* Use [IEC](https://github.com/pingcap/pd/pull/646) size for size output. 
* Enlarge max [duration](https://github.com/pingcap/tikv/pull/1854) for scheduler histogram metrics.

## Improved

* Use [`SmallGroupFirstQueue`](https://github.com/pingcap/tikv/pull/1818) in endpoint scheduler.
* Fetch snapshot [lazily](https://github.com/pingcap/tikv/pull/1845) to reduce the cost of creating unnecessary snapshot.
* Create WriteBatch [with capacity](https://github.com/pingcap/tikv/pull/1846) to avoid reallocating.
