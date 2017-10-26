---
date: 2017-01-01T00:00:00Z
title: Weekly Update
---

## Weekly update in TiDB

Last week, we landed [28 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-12-26..2017-01-01%20) in the TiDB repositories.

## Added

* [Support the `CHAR_LENGTH` built-in function.](https://github.com/pingcap/tidb/pull/2323)

* [Support the `CRC32` built-in function.](https://github.com/pingcap/tidb/pull/2347)

* [Support the `LEAST` built-in function.](https://github.com/pingcap/tidb/pull/2360)

## Fixed

* [Fix a bug in Add Column with invalid default value.](https://github.com/pingcap/tidb/pull/2316)

* [Fix a bug about parsing string to float.](https://github.com/pingcap/tidb/pull/2337)

* [Fix a bug when using int and uint as join key.](https://github.com/pingcap/tidb/pull/2355)

* [Fix a bug in MySQL Protocol layer about prepared statement.](https://github.com/pingcap/tidb/pull/2351)

## Improved

* [Improve string to date parser.](https://github.com/pingcap/tidb/pull/2310)

* [Improve TiDB schema lease checker.](https://github.com/pingcap/tidb/pull/2137)

* Refactor optimizer: [#2321](https://github.com/pingcap/tidb/pull/2321), [#2322](https://github.com/pingcap/tidb/pull/2322)

* [Set a limitation on the quantity of the data in a single transaction.](https://github.com/pingcap/tidb/pull/2325)

* [Improve mocked tikv](https://github.com/pingcap/tidb/pull/2331): Split data in a table into multiple mocked regions. This will used in unit tests.

* [Speed up creating table](https://github.com/pingcap/tidb/pull/2332): In some cases, it is not necessary to wait a long time to create table.

* [Use MySQL standard error code when meeting incorrect function argument count error.](https://github.com/pingcap/tidb/pull/2335)

* [Find a better way to handle StoreNotMatch error.](https://github.com/pingcap/tidb/pull/2339)

* Refactor built-in function: [#2343](https://github.com/pingcap/tidb/pull/2343), [#2344](https://github.com/pingcap/tidb/pull/2344), [#2362](https://github.com/pingcap/tidb/pull/2362), [#2367](https://github.com/pingcap/tidb/pull/2367)

* Clean up tidb-server codes: [#2356](https://github.com/pingcap/tidb/pull/2356), [#2358](https://github.com/pingcap/tidb/pull/2358)

## New contributor

* [Zyguan](https://github.com/zyguan)

* [AndreMouche](https://github.com/AndreMouche)

# Weekly update in TiKV

Last week, We landed [19 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2016-12-26..2017-01-01&type=Issues&ref=searchresults) in the TiKV repositories.

## Added

* Move `raw_get` to [thread pool](https://github.com/pingcap/tikv/pull/1434).

* Add `ResourceKind` for operator and don't resend duplicated `AddPeer` response when the peer is still pending, see [#449](https://github.com/pingcap/pd/pull/449).

* Add [member command](https://github.com/pingcap/pd/pull/455) for `pd-ctl`.

## Fixed

* Fix getting [valid float](https://github.com/pingcap/tikv/pull/1454).

## Improved

* Update default configuration to [speed up scheduler](https://github.com/pingcap/pd/pull/452).

* [Don't panic](https://github.com/pingcap/tikv/pull/1443) when receiving stale snapshot.

* Remove unnecessary [region cache](https://github.com/pingcap/pd/pull/457).

* Remove no used [constraint feature](https://github.com/pingcap/pd/pull/458).

* [Exit](https://github.com/pingcap/tikv/pull/1451) with error message if clusert ID mismatches directly.

* Add [replication section](https://github.com/pingcap/pd/pull/460) in configuration.
