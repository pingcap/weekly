---
title: Weekly update (March 19 ~ March 25, 2018)
date: 2018-03-26
summary: Last week, we landed 35 PRs in the TiDB repositories, 4 PRs in the TiSpark repositories, and 26 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [35 PRs](https://github.com/search?p=3&q=repo%3Apingcap%2Ftidb+is%3Apr+is%3Amerged+merged%3A2018-03-19..2018-03-25&type=Issues&utf8=%E2%9C%93) in the TiDB repositories.

## Added

* [Add the average column size for `histogram`](https://github.com/pingcap/tidb/pull/5974)
* [Support `STRAIGHT_JOIN` to disable join reordering](https://github.com/pingcap/tidb/pull/6007)
* [Add the `AdminChecksumTable` command](https://github.com/pingcap/tidb/pull/6067)
* [Show Region key's record ID or index values](https://github.com/pingcap/tidb/pull/6030)

## Fixed

* [Support converting `json` to `float64`](https://github.com/pingcap/tidb/pull/6081)
* [Fix incompatible behavior when modifying value from Navicat GUI](https://github.com/pingcap/tidb/pull/6105)
* [Fix panic by cloning the predicates of `UnionScan`](https://github.com/pingcap/tidb/pull/6124)
* [Fix the syntax error on `set transaction isolation level serializable`](https://github.com/pingcap/tidb/pull/6131)
* [Fix a data race on the concurrent access of `Tracker.children`](https://github.com/pingcap/tidb/pull/6108)
* [Fix a data race for the `SelectForUpdate` executor](https://github.com/pingcap/tidb/pull/6096)

## Improved

* [Speed up adding index for discrete tables](https://github.com/pingcap/tidb/pull/5964)
* [Refactor `MergeJoin`](https://github.com/pingcap/tidb/pull/6078)
* [Fill the `TABLE_ROWS` field of `information_schema.TABLES` with the information from statistics](https://github.com/pingcap/tidb/pull/6111)

# Weekly update in TiSpark

Last week, we landed [4 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-03-19..2018-03-25) in the TiSpark repositories.

## Fixed

* [Fix the range of the prefix index](https://github.com/pingcap/tispark/pull/292)
* [Fix the bucket loading issue](https://github.com/pingcap/tispark/pull/288)

# Weekly update in TiKV and PD

Last week, we landed [26 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-03-19..2018-03-25) in the TiKV and PD repositories.

## Added

* [Dump the snapshot meta file](https://github.com/pingcap/tikv/pull/2847)
* [Modify the TiKV configuration dynamically](https://github.com/pingcap/tikv/pull/2838)
* [Implement the `checksum` push down request](https://github.com/pingcap/tikv/pull/2822)
* [Support Region merging](https://github.com/pingcap/tikv/pull/2502)
* [Add the checker for Region merging](https://github.com/pingcap/pd/pull/839)
* [Support TiKV recovering services from the unsafe state of the majority failure of replicas](https://github.com/pingcap/tikv/pull/2743)

## Fixed

* [Replace `%I` with `%H`](https://github.com/pingcap/tikv/pull/2836)
* [Transfer the leader to the new peer when scattering Regions](https://github.com/pingcap/pd/pull/995)

## Improved

* [Improve the `balance-region` scheduler](https://github.com/pingcap/pd/pull/1000)
* [Improve the `balance-leader` scheduler](https://github.com/pingcap/pd/pull/996)
* [Simplify the `shuffle-leader` scheduler](https://github.com/pingcap/pd/pull/993)
* [Inform PD ASAP after new peers are not pending any more](https://github.com/pingcap/tikv/pull/2786)
* [Use `delete range` by default](https://github.com/pingcap/tikv/pull/2806)
* [Pick the hot Region from the store randomly](https://github.com/pingcap/pd/pull/994)
* [Refactor the worker with `crossbeam-channel`](https://github.com/pingcap/tikv/pull/2846)

# New contributors (Thanks!)

TiDB:

- [lwh](https://github.com/lwhile)

TiKV:

- [csmoe](https://github.com/csmoe)
- [wspsxing](https://github.com/biluohc)

Docs:

- [Ryan Brewster](https://github.com/ryanpbrewster)