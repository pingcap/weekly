---
title: Weekly update (March 12 ~ March 18, 2018)
date: 2018-03-19
summary: Last week, we landed 60 PRs in the TiDB repositories, 14 PRs in the TiSpark repositories, and 29 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [60 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftidb+is%3Apr+is%3Amerged+merged%3A2018-03-12..2018-03-18) in the TiDB repositories.

## Added

- [Collect query feedbacks](https://github.com/pingcap/tidb/pull/5909)
- [Support `admin recover index`](https://github.com/pingcap/tidb/pull/5980)
- [Support retry and timeout for Coprocessor streaming API](https://github.com/pingcap/tidb/pull/5965)
- [Export implicit `rowid` and use it in CRUD](https://github.com/pingcap/tidb/pull/5984)

## Fixed

- [Fix the column length when converting the column information for `tinyint`](https://github.com/pingcap/tidb/pull/6008)
- [Add the deprecation warning for `builtin` function PASSWORD](https://github.com/pingcap/tidb/pull/6000)
- [Add missing columns in `collations_information_applicability`](https://github.com/pingcap/tidb/pull/6025)
- [Fix the comparison between `uint` and `int`](https://github.com/pingcap/tidb/pull/6028)
- [Fix the index iterator for unique index with a null value](https://github.com/pingcap/tidb/pull/6032)
- [Fix `insert into t1 (select * from t)`](https://github.com/pingcap/tidb/pull/6039)
- [Fix a bug when performing column substitution for join](https://github.com/pingcap/tidb/pull/6041)
- [Change `makeJoinRowToChunk` to account for virtual rows](https://github.com/pingcap/tidb/pull/6049)
- [Rollback the transaction when `Compile` returns `error`](https://github.com/pingcap/tidb/pull/6073)

## Improved

- [Add a unit test for `distsql.go`](https://github.com/pingcap/tidb/pull/5928)
- [Add the isolation test](https://github.com/pingcap/tidb/pull/5990)
- [Show more information on DDL history](https://github.com/pingcap/tidb/pull/6035)

# Weekly update in TiSpark

Last week, we landed [14 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-03-12..2018-03-18) in the TiSpark repositories and released [1.0-RC1](https://github.com/pingcap/tispark/releases/tag/1.0-RC1).

## Fixed

- [Fix the downgrade index scan logic to make it easier to downgrade](https://github.com/pingcap/tispark/pull/276)
- [Fix the prefix index logic for covering index](https://github.com/pingcap/tispark/pull/275)
- [Fix `0000-00-00` related test cases](https://github.com/pingcap/tispark/pull/273)
- [Rename the configuration item from `allow_index_double_read` to `allow_index_read`](https://github.com/pingcap/tispark/pull/270)
- [Map non-binary encoding blob to String type](https://github.com/pingcap/tispark/pull/269)
- [Make histogram loading compatible with TiDB of the earlier version](https://github.com/pingcap/tispark/pull/267)
- [Suppress JSON mapping exception](https://github.com/pingcap/tispark/pull/264)
- [Fix error handling for `OtherError` cases](https://github.com/pingcap/tispark/pull/277)
- [Fix the problem that the decimal precision is too large](https://github.com/pingcap/tispark/pull/285)

## Improved

- [Add statistics count in the plan for easier debugging](https://github.com/pingcap/tispark/pull/278)

## RC1 released

- [RC1 is released](https://github.com/pingcap/tispark/pull/263)

# Weekly update in TiKV and PD

Last week, we landed [29 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-03-12..2018-03-18) in the TiKV and PD repositories.

## Added

* [Add `raw_delete_range` interface](https://github.com/pingcap/tikv/pull/2825)
* [Support dump metrics](https://github.com/pingcap/tikv/pull/2824)
* [Add metrics for PD member health ](https://github.com/pingcap/pd/pull/990)
* [Support `merge`](https://github.com/pingcap/tikv/pull/2819)
* [Upgrade the indexmap](https://github.com/pingcap/tikv/pull/2816)
* [Dump statistics of `rocksdb` and `malloc`](https://github.com/pingcap/tikv/pull/2805)
* [Add the `consistency-check` subcommand to `tikv-ctl`](https://github.com/pingcap/tikv/pull/2750)
* [Implement `IngestSST` API](https://github.com/pingcap/tikv/pull/2712)

## Fixed

* [Fix Region size calculation](https://github.com/pingcap/pd/pull/992)
* [Apply a hotfix in `murmur3`](https://github.com/pingcap/tikv/pull/2828)
* [Make the PD mock server ignore the sending failure](https://github.com/pingcap/tikv/pull/2826)
* [Fix a bug that the help information always shows after `help`  is used once](https://github.com/pingcap/pd/pull/988)
* [Notify snapshot failure when resolving the remote address](https://github.com/pingcap/tikv/pull/2815)
* [Fix the pd-ctl post bug when `tls` is enabled](https://github.com/pingcap/pd/pull/987)
* [Fix a bug that too many pending Regions exist when `checker` adds peers to TiKV](https://github.com/pingcap/pd/pull/984)

## Improved

* [Poll significant message](https://github.com/pingcap/tikv/pull/2830)
* [Make the balance scheduler do not depend on the average score](https://github.com/pingcap/pd/pull/991)
* [Set the default value for `wal_bytes_per_sync` and `bytes_per_sync`](https://github.com/pingcap/tikv/pull/2818)
* [Make it possible to call the `apply` process recursively](https://github.com/pingcap/tikv/pull/2814)
* [Separate read pool configuration from `name_prefix`](https://github.com/pingcap/tikv/pull/2813)
* [Add assertion for error cases](https://github.com/pingcap/tikv/pull/2793)
* [Change the isolation level of PD Region label from Histogram to Gauge](https://github.com/pingcap/pd/pull/976)
* [Reclaim the disk space aggressively after data is deleted](https://github.com/pingcap/tikv/pull/2631)
* [Add Coprocessor streaming support](https://github.com/pingcap/tikv/pull/2478)

# New contributors (Thanks!)

- TiKV: [Hugo Wang](https://github.com/mitnk)
- Docs-cn: [康晓宁](https://github.com/kangxiaoning)