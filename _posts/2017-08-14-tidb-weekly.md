---
layout: post
title: Weekly Update
---
## Weekly update in TiDB

2017-08-14

Last week, we landed [78 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-08-07..2017-08-13%20) in the TiDB repositories.

## Added
* Enable pushing down the following operations to TiKV.
	- [the JSON function](https://github.com/pingcap/tidb/pull/3793)
	- [ifnull](https://github.com/pingcap/tidb/pull/4126)
	- [minus and multiply](https://github.com/pingcap/tidb/pull/4151)
* [Use the `Delete-in-Range` feature to speed up the `Drop Database/Table/Index` operations.](https://github.com/pingcap/tidb/pull/3993)
* [Support prioritizing statements.](https://github.com/pingcap/tidb/pull/4119)

## Fixed
* [Fix the `TimeDiff` compatibility issue.](https://github.com/pingcap/tidb/pull/4018)
* [Consider charset in `Right/Left/Substr`.](https://github.com/pingcap/tidb/pull/4033)
* [Do not record metrics when running intenal SQL.](https://github.com/pingcap/tidb/pull/4064)
* [Fix potential issue of schema validation check.](https://github.com/pingcap/tidb/pull/4073)
* [Add desc order info in `explain`.](https://github.com/pingcap/tidb/pull/4108)

## Improved
* [Refactor the row structure](https://github.com/pingcap/tidb/pull/3758) to reduce memory allocation.
* Refactor the following expressions/builtin-functions evaluation framework:
  - [Plus](https://github.com/pingcap/tidb/pull/3858)
  - [Multiply](https://github.com/pingcap/tidb/pull/4118)
  - [Minus](https://github.com/pingcap/tidb/pullt/4077)
  - [lpad/rpad](https://github.com/pingcap/tidb/pull/4036)
  - [bin](https://github.com/pingcap/tidb/pull/4039)
  - [from_base64](https://github.com/pingcap/tidb/pull/4040)
  - [char](https://github.com/pingcap/tidb/pull/4041)
  - [reverse](https://github.com/pingcap/tidb/pull/4042)
  - [ifnull](https://github.com/pingcap/tidb/pull/4050)
  - [instr](https://github.com/pingcap/tidb/pull/4052)
  - [aes_encrypt/aes_decrypt](https://github.com/pingcap/tidb/pull/4085)
  - [is_true/is_false](https://github.com/pingcap/tidb/pull/4086)
  - [locate](https://github.com/pingcap/tidb/pull/4088)
  - [last_insert_id](https://github.com/pingcap/tidb/pull/4093)
  - [compress/uncompress/uncompress_length](https://github.com/pingcap/tidb/pull/4095)
  - [sleep](https://github.com/pingcap/tidb/pull/4096)
  - [conv](https://github.com/pingcap/tidb/pull/4100)
  - [char_length](https://github.com/pingcap/tidb/pull/4105)
  - [md5/sha1/sha2](https://github.com/pingcap/tidb/pull/4109)
  - [charactor_length](https://github.com/pingcap/tidb/pull/4113)
  - [elt](https://github.com/pingcap/tidb/pull/4124)
  - [ifnull](https://github.com/pingcap/tidb/pull/4127)
  - [if](https://github.com/pingcap/tidb/pull/4137)
  - [round/abs](https://github.com/pingcap/tidb/pull/4146)
  - [random_bytes](https://github.com/pingcap/tidb/pull/4148)
  - [unaryplus](https://github.com/pingcap/tidb/pull/4152)
* [Adjust cost for the `Sort` operator.](https://github.com/pingcap/tidb/pull/4070)
* [Change the row format from structure to `Datum` slice.](https://github.com/pingcap/tidb/pull/4072)

## Weekly update in TiKV

Last week, We landed [28 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-08-06..2017-08-12&type=Issues) in the TiKV repositories.

## Added

* Add [hex/escaped converting](https://github.com/pingcap/tikv/pull/2143) for tikv-ctl.
* Add [custom instant](https://github.com/pingcap/tikv/pull/2139) for time utilities.
* Add [rows properties](https://github.com/pingcap/tikv/pull/2136).
* Add [size properties](https://github.com/pingcap/tikv/pull/2097).
* Add [region approximate size](https://github.com/pingcap/tikv/pull/2132).
* Support basic [DAG expression evaluation](https://github.com/pingcap/tikv/pull/2133) for coprocessor.
* Support the [delete range KV](https://github.com/pingcap/tikv/pull/1983) command.
* Add the [diff](https://github.com/pingcap/tikv/pull/2126) command for tikv-ctl to check the difference between 2 databases.

## Fixed

* Fix a bug caused by [using box_try](https://github.com/pingcap/tikv/pull/2131) for the coprocessor.

## Improved

* Speed up [clearing meta](https://github.com/pingcap/tikv/pull/2095).
* Reduce callback by [batching RaftCmdRequest](https://github.com/pingcap/tikv/pull/2107).
* Refactor the [configuration](https://github.com/pingcap/tikv/pull/2116).
* Refactor the [DAG and old selection](https://github.com/pingcap/tikv/pull/2128).
* Refactor the [time utilities](https://github.com/pingcap/tikv/pull/2137).