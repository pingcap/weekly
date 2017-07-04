---
layout: post
title: Weekly Update
---
## Weekly update in TiDB
2017-07-03

Last week, we landed [33 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-06-26..2017-07-02%20) in the TiDB repositories.

## Added
* [Support priority options in the `select` statement.](https://github.com/pingcap/tidb/pull/3466)
* [Add the `GetOwnerID` interface in `OwnerManager`.](https://github.com/pingcap/tidb/pull/3525)
* [Add some columns in `mysql.db`:](https://github.com/pingcap/tidb/pull/3532) Make it compatible with MySQL.
* [Add the `IsolationLevel` option in the coprocessor request to TiKV.](https://github.com/pingcap/tidb/pull/3535)
* [Add the `priority` option in Key-Value request to TiKV.](https://github.com/pingcap/tidb/pull/3547)
* [Support the `RenameTable` statement without the `To` keyword.](https://github.com/pingcap/tidb/pull/3552)

## Fixed
* [Fix a bug in the `update` statement like `update T set a = 8, b = a`.](https://github.com/pingcap/tidb/pull/3531) 
* [Consider the timezone information when using `current_timestamp` as the default value.](https://github.com/pingcap/tidb/pull/3544)
* [Break the campaigning owner loop when closing a DDL worker.](https://github.com/pingcap/tidb/pull/3553)
* [Check the validity of table name in the `CreateTable` statement.](https://github.com/pingcap/tidb/pull/3554)
* [Handle the null argument in `substr` function.](https://github.com/pingcap/tidb/pull/3555)
* [Disable concurrent pre-write when meeting the `SkipConstrainCheck` option.](https://github.com/pingcap/tidb/pull/3561)
* Handle binary data in the [HEX](https://github.com/pingcap/tidb/pull/3567) function and the [unhex](https://github.com/pingcap/tidb/pull/3569) function.
* [Return `ErrNoDB` (No database selected) when no database is used and the table name is without database qualifier.](https://github.com/pingcap/tidb/pull/3572)

## Improved
* Refactor optimiser:
  - [Prune ordered column paths.](https://github.com/pingcap/tidb/pull/3473)
  - [Prepare for using the new CBO framework.](https://github.com/pingcap/tidb/pull/3577)
* [Flatten the `row` operations.](https://github.com/pingcap/tidb/pull/3528)
* [Log critical statements.](https://github.com/pingcap/tidb/pull/3557)
* [Code clean up.](https://github.com/pingcap/tidb/pull/3564)


## New contributor

[sempr](https://github.com/sempr)
[JackDrogon](https://github.com/JackDrogon)
[Zhang Jian](https://github.com/zz-jason)

## Weekly update in TiKV

Last week, We landed [12 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-06-25..2017-07-01&type=Issues) in the TiKV repositories.

## Added

* Use the [bi-directional stream](https://github.com/pingcap/tikv/pull/1888) for PD region heartbeat.
* Add the [selection executor](https://github.com/pingcap/tikv/pull/1914) for coprocessor.
* Support the [read committed](https://github.com/pingcap/tikv/pull/1958) isolation level for transactions.
* Add the [modify](https://github.com/pingcap/tikv/pull/1964) function for JSON document.

## Fixed

* Use [Equal](https://github.com/pingcap/pd/pull/666) to check parsed timestamp.
* Fix the [heartbeat](https://github.com/pingcap/pd/pull/663) tests.

## Improved

* [Generate snapshot](https://github.com/pingcap/tikv/pull/1963) concurrently.
* [Skip handling read only](https://github.com/pingcap/tikv/pull/1966) commands in the Raft apply worker.
* Upgrade Rust Protobuf to the [1.4](https://github.com/pingcap/tikv/pull/1969) version.