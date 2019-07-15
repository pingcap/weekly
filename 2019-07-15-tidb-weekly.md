---
title: Weekly update (July 08 ~ July 14, 2019)
date: 2019-07-15
summary: Last week, we landed 65 PRs in the TiDB repository, 5 PRs in the TiSpark repository, and 40 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [65 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-07-08..2019-07-14+) in the TiDB repository.

## Added

- [Add trace support for the `AllocAutoIncrementValue` function](https://github.com/pingcap/tidb/pull/11158)
- [Add the `json_array_insert` built-in function](https://github.com/pingcap/tidb/pull/11076)
- [Add metrics for fast `Analyze`](https://github.com/pingcap/tidb/pull/11079)
- [Add the `SHOW TABLE REGIONS` syntax](https://github.com/pingcap/tidb/pull/10612)
- [Add the `ADMIN CLEANUP TABLE LOCK` syntax for support](https://github.com/pingcap/tidb/pull/10423)

## Improved

- [Do not split the index when creating tables](https://github.com/pingcap/tidb/pull/11183)
- [Improve the logic of data loading in batch](https://github.com/pingcap/tidb/pull/11132)
- [Refine the error messages in unsupported column options](https://github.com/pingcap/tidb/pull/11065)
- [Support the dynamic `enable`/`disable` plugins](https://github.com/pingcap/tidb/pull/11122)
- [Support subqueries in the `SHOW` statement](https://github.com/pingcap/tidb/pull/10942)

## Fixed

- [Fix a bug of `point get` when meeting null values](https://github.com/pingcap/tidb/pull/11219)
- [Fix a bug of the `insert on duplicate update` statement on the partitioned table](https://github.com/pingcap/tidb/pull/11204)
- [Fix a bug of union scan on the partitioned table](https://github.com/pingcap/tidb/pull/11187)
- [Fix the data race for the `rand` function](https://github.com/pingcap/tidb/pull/11168)
- [Handle the `explain analyze` panic when processing the `explain analyze insert ... select` statements](https://github.com/pingcap/tidb/pull/11162)
- [Fix a bug for `int column <cmp> non-int constant`](https://github.com/pingcap/tidb/pull/11050)
- [Fix the privilege check for `show create user current_user()`](https://github.com/pingcap/tidb/pull/11142)
- [Fix the issue that index join fails to correctly handle the index with prefix length](https://github.com/pingcap/tidb/pull/11081)
- [Fix a bug when pruning columns for `TableDual`](https://github.com/pingcap/tidb/pull/11054)
- [Fix the incorrect `weekday` for the `ALLOW_INVALID_DATES` mode](https://github.com/pingcap/tidb/pull/10864)
- [Fix an error in the `update` privilege](https://github.com/pingcap/tidb/pull/10087)

# Weekly update in TiSpark

Last week, we landed [5 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-07-08..2019-07-14+) in the TiSpark repository.

## Added

- [Add documents for reading the partitioned table](https://github.com/pingcap/tispark/pull/916)

# Weekly update in TiKV and PD

Last week, we landed [40 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-07-08..2019-07-14&type=Issues) in the TiKV and PD repositories.

## Improved

- [Remove the unnecessary clone](https://github.com/tikv/tikv/pull/5039)
- [Support the `RPN` function validator](https://github.com/tikv/tikv/pull/5033)
- [Balance Regions to address `pending peers`](https://github.com/pingcap/pd/pull/1617)
- [Replace `Hashbrown` with the `std` `HashMap` implementation](https://github.com/tikv/tikv/pull/5010)
- [Fix the issue that `balanceRegionScheduler` always selects the same source and target](https://github.com/pingcap/pd/pull/1442)

## Added

- [Add a Regions dumper](https://github.com/pingcap/pd/pull/1631)
- [Specify multiple PD addresses separated by commas](https://github.com/pingcap/pd/pull/1629)
- [Add the `mimalloc` feature to `tikv_alloc`](https://github.com/tikv/tikv/pull/5041)
- [Add `IntDivideInt` and `IntDivideDecimal` for `rpn_expr`](https://github.com/tikv/tikv/pull/4983)
- [Add the `skip-paranoid-checks` flag for `tikv-ctl`](https://github.com/tikv/tikv/pull/4819)

## Fixed

- [Fix the merge-related operators in waiting operators](https://github.com/pingcap/pd/pull/1633)
- [Fix `Duration::parse` while the input is empty](https://github.com/tikv/tikv/pull/5066)
- [Scan versions from `u64::max` to `start_ts` in `get_txn_commit_info`](https://github.com/tikv/tikv/pull/5062)
- [Count the size of blob files in the disk space used by RocksDB](https://github.com/tikv/tikv/pull/5060)
- [Call `_exit` instead of `exit` in `panic hook`](https://github.com/tikv/tikv/pull/5053)
- [Fix `test_node_request_snapshot_reject_merge`](https://github.com/tikv/tikv/pull/5056)

# New contributors (Thanks!)

tidb:

- [tptpp](https://github.com/tptpp)

tikv:

- [divinerapier](https://github.com/divinerapier)
- [psinghal20](https://github.com/psinghal20)

docs-cn:

- [tptpp](https://github.com/tptpp)
