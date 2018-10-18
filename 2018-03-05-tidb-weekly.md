---
title: Weekly update (February 26 ~ March 04, 2018)
date: 2018-03-05
summary: Last week, we landed 27 PRs in the TiDB repositories, 4 PRs in the TiSpark repositories, and 12 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [27 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftidb+is%3Apr+is%3Amerged+merged%3A2018-02-26..2018-03-04) in the TiDB repositories.

## Added

* [Support stream aggregation on TiKV](https://github.com/pingcap/tidb/pull/5725)
* [Support long VARCHAR](https://github.com/pingcap/tidb/pull/5920)
* [Set `Range` and `OutputCounts` in Coprocessor Response for streaming API](https://github.com/pingcap/tidb/pull/5923)
* [Support `COMMENT = string` in partition definition](https://github.com/pingcap/tidb/pull/5933)
* [Add `restrict` and `cascade` in `DropTable`](https://github.com/pingcap/tidb/pull/5938)

## Fixed

* [Set `have_profiling` to `NO`](https://github.com/pingcap/tidb/pull/5907)

## Improved

* [Remove invalid intervals in building Range](https://github.com/pingcap/tidb/pull/5939)
* [Resolve locks in a batch](https://github.com/pingcap/tidb/pull/5750)
* [Extract the same part from DNF's leaves](https://github.com/pingcap/tidb/pull/5831)
* [Simplify the logic of HashCode](https://github.com/pingcap/tidb/pull/5911)
* [Improve the performance of decoding decimal](https://github.com/pingcap/tidb/pull/5921)
* Test coverage:
 - [Improve the test coverage in the `executor` package](https://github.com/pingcap/tidb/pull/5836)
 - [Improve the test coverage in the `plan` package](https://github.com/pingcap/tidb/pull/5929)
 - [Improve the test coverage in the `distsql` package](https://github.com/pingcap/tidb/pull/5908)
* Panic recover:
 - [Add the recover mechanism for index lookup reader workers](https://github.com/pingcap/tidb/pull/5913)
 - [Add the recover mechanism for `union` workers](https://github.com/pingcap/tidb/pull/5900)
 - [Add the recover panic in `owner.CampaignLoop`](https://github.com/pingcap/tidb/pull/5904)

# Weekly update in TiSpark

Last week, we landed [4 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-02-26..2018-03-04) in the TiSpark repositories.

## Added

* [Add the index covering optimization](https://github.com/pingcap/tispark/pull/148)
* [Add the broadcast join support](https://github.com/pingcap/tispark/pull/248)

## Improved

* [Add more tests](https://github.com/pingcap/tispark/pull/233)
* [Add DDL Dump for using TiDB as Spark MetaStore](https://github.com/pingcap/tispark/pull/247)

# Weekly update in TiKV and PD

Last week, we landed [12 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-02-26..2018-03-04) in the TiKV and PD repositories.

## Added

* [Export some `struct` expressions for other tools](https://github.com/pingcap/pd/pull/972)
* [Log panic stacks](https://github.com/pingcap/pd/pull/970)
* [Update the TiKV version](https://github.com/pingcap/tikv/pull/2782)
* [Add a Raft message flush metrics](https://github.com/pingcap/tikv/pull/2771)

## Fixed

* [Update the Rust dockerfile](https://github.com/pingcap/tikv/pull/2778)
* [Fix lowspace metrics](https://github.com/pingcap/pd/pull/965)
* [Check Regions in the background goroutine](https://github.com/pingcap/pd/pull/963)
* [Handle the problem that only one row returns in stream aggregation](https://github.com/pingcap/tikv/pull/2762)

## Improved

* [Rename a confused constant variable](https://github.com/pingcap/tikv/pull/2775)
* [Make `end_point_request_max_handle_secs` configurable](https://github.com/pingcap/tikv/pull/2769)
* [Precreate some labal metrics](https://github.com/pingcap/tikv/pull/2765)

# New contributor (Thanks!)

* TiKV: [Greg Weber](https://github.com/gregwebs)