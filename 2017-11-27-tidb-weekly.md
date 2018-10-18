---
title: Weekly update (November 20 ~ November 26, 2017)
date: 2017-11-27
summary: Last week, we landed 60 PRs in the TiDB repositories, 5 PRs in the TiSpark repositories, and 10 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [60 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is:pr%20is:merged%20merged:2017-11-20..2017-11-26) in the TiDB repositories.

## Added

* [Support the `Create View` syntax](https://github.com/pingcap/tidb/pull/5197).
* [Support the `PAD_CHAR_TO_FULL_LENGTH` sql_mode.](https://github.com/pingcap/tidb/pull/5065)
* [Support the `PROXY` protocol.](https://github.com/pingcap/tidb/pull/3757)

## Fixed

* [Fix a bug in `retry()`.](https://github.com/pingcap/tidb/pull/5202)
* [Fix a bug about parse duration when the fsp round overflows 60 seconds.](https://github.com/pingcap/tidb/pull/5199)
* [Fix the missing index update about automatic updating for TIMESTAMP.](https://github.com/pingcap/tidb/pull/5176)
* [Fix a bug when `val > MaxInt32` in the `from_unixtime` argument.](https://github.com/pingcap/tidb/pull/5170)
* [Clean up the goroutine after closing a domain.](https://github.com/pingcap/tidb/pull/5163)
* [Deep clone TopN when pushing it down through `Join`.](https://github.com/pingcap/tidb/pull/5158)
* [Add overflow `Truncate` when converting `Str` to `Float`.](https://github.com/pingcap/tidb/pull/5130)
* [The password used to grant the privilege should be a hash string.](https://github.com/pingcap/tidb/pull/5129)
* [Throw out error if the index hint not exist.](https://github.com/pingcap/tidb/pull/4951)
* [Fix an invalid time cast bug.](https://github.com/pingcap/tidb/pull/4338)

## Improved

* [Use `Chunk` in `TableReader`.](https://github.com/pingcap/tidb/pull/5142)
* [Support `Chunk` in `IndexLookupReader`.](https://github.com/pingcap/tidb/pull/5206)
* [Support `Chunk` in `ProjectionExec`.](https://github.com/pingcap/tidb/pull/5178)
* [Make `chunk.Row` iterable.](https://github.com/pingcap/tidb/pull/5196)
* [Load the `stats` table asynchronously.](https://github.com/pingcap/tidb/pull/5188)
* [Support vectorized execution of expressions.](https://github.com/pingcap/tidb/pull/5184)
* [Avoid updating delta when the modified count is 0.](https://github.com/pingcap/tidb/pull/5162)
* [Limit the length of the index name.](https://github.com/pingcap/tidb/pull/5161)
* [Support the builtin aggregation function `bit_and`.](https://github.com/pingcap/tidb/pull/5147)

# Weekly update in TiSpark

Last week, we landed [5 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2017-11-20..2017-11-26) in the TiSpark repositories.

## Added

* [Add the code format for `scala`.](https://github.com/pingcap/tispark/pull/95)

## Fixed

* [Fix a column binding error which prevents the pushdown.](https://github.com/pingcap/tispark/pull/87) 
* [Fix the integration test loading.](https://github.com/pingcap/tispark/pull/92)
* [Fix the Stale Region error.](https://github.com/pingcap/tikv-client-lib-java/pull/149)

## Improved

* [Upgrade to GRPC 1.7.](https://github.com/pingcap/tikv-client-lib-java/pull/157)

# Weekly update in TiKV

Last week, we landed [10 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-11-20..2017-11-26) in the TiKV repositories.

## Added

* [Add the fake TiKV.](https://github.com/pingcap/pd/pull/854)
* [Support the namespace configuration.](https://github.com/pingcap/pd/pull/858)

## Fixed

* [Fix potential disk full due to too many stale snapshots.](https://github.com/pingcap/tikv/pull/2429)
* [Fix `Chunk` count detection.](https://github.com/pingcap/tikv/pull/2480)
* [Fix a deadlock when trying to reconnect to PD.](https://github.com/pingcap/tikv/pull/2493)

## Improved

* [Update to protobuf 3.](https://github.com/pingcap/tikv/pull/2485)
* [Adjust the gRPC metrics.](https://github.com/pingcap/tikv/pull/2488)
* [Clean up codes.](https://github.com/pingcap/tikv/pull/2500)

# New contributors (Thanks!)

TiDB:

- [ZhengQian](https://github.com/buggithubs)
- [Zheng Dayu](https://github.com/ceshihao)
