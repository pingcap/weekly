---
date: 2017-07-17T00:00:00Z
title: Weekly Update
url: /2017/07/17/tidb-weekly/
---

## Weekly update in TiDB
2017-07-17

Last week, we landed [51 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-07-10..2017-07-16%20) in the TiDB repositories.

## Added
* [Support setting variables with `ON` and `OFF`.](https://github.com/pingcap/tidb/pull/3631)
* Support [`show stats_histgrams`](https://github.com/pingcap/tidb/pull/3683) and [`show stats_buckets`](https://github.com/pingcap/tidb/pull/3720) for debugging.
* [Support the `Scan` API for the raw KV interface.](https://github.com/pingcap/tidb/pull/3707)
* [Support the `Show Charset` statement.](https://github.com/pingcap/tidb/pull/3726)
* [Support user name without quotes such as `root@127.0.0.1`.](https://github.com/pingcap/tidb/pull/3742)

## Fixed
* [Fix a bug when explicitly inserting the `null` value into columns with the timestamp type.](https://github.com/pingcap/tidb/pull/3646)
* [Do not check privileges for the `information_schema` database.](https://github.com/pingcap/tidb/pull/3675)
* [Correct the error message for the authentication error.](https://github.com/pingcap/tidb/pull/3696)
* [Fix a bug in the `cast` function with an unsigned type.](https://github.com/pingcap/tidb/pull/3705)

## Improved
* Refactor optimizer:
  - Select Join operator by CBO framework automatically: [#3623](https://github.com/pingcap/tidb/pull/3623), [#3737](https://github.com/pingcap/tidb/pull/3737), [#3761](https://github.com/pingcap/tidb/pull/3761)
  - [Use statsProfile to estimate count and cardinality.](https://github.com/pingcap/tidb/pull/3728)
* Refactor the builtin function evaluation framework:
  - [left & right](https://github.com/pingcap/tidb/pull/3540)
  - [lower & upper](https://github.com/pingcap/tidb/pull/3550)
  - [concat_ws](https://github.com/pingcap/tidb/pull/3558)
  - [to_base64](https://github.com/pingcap/tidb/pull/3598)
  - [md5](https://github.com/pingcap/tidb/pull/3673)
  - [space](https://github.com/pingcap/tidb/pull/3684)
  - [replace](https://github.com/pingcap/tidb/pull/3702)
  - [substring/substr](https://github.com/pingcap/tidb/pull/3711)
  - [compare](https://github.com/pingcap/tidb/pull/3714)
  - [uuid](https://github.com/pingcap/tidb/pull/3721)
  - [bit_length](https://github.com/pingcap/tidb/pull/3722)
  - [log10](https://github.com/pingcap/tidb/pull/3733)
  - Move the type inference work from typeinfer to expression rewritter: [aggregate expression](https://github.com/pingcap/tidb/pull/3654), [column & constant expression](https://github.com/pingcap/tidb/pull/3667)
* [Close the connection after sending `ERR_Packet`.](https://github.com/pingcap/tidb/pull/3678)
* [Improve the unit test coverage for parser packages.](https://github.com/pingcap/tidb/pull/3718)

## Weekly update in TiKV

Last week, We landed [23 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-07-09..2017-07-15&type=Issues) in the TiKV repositories.

## Added

* Add [`json_modify`](https://github.com/pingcap/tikv/pull/1998), [math function](https://github.com/pingcap/tikv/pull/2024) evaluators for the coprocessor.
* Pass the [compression type](https://github.com/pingcap/tikv/pull/2001) to generate snapshot SST.
* Set [256 MB](https://github.com/pingcap/tikv/pull/2017) as the default region size.
* Add the raw [Scan](https://github.com/pingcap/tikv/pull/2020) API.

## Fixed

* [Ignore the command](https://github.com/pingcap/tikv/pull/2016) that removes the leader itself.
* Fix [diff hint](https://github.com/pingcap/tikv/pull/2019) overflow.
* [Rotate PD log](https://github.com/pingcap/pd/pull/678) by default.
* Fix the [leap second](https://github.com/pingcap/pd/pull/681) problem in Go 1.9.
* Clean up [stale metadata](https://github.com/pingcap/tikv/pull/2041) when start.

## Improved

* [Reduce the lock scope](https://github.com/pingcap/pd/pull/677) for region heartbeat.
* Send the [raft messages in batch](https://github.com/pingcap/tikv/pull/2022).
* Refactor the [coprocessor](https://github.com/pingcap/tikv/pull/2029) code directory.
* Enable the [pipelined write](https://github.com/pingcap/tikv/pull/2031).
* Remove [unnecessary hash](https://github.com/pingcap/tikv/pull/2042) group keys.