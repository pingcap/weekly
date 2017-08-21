---
layout: post
title: Weekly Update
---
## Weekly update in TiDB

2017-08-21

Last week, we landed [57 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-08-14..2017-08-20%20) in the TiDB repositories.

## Added

* [Add the version information in diagnostic messages.](https://github.com/pingcap/tidb/pull/4218)
* [Add the `Close()` method to `RawKVClient`.](https://github.com/pingcap/tidb/pull/4194/files)
* [Add JSON in `fieldTypeMergeRules`.](https://github.com/pingcap/tidb/pull/4189)
* [Add support to MySQL connector 6.06.](https://github.com/pingcap/tidb/pull/4177)
* [Add Git branch name in `tidb_version()` and the starting log.](https://github.com/pingcap/tidb/pull/4168)
* [Add the `auto analyze` feature for tables.](https://github.com/pingcap/tidb/pull/4141)

## Fixed

* [DDL uses the `correct` method to check whether the context is done.](https://github.com/pingcap/tidb/pull/4221)
* [Close the PD client in TiKV store and raw KV to prevent connection leak.](https://github.com/pingcap/tidb/pull/4209)
* [Restore `WrapCastAsReal` and `WrapCastAsDecimal` if the argument is `ClassInt`.](https://github.com/pingcap/tidb/pull/4202)
* [Notify the fetching goroutines to exit when `IndexLookupExecutor` closes.](https://github.com/pingcap/tidb/pull/4201)
* [Fix the error in the return type for the `ceil`/`floor` function.](https://github.com/pingcap/tidb/pull/4181)
* [Start `GCWorker` after the bootstrapping is finished.](https://github.com/pingcap/tidb/pull/4167)
* [Add a limit to the number of multi-column index key parts.](https://github.com/pingcap/tidb/pull/4159)
* [Disable the `mysql.ClientMultiStatements` capability](https://github.com/pingcap/tidb/pull/4143)
* [Allow `username` to contain '@'.](https://github.com/pingcap/tidb/issues/3740)

## Improved

* [Handle canceled error by Grpc remote.](https://github.com/pingcap/tidb/pull/4237)
* [Remove all the stuff about the backgroud DDL worker.](https://github.com/pingcap/tidb/pull/4227)
* [Use more effective terror comparison method.](https://github.com/pingcap/tidb/pull/4217)
* [Union scan reuses PK when it is a handle.](https://github.com/pingcap/tidb/pull/4185)
* [Use `FieldType.Decimal` to control the decimal length of double values to be shown in client.](https://github.com/pingcap/tidb/pull/4191)
* [Support `time constant` pushdown in `mocktikv`.](https://github.com/pingcap/tidb/pull/4176)
* [Return the `unsupported` error in the type infer stage.](https://github.com/pingcap/tidb/pull/4156)
* Refactor the following expression/builtin-function evaluation framework:
  - [CRC32](https://github.com/pingcap/tidb/pull/4215)
  - [TIME](https://github.com/pingcap/tidb/pull/4192)
  - [HOUR, MINUTE, SECOND, MICROSECOND](https://github.com/pingcap/tidb/pull/4183)
  - [RAND, POW, SIGN, SQRT](https://github.com/pingcap/tidb/pull/4182)
  - [DIV](https://github.com/pingcap/tidb/pull/4180)
  - [TRUNCATE](https://github.com/pingcap/tidb/pull/4179)
  - [ANY_VALUE](https://github.com/pingcap/tidb/pull/4178)
  - [DNF](https://github.com/pingcap/tidb/pull/4174)
  - [NULLIF](https://github.com/pingcap/tidb/pull/4170)
  - [TIMESTAMPADD](https://github.com/pingcap/tidb/pull/4169)
  - [TO_SECONDS](https://github.com/pingcap/tidb/pull/4164)
  - [TO_DAYS](https://github.com/pingcap/tidb/pull/4161)
  - [CASE](https://github.com/pingcap/tidb/pull/4160)
  - [RADIANS](https://github.com/pingcap/tidb/pull/4155)
  - [OCT](https://github.com/pingcap/tidb/pull/4154)
  - [IS_IPV4, IS_IPV6, IS_IPV4_COMPAT, IS_IPV4_MAPP](https://github.com/pingcap/tidb/pull/4144)
  - [INET_ATON, INET_NTOA, INET6_ATON, INET6_NTOA](https://github.com/pingcap/tidb/pull/4130)
  - [TIME_FORMAT](https://github.com/pingcap/tidb/pull/4051)


## Weekly update in TiKV


Last week, We landed [33 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-08-13..2017-08-19&type=Issues) in the TiKV repositories.

## Added

* Add [hex/escaped converting](https://github.com/pingcap/tikv/pull/2143) for tikv-ctl.
* Implement the basic structure of [builtin_cast and some functions](https://github.com/pingcap/tikv/pull/2144) for DAG.
* Add [compare](https://github.com/pingcap/tikv/pull/2151) to new expression calculate framework.
* Support [leader resignation](https://github.com/pingcap/pd/pull/702) for PD.
* Add Git [branch information](https://github.com/pingcap/tikv/pull/2170) to the starting log.
* Support the [`mysql-time`](https://github.com/pingcap/tikv/pull/2177) constant.
* Add [Constant and Column](https://github.com/pingcap/tikv/pull/2179) for coprocessor.
* Add [RocksDB event metrics](https://github.com/pingcap/tikv/pull/2181).

## Fixed

* Declare [`config`](https://github.com/pingcap/tikv/pull/2164) for each CF explicitly.
* Use [millisecond resolution](https://github.com/pingcap/tikv/pull/2165) for the coarse Instant.
* Only collect [properties for `DBEntryType::Put`](https://github.com/pingcap/tikv/pull/2174).
* Allow [coarse error](https://github.com/pingcap/tikv/pull/2178).

## Improved

* Check [approximate size](https://github.com/pingcap/tikv/pull/2106) before split check.
* [Get snapshot](https://github.com/pingcap/tikv/pull/2111) in batches for coprocessor.
* [Get snapshot](https://github.com/pingcap/tikv/pull/2148) in batches for endpoint.
* Use separated thread to [flush metrics](https://github.com/pingcap/tikv/pull/2120).
* Use [histogram coarse timer](https://github.com/pingcap/tikv/pull/2159).
* Upgrade Rocksdb to [5.6.2](https://github.com/pingcap/tikv/pull/2166).
* Deprecate [v1 snapshot](https://github.com/pingcap/tikv/pull/2168).
* Reorganize the server [start up](https://github.com/pingcap/pd/pull/705) process for PD.
* [Broadcast](https://github.com/pingcap/tikv/pull/2184) when there is pending conf change.
