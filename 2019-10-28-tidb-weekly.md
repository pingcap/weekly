---
title: Weekly update (October 21 ~ October 27, 2019)
date: 2019-10-28
summary: Last week, we landed 60 PRs in the TiDB repository, 6 PRs in the TiSpark repository, and 28 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## Community

### New contributors

tidb:

* [young-127](https://github.com/young-127)
* [yongchaoyan](https://github.com/yongchaoyan)
* [chacha923](https://github.com/chacha923)
* [liugangjian](https://github.com/liugangjian)

parser:

* [ekalinin](https://github.com/ekalinin)
* [sim41](https://github.com/sim41)

docs-cn:

* [elvizlai](https://github.com/elvizlai)

## Call for participation

* [Vectorized Expression Working Group](https://github.com/pingcap/community/blob/master/working-groups/wg-vec-expr.md)
  * [`Date` or `Time` built-in functions (14/65)](https://github.com/pingcap/tidb/issues/12101)
  * [`Decimal` built-in functions (15/31)](https://github.com/pingcap/tidb/issues/12102)
  * [`Int` built-in functions (69/187)](https://github.com/pingcap/tidb/issues/12103)
  * [`JSON` built-in functions (13/27)](https://github.com/pingcap/tidb/issues/12104)
  * [`Real` built-in functions (41/49)](https://github.com/pingcap/tidb/issues/12105)
  * [`String` built-in functions (53/133)](https://github.com/pingcap/tidb/issues/12106)
  * [`Duration` built-in functions (13/45)](https://github.com/pingcap/tidb/issues/12176)
  * Last week, [30 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+sort%3Aupdated-desc+merged%3A2019-10-21..2019-10-27+label%3Acomponent%2Fexpression) are landed in the expression component.
* [Issues to solve for TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)
* [Issues to solve for TiKV](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

Last week, we landed [60 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-10-21..2019-10-27+) in the TiDB repository, [6 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-10-21..2019-10-27+) in the TiSpark repository, and [28 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-10-21..2019-10-27&type=Issues) in the TiKV and PD repositories.

### Critical PRs

TiDB:

* [Introduce `TransformationID` in the cascades planner](https://github.com/pingcap/tidb/pull/12879)
* [Fix the issue that the snapshot does not cache the non-existing KV entries that lead to the poor `insert ignore` performance](https://github.com/pingcap/tidb/pull/12872)
* [Reuse the chunk row for the row insertion on the duplicate update](https://github.com/pingcap/tidb/pull/12847)
* [Fix the panic caused by the data race in `GetDirtyTable()`](https://github.com/pingcap/tidb/pull/12767)
* [Support `CREATE VIEW` on the union](https://github.com/pingcap/tidb/pull/12595)
* [Make requests fail quickly when the dial times out](https://github.com/pingcap/tidb/pull/12819)???

TiSpark:

* [Fix the `No Matching column` bug](https://github.com/pingcap/tispark/pull/1162)

TiKV and PD:

* [Add the checksum feature for the backup and restore](https://github.com/tikv/tikv/pull/5683)
* [Update the rust-rocksdb to avoid the intra-L0 compaction issue](https://github.com/tikv/tikv/pull/5710)
* [Revert the `approximate` update in the pd-worker](https://github.com/tikv/tikv/pull/5711)
* [Add `used_size` for the store API](https://github.com/pingcap/pd/pull/1844/files)
* [Fix the race issue of the scatter range scheduler](https://github.com/pingcap/pd/pull/1840)
* [Add options to enable the placement rules](https://github.com/pingcap/pd/pull/1835)
