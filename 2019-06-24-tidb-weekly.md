---
title: Weekly update (June 17 ~ June 23, 2019)
date: 2019-06-24
summary: Last week, we landed 68 PRs in the TiDB repository, 12 PRs in the TiSpark repository, and 47 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [68 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-06-17..2019-06-23+) in the TiDB repository.

## Added

- [Add a column describing memory usage for `information_schema.processlist`](https://github.com/pingcap/tidb/pull/10837)
- [Add the `update-stats` bool configuration to control the updating statistics](https://github.com/pingcap/tidb/pull/10772)

## Improved

- [Remove expired keys from PD](https://github.com/pingcap/tidb/pull/10406)
- [Reuse the `tipb.Expr` value to push down expression `implicitParameters`](https://github.com/pingcap/tidb/pull/10790)
- [Make `RangeTaskRunner` support dividing tasks by Region](https://github.com/pingcap/tidb/pull/10482)
- [Notify affected Regions after sending `UnsafeDestroyRange` requests](https://github.com/pingcap/tidb/pull/10069)

## Fixed

- [Fix the `alter table drop partition` check on hash partitioned tables](https://github.com/pingcap/tidb/pull/10902)
- [Fix the wrong row count in fast `Analyze`](https://github.com/pingcap/tidb/pull/10859)
- [Fix the performance issue in the mixed transaction mode](https://github.com/pingcap/tidb/pull/10847)
- [Re-implement the `kill` statement in a safe way](https://github.com/pingcap/tidb/pull/10841)
- [Fix the `CMSketch` index for fast `Analyze`](https://github.com/pingcap/tidb/pull/10839)
- [Fix the configuration JSON key of `PessimisticTxn`](https://github.com/pingcap/tidb/pull/10820)
- [Fix the issue that the `pb` memory cannot be released quickly](https://github.com/pingcap/tidb/pull/10815)
- [Fix the issue that GC stops working when an error occurs during the execution process of the `UnsafeDestroyRange` operation](https://github.com/pingcap/tidb/pull/10743)

# Weekly update in TiSpark

Last week, we landed [12 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-06-17..2019-06-23+) in the TiSpark repository.

## Added

- [Add a feature of locking a table](https://github.com/pingcap/tispark/pull/824)
- [Add documents about `Timezone` and support writing data of the `Timestamp` type](https://github.com/pingcap/tispark/pull/842)

## Improved

- [Update Spark version for the `spark_2.4` profile to Spark 2.4.3](https://github.com/pingcap/tispark/pull/852)
- [Extend `JODA DateTime` to support scaling `Timestamp` up to microseconds](https://github.com/pingcap/tispark/pull/853)

# Weekly update in TiKV and PD

Last week, we landed [47 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-06-17..2019-06-23&type=Issues) in the TiKV and PD repositories.

## Improved

- [Adjust the meaning for `store-balance-rate`](https://github.com/pingcap/pd/pull/1589)
- [Resolve the problem that stores might be overloaded for a long time](https://github.com/pingcap/pd/pull/1586)
- [Validate `block-size` in the column family option of RocksDB](https://github.com/tikv/tikv/pull/4920)
- [Add a command to show the replication configuration in pd-ctl](https://github.com/pingcap/pd/pull/1587)
- [Do not support dynamic allocation in `decimal`](https://github.com/tikv/tikv/pull/4909)

## Added

- [Implement the `if_null` RPN Function](https://github.com/tikv/tikv/pull/4911)
- [Implement the `add_time_string_null` RPN Function](https://github.com/tikv/tikv/pull/4855)

# New contributors (Thanks!)

tikv:

* [NOVA-ME](https://github.com/NOVA-ME)
* [summer-slow-grace](https://github.com/summer-slow-grace)
