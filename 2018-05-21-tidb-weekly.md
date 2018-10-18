---
title: Weekly update (May 14 ~ May 20, 2018)
date: 2018-05-21
summary: Last week, we landed 40 PRs in the TiDB repositories, 4 PRs in the TiSpark repositories, and 35 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [40 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-05-14..2018-05-20) in the TiDB repositories.

## Added

- [Support `TIME` and `TIMESTAMP` binary types for the `PREPARE`/`EXECUTE` statements](https://github.com/pingcap/tidb/pull/6516)
- [Make `tidb_build_stats_concurrency` a global variable](https://github.com/pingcap/tidb/pull/6558)
- [Support `USE INDEX` in the `DELETE FROM` statement](https://github.com/pingcap/tidb/pull/6570)

## Fixed

- [Fix the compatibility problem of the `UNION` statement](https://github.com/pingcap/tidb/pull/6335)
- [Fix range calculation of `Index Scan` when `Prepared Plan Cache` is enabled](https://github.com/pingcap/tidb/pull/6539)
- [Check the `AUTO_INCREMENT` column for the `SHARD_ROW_ID_BITS` statement](https://github.com/pingcap/tidb/pull/6572)
- [Set PB code for `builtinArithmeticDivideDecimalSig`](https://github.com/pingcap/tidb/pull/6583)

## Improved

- [Refine the error message about `Invalid default value`](https://github.com/pingcap/tidb/pull/6333)
- [Make the error log for `WriteConflict` more friendly ](https://github.com/pingcap/tidb/pull/6457)
- [Add the schema version to the log](https://github.com/pingcap/tidb/pull/6527)
- [Support warnings when using Coprocessor streaming](https://github.com/pingcap/tidb/pull/6544)
- [Add the DDL Callback log](https://github.com/pingcap/tidb/pull/6549)
- [Do not log `handshake error`](https://github.com/pingcap/tidb/pull/6552)
- [Log slow processing and waiting Coprocessor tasks separately with different labels](https://github.com/pingcap/tidb/pull/6553)
- [Do not bind graceful shutdown to `SIGTERM`](https://github.com/pingcap/tidb/pull/6562)

# Weekly update in TiSpark

Last week, we landed [4 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-05-14..2018-05-20) in the TiSpark repositories.

## Fixed

- [Fix the `DateTime` parse error when `DateTime` is in DST gap](https://github.com/pingcap/tispark/pull/347)
- [Fix the `count(1)` function used with the `limit` clause](https://github.com/pingcap/tispark/pull/346)

## Improved

- [Make the `tidbMapTable` method return the corresponding `DataFrame`](https://github.com/pingcap/tispark/pull/349)
- [Improve the query plan test](https://github.com/pingcap/tispark/pull/344)

# Weekly update in TiKV and PD

Last week, we landed [35 PRs](https://github.com/search?p=1&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-05-14..2018-05-20&type=Issues&utf8=%E2%9C%93) in the TiKV and PD repositories.

## Added

- [Use `slog` via the `slog_stdlog` crate](https://github.com/pingcap/tikv/pull/3010)
- [Support compression in the gRPC layer](https://github.com/pingcap/tikv/pull/3088)

## Fixed

- [Fix the issue that split might cause dirty read in extreme conditions](https://github.com/pingcap/tikv/pull/3045)
- [Correct the default value of the read thread pool configuration](https://github.com/pingcap/tikv/pull/3058)
- [Fix load Region failure due to too large packet size](https://github.com/pingcap/pd/pull/1064)
- [Fix the issue that Learner cannot be successfully elected in special conditions](https://github.com/pingcap/tikv/pull/3069)

## Improved

- [Speed up decoding datum and table](https://github.com/pingcap/tikv/pull/3060)
- [Speed up `Deleting Range`](https://github.com/pingcap/tikv/pull/3046)
- [Update the gRPC version](https://github.com/pingcap/pd/pull/1062)
- [Make Label scheduler take care of unhealthy Regions](https://github.com/pingcap/pd/pull/1079)
- [Adjust timeout time for the operator which only contains `TransferLeader`](https://github.com/pingcap/pd/pull/1077)
- [Filter disconnected stores for leader transfer](https://github.com/pingcap/pd/pull/1072)