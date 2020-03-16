---
title: Weekly update (March 09 ~ March 15, 2020)
date: 2020-03-16
summary: Last week, we landed 104 PRs in the TiDB repository and 57 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog post

Last week, we published a case study written by Chunhui Liu and Chao Hong (Database Administrators at Shopee) that discusses the following issues:

* Which databases is Shopee using?
* The importance of database selection
* Shopee's database selection strategy
* Factors to consider when choosing a database
* To shard or not to shard?
* Shopee's lessons learned in database selection
* How Shopee is using TiDB

The full article is here:

[Choosing the Right Database for Your Applications](https://pingcap.com/success-stories/choosing-right-database-for-your-applications/#which-databases-are-we-using-at-shopee)

## Community

### New contributors

tidb:

* [yzwqf](https://github.com/yzwqf)
* [zhang555](https://github.com/zhang555)

tikv:

* [ziyi-yan](https://github.com/ziyi-yan)

pd:

* [niedhui](https://github.com/niedhui)
* [wangrzneu](https://github.com/wangrzneu)

docs:

* [tsthght](https://github.com/tsthght)

docs-cn:

* [CharLotteiu](https://github.com/CharLotteiu)

dm:

* [chenlx0](https://github.com/chenlx0)

ansible:

* [hawkingrei](https://github.com/hawkingrei)

## Call for participation

### TiDB

* [Misleading log information when spilling to disk](https://github.com/pingcap/tidb/issues/15401)
* [Incompatible issues about the scalar functions](https://github.com/pingcap/tidb/issues/11223)

### TiKV

* New: [Support the slow query log searching](https://github.com/tikv/tikv/issues/7069)
* New: [Support auto flush metrics](https://github.com/tikv/tikv/issues/7062)
* New: [Optimize the performance of Coprocessor Analyze](https://github.com/tikv/tikv/issues/7039)
* [All help-wanted issues in TiKV](https://github.com/tikv/tikv/issues?q=is%3Aopen+is%3Aissue+label%3Astatus%2Fhelp-wanted)

### TiDB Dashboard

* New: [Support case insensitive log searching](https://github.com/pingcap-incubator/tidb-dashboard/issues/203)
* New: [Add left navigations for the diagnosis report](https://github.com/pingcap-incubator/tidb-dashboard/issues/200)
* [All help-wanted issues in TiDB Dashboard](https://github.com/pingcap-incubator/tidb-dashboard/issues?q=is%3Aopen+is%3Aissue+label%3Astatus%2Fhelp-wanted)

### TiDB Backup & Restore (BR)

* New: [Add the backup retry when some TiKV nodes get down](https://github.com/pingcap/br/issues/192)
* [All help-wanted issues in TiDB Backup & Restore](https://github.com/pingcap/br/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)

### TiDB Change Data Capture (CDC)

* New: [Refine the log and the standard output (stdout) of the CDC `cli` tool](https://github.com/pingcap/ticdc/issues/343)
* New: [Fix the DDL incompatibility issue between upstream and downstream](https://github.com/pingcap/ticdc/issues/266)
* [All help-wanted issues in TiDB Change Data Capture](https://github.com/pingcap/ticdc/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)

## Updates of the week

### Progress

Last week, we landed [104 PRs](https://github.com/pingcap/tidb/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-03-09..2020-03-15+) in the TiDB repository and [57 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2020-03-09..2020-03-15&type=Issues) in the TiKV and PD repositories.

#### TiDB Dashboard

* [Add the authentication support for TiDB Dashboard](https://github.com/pingcap-incubator/tidb-dashboard/pull/165)

#### CI collation

* [Add the support for the `COLLATE 'collate'` syntax](https://github.com/pingcap/tidb/pull/14959)
* [Move `ColumnsToProto` from Parser to TiDB and add the rewrite collate ID for `ColumnsToProto`](https://github.com/pingcap/tidb/pull/14971)
* [Make `field` and `findInSet` support the collation](https://github.com/pingcap/tidb/pull/15100)
* [Use `SetString()` for string instead of using `SetBytes`](https://github.com/pingcap/tidb/pull/14989)

#### TiUP

* [Implement the TiUP `status`/`clean`/`run` sub-commands](https://github.com/pingcap-incubator/tiup/pull/31)
* Release v0.0.1

#### OLTP performance

* [Push down locks to `PointGet` and `BatchPointGet`](https://github.com/pingcap/tidb/pull/15257)
* [Support the `min-overlap` compaction strategy in Badger](https://github.com/coocood/badger/pull/172)

#### OLAP performance

* [Support pushing down the bloom filter for `join`](https://github.com/pingcap/tidb/issues/15351)
* [Optimize `count distinct` to a single column](https://github.com/pingcap/tidb/issues/7539)

#### Improve `Explain`

* [Update the `Explain` information of outer Hash Joins](https://github.com/pingcap/tidb/pull/15247)
* [Refine the `Explain` format and content](https://github.com/pingcap/tidb/issues/15347)

#### SQL plan management

* [Set the text for the explainable statements](https://github.com/pingcap/parser/pull/763)
* [Support the partition baseline according to the parameter's selectivity](https://github.com/pingcap/tidb/pull/15281)

The progress of TiKV and PD:

* [Fix a bug that Coprocessor RocksDB statistics are incorrect due to the YATP thread switch](https://github.com/tikv/tikv/pull/6981)
* [Make keyvisual work in PD followers](https://github.com/pingcap/pd/pull/2218)

## On-going TiDB event

[TiDB Usability Challenge Program](https://pingcap.com/community/tidb-usability-challenge/)
