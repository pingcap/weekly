---
title: Weekly update (December 09 ~ December 15, 2019)
date: 2019-12-16
summary: Last week, we landed 62 PRs in the TiDB repository, 20 PRs in the TiSpark repository, and 37 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog post

JD Cloud, owned by JD.com (China's largest online retailer), is a full-service cloud computing platform and integrated cloud service provider. Previously, they used MySQL to store OSS metadata. But as the metadata grew rapidly, standalone MySQL couldn't meet their storage requirements. They faced severe challenges in storing unprecedented amounts of data that kept soaring.

Last week, we published a post written by Can Cui, an infrastructure specialist at JD Cloud, that deep dives into how TiKV, an open-source distributed transactional key-value database, empowered JD Cloud to manage huge amounts of OSS metadata with a simple and horizontally scalable architecture. The post introduces why they chose TiKV, how they're using it, and some thoughts about future plans.

The full article is here:

[Lesson Learned from 40 K QPS and 20+ Billion Rows of Data in a Single Scale-out Cluster](https://pingcap.com/success-stories/lesson-learned-from-40-k-qps-and-20-billion-rows-of-data-in-a-single-scale-out-cluster/)

## Community

### New contributors

tidb:

* [Tian-JQ](https://github.com/Tian-JQ)
* [gauss1314](https://github.com/gauss1314)
* [Thincher](https://github.com/Thincher)
* [knock-C](https://github.com/knock-C)

tikv:

* [Aloxaf](https://github.com/Aloxaf)
* [Rustin-Liu](https://github.com/Rustin-Liu)
* [hanahmily](https://github.com/hanahmily)

pd:

* [mantuliu](https://github.com/mantuliu)

## Call for participation

* [Vectorized Expression Working Group](https://github.com/pingcap/community/blob/master/working-groups/wg-vec-expr.md)
    * [`Date` or `Time` built-in functions (63/65)](https://github.com/pingcap/tidb/issues/12101)
    * [`Decimal` built-in functions (29/31)](https://github.com/pingcap/tidb/issues/12102)
    * [`Int` built-in functions (165/187)](https://github.com/pingcap/tidb/issues/12103)
    * [`JSON` built-in functions (23/27)](https://github.com/pingcap/tidb/issues/12104)
    * [`Real` built-in functions (47/49)](https://github.com/pingcap/tidb/issues/12105)
    * [`String` built-in functions (125/133)](https://github.com/pingcap/tidb/issues/12106)
    * [`Duration` built-in functions (42/45)](https://github.com/pingcap/tidb/issues/12176)
    * Last week, [6 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+sort%3Aupdated-desc+merged%3A2019-12-09..2019-12-15+label%3Acomponent%2Fexpression+) were landed in the expression component.

* Coprocessor SIG:
    * [Improve the performance of Chunk Encoder](https://github.com/tikv/tikv/issues/5729)
    * [Implement more UDFs](https://github.com/tikv/tikv/issues/5727)
    * [Implement the new row format](https://github.com/tikv/tikv/issues/5726)
    * [Port `BinaryJSON`](https://github.com/tikv/tikv/issues/5715)
    * [Tracing](https://github.com/tikv/tikv/issues/5714)
    * [The maximum execution time of Per-request](https://github.com/tikv/tikv/issues/5712)

* Planner SIG:
    * [Add rules for the cascades planner](https://github.com/pingcap/tidb/issues/13709)

* [More issues to solve for TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)
* [More issues to solve for TiKV](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

Last week, we landed [62 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-12-09..2019-12-15+) in the TiDB repository, [20 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-12-09..2019-12-15+) in the TiSpark repository, and [37 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-12-09..2019-12-15&type=Issues) in the TiKV and PD repositories.

### Critical PRs

TiDB:

* [Fix the bug that `VIEW`s can be dropped by the `DROP TABLE` syntax](https://github.com/pingcap/tidb/pull/14048)
* [Fix a memory leak issue in `batchClient` for large transactions](https://github.com/pingcap/tidb/pull/14031)
* [Add the `MergeAggregationProjection` transformation rule](https://github.com/pingcap/tidb/pull/13986)
* [Support the index advisor and complete the input preparation part](https://github.com/pingcap/tidb/pull/13968)
* [Make `rowcodec` used for mocktikv and unistore](https://github.com/pingcap/tidb/pull/13774)

TiSpark:

* [Release TiSpark 2.1.8](https://github.com/pingcap/tispark/pull/1305)
* [Fix the issue that `Residual Filter` contains wrong information](https://github.com/pingcap/tispark/pull/1308)
* [Add `TiChunkBatchColumnVector` to the `Chunk` data in batches](https://github.com/pingcap/tispark/pull/1292)

TiKV and PD:

* [Abstract a general forward scanner](https://github.com/tikv/tikv/pull/6218)
* [Support streaming for the diagnostics interface](https://github.com/tikv/tikv/pull/6229)
* [Add a flow control mechanism to ingest SST](https://github.com/tikv/tikv/pull/6202)
* [Add the maximum and minimum timestamp hint for the iterator](https://github.com/tikv/tikv/pull/6194)
* [Vectorize `bit_count`](https://github.com/tikv/tikv/pull/6184)
* [Vectorize `any_value`](https://github.com/tikv/tikv/pull/6164)
* [Vectorize `rand` and `rand_with_seed`](https://github.com/tikv/tikv/pull/6117)

## Upcoming TiDB event

[Paper reading (in Chinese) on Dec 16](https://github.com/pingcap/presentations/blob/master/paper-reading.md)
