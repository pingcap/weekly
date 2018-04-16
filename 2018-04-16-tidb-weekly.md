---
title: Weekly update (April 09 ~ April 15, 2018)
date: 2018-04-15
summary: Last week, we landed 32 PRs in the TiDB repositories, 3 PRs in the TiSpark repositories, and 25 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [32 PRs](https://github.com/search?p=1&q=repo%3Apingcap%2Ftidb+is%3Apr+is%3Amerged+merged%3A2018-04-09..2018-04-15&type=Issues) in the TiDB repositories.

## Added

- [Update the average column size dynamically](https://github.com/pingcap/tidb/pull/6170)
- [Update statistics using query feedback](https://github.com/pingcap/tidb/pull/6197)
- [Use `tidb_index_lookup_join_currency` to control the number of `IndexLookupJoin` inner workers](https://github.com/pingcap/tidb/pull/6240)
- [Add a TiDB system variable `tidb_hash_join_concurrency`](https://github.com/pingcap/tidb/pull/6244)
- [Make pseudo estimate ratio configurable](https://github.com/pingcap/tidb/pull/6254)
- [Show memory usage in `show processlist`](https://github.com/pingcap/tidb/pull/6266)

## Fixed

- [Make inferring of decimal for `unix_timestamp` more consistent with MySQL](https://github.com/pingcap/tidb/pull/6233)
- [Fix the bug of writing null value into not null column in write-only state](https://github.com/pingcap/tidb/pull/6249)
- [Fix the `IndexLookUpJoin` hang problem](https://github.com/pingcap/tidb/pull/6267)
- [Update the column's offset when modifying the column](https://github.com/pingcap/tidb/pull/6274)
- [Support `insert ignore` on duplicate update](https://github.com/pingcap/tidb/pull/6283)

## Improved

- [Set `explicit_defaults_for_timestamp = on` for compatibility with MySQL](https://github.com/pingcap/tidb/pull/6238)
- [Increase the default lease](https://github.com/pingcap/tidb/pull/6255)
- [Improve the performance of `Clone`](https://github.com/pingcap/tidb/pull/6260)
- [Use a cloned `Expression` when setting it to `plan`](https://github.com/pingcap/tidb/pull/6263)

# Weekly update in TiSpark

Last week, we landed [3 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-04-09..2018-04-15) in the TiSpark repositories.

## Added

- [Add `wrapper` for `Exception` handling](https://github.com/pingcap/tispark/pull/309)
- [Build a new RPC error handling framework](https://github.com/pingcap/tispark/pull/301)

# Weekly update in TiKV and PD

Last week, we landed [25 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-04-09..2018-04-15) in the TiKV and PD repositories.

## Added

- [Support Raft learner in `raftstore`](https://github.com/pingcap/tikv/pull/2726)
- [Support adding the learner node](https://github.com/pingcap/pd/pull/896)
- [Modify RocksDB cache size dynamically](https://github.com/pingcap/tikv/pull/2921)
- [Build `tikv-importer` as a standalone binary](https://github.com/pingcap/tikv/pull/2919)

## Fixed

- [Remove a misused RocksDB ticker](https://github.com/pingcap/tikv/pull/2940)
- [Disable `DeleteRange` by default](https://github.com/pingcap/tikv/pull/2927)
- [Avoid the panic caused by extreme conditions when generating snapshots](https://github.com/pingcap/tikv/pull/2923)
- [Fix the issue of allocating IDs frequently](https://github.com/pingcap/pd/pull/1013)

## Improved

- [Shrink queues into smaller ones to save memory when they are not used anymore](https://github.com/pingcap/tikv/pull/2943)
- [Simplify the process of `ImportSST::Upload` API](https://github.com/pingcap/tikv/pull/2920)
- [Process the `overflow_as_warning` flag](https://github.com/pingcap/tikv/pull/2901)
- [Collect the number of rows scanned for each range](https://github.com/pingcap/tikv/pull/2878)
- [Do not clear `taintCache` in `balanceRegionScheduler`](https://github.com/pingcap/pd/pull/1017)
- [Adjust the balance configuration](https://github.com/pingcap/pd/pull/1016)
- [Add `keepalive`](https://github.com/pingcap/tikv/pull/2926)
- [Fix the compatibility issue when adding a new scheduler](https://github.com/pingcap/pd/pull/1010)

# New contributors (Thanks!)

- TiKV: [Zhang Yuning](https://github.com/codeworm96)
- Docs: [John Liu](https://github.com/elitecodegroovy)
- Docs-cn: [yanchaozhong](https://github.com/yanchaozhong)