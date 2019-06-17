---
title: Weekly update (June 10 ~ June 16, 2019)
date: 2019-06-17
summary: Last week, we landed 40 PRs in the TiDB repository, 9 PRs in the TiSpark repository, and 37 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [40 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-06-10..2019-06-16+) in the TiDB repository.

## Added

- [Add a failpoint switch to control expression pushdown in the integration test](https://github.com/pingcap/tidb/pull/10786)
- [Add the `SplitTable` syntax to split table Regions](https://github.com/pingcap/tidb/pull/10553)
- [Allow using `SHARD_ROW_ID_BITS` for tables with auto-increment columns](https://github.com/pingcap/tidb/pull/10759)

## Improved

- [Support loading statistics when the statistics lease is 0](https://github.com/pingcap/tidb/pull/10771)
- [Disallow adding stored generated columns using `ALTER TABLE`](https://github.com/pingcap/tidb/pull/10758)
- [Adjust the datum type when using the index query feedback](https://github.com/pingcap/tidb/pull/10614)
- [Set `SyncerSessionTTL` to a smaller value](https://github.com/pingcap/tidb/pull/10371)
- [Add a blacklist to disallow pushing down specific expressions](https://github.com/pingcap/tidb/pull/10688)
- [Propagate more possible props to enlarge search space in the planner](https://github.com/pingcap/tidb/pull/10548)
- [Support resolving specified lock keys](https://github.com/pingcap/tidb/pull/10292)

## Fixed

- [Fix the `create table like` operation for partitioned tables](https://github.com/pingcap/tidb/pull/10785)
- [Fix an issue about `split table by`](https://github.com/pingcap/tidb/pull/10761)
- [Fix the wrong selectivity for the inner selection in index join](https://github.com/pingcap/tidb/pull/10633)
- [Fix the behavior when the output of `date_sub` is of the `Time` type](https://github.com/pingcap/tidb/pull/10607)
- [Fix some unnecessary loops in failures of running a range](https://github.com/pingcap/tidb/pull/10708)
- [Exclude keys that are already locked in `LockKeys`](https://github.com/pingcap/tidb/pull/10800)
- [Fix the issue that the backoff retry stops early](https://github.com/pingcap/tidb/pull/10809)

# Weekly update in TiSpark

Last week, we landed [9 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-06-10..2019-06-16+) in the TiSpark repository.

## Fixed

- [Fix a potential empty collection issue during Region pre-splitting](https://github.com/pingcap/tispark/pull/808)

## Improved

- [Add the TiDB/TiKV/PD/Spark version supported for each latest major release](https://github.com/pingcap/tispark/pull/804)

# Weekly update in TiKV and PD

Last week, we landed [37 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-06-10..2019-06-16&type=Issues) in the TiKV and PD repositories.

## Added

- [Add `blob-run-mode` for Titan](https://github.com/tikv/tikv/pull/4865)
- Pessimistic-txn
  - [Resolve all optimistic locks when a non-pessimistic lock conflict occurs](https://github.com/tikv/tikv/pull/4883)
  - [Add metrics](https://github.com/tikv/tikv/pull/4852)
  - [Implement pessimistic rollback](https://github.com/tikv/tikv/pull/4848)
- [Implement the `LIKE` RPN Function](https://github.com/tikv/tikv/pull/4847)
- [Add metrics for Titan](https://github.com/tikv/tikv/pull/4836)  
- [Use a different timeout for HTTP clients](https://github.com/pingcap/pd/pull/1574)
- [Add two metrics for `gc_worker`](https://github.com/tikv/tikv/pull/4705)

## Improved

- [Reduce allocations in slow hash aggregation](https://github.com/tikv/tikv/pull/4869)
- [Check the `iter` status when scanning](https://github.com/tikv/tikv/pull/4863)
- [Improve `bad_regions` and tombstone subcommands for tikv-ctl](https://github.com/tikv/tikv/pull/4862)
- [Always merge left Regions into right ones](https://github.com/pingcap/pd/pull/1564)
- [Use `spin::Mutex`](https://github.com/tikv/tikv/pull/4829)
- [Use static metrics to reduce the cost of `with_label_values`](https://github.com/tikv/tikv/pull/4826)
- [Avoid useless calculation and `WakeUp` messages](https://github.com/tikv/tikv/pull/4813)
- [Expire long remaining detection information in `DetectTable` to prevent memory leak](https://github.com/tikv/tikv/pull/4754)
- [Disable the label check by default](https://github.com/pingcap/pd/pull/1568)

## Fixed

- [Acquire the write lock for the write command](https://github.com/tikv/tikv/pull/4614)

# New contributors (Thanks!)

- tispark: [windtalker](https://github.com/windtalker)
- tikv: [xiamengyu](https://github.com/xiamengyu)
- tidb-operator: [tkanng](https://github.com/tkanng)
- pd: [b41sh](https://github.com/b41sh)
- docs-cn: [tangenta](https://github.com/tangenta)
