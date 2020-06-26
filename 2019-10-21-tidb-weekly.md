---
title: Weekly update (October 14 ~ October 20, 2019)
date: 2019-10-21
summary: Last two weeks, we landed 132 PRs in the TiDB repository, 6 PRs in the TiSpark repository, and 45 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## Community

### New contributors

tidb:

* [mmyj](https://github.com/mmyj)
* [js00070](https://github.com/js00070)
* [ZhaoQian888](https://github.com/ZhaoQian888)
* [justarandomstring](https://github.com/justarandomstring)
* [XiaTianliang](https://github.com/XiaTianliang)
* [rogaps](https://github.com/rogaps)

parser:

* [tsthght](https://github.com/tsthght)

## Call for participation

* [Redefine System Variables with Golang type](https://github.com/pingcap/tidb/issues/11269)
* [Vectorized Expression Working Group](https://github.com/pingcap/community/blob/master/working-groups/wg-vec-expr.md)
  * [`Date` or `Time` built-in functions (11/65)](https://github.com/pingcap/tidb/issues/12101)
  * [`Decimal` built-in functions (9/31)](https://github.com/pingcap/tidb/issues/12102)
  * [`Int` built-in functions (55/187)](https://github.com/pingcap/tidb/issues/12103)
  * [`JSON` built-in functions (3/27)](https://github.com/pingcap/tidb/issues/12104)
  * [`Real` built-in functions (38/49)](https://github.com/pingcap/tidb/issues/12105)
  * [`String` built-in functions (32/133)](https://github.com/pingcap/tidb/issues/12106)
  * [`Duration` built-in functions (5/45)](https://github.com/pingcap/tidb/issues/12176)
  * Total Progress (153/537)
  * [67 PRs](https://github.com/pingcap/tidb/pulls?page=1&q=is%3Apr+is%3Amerged+sort%3Aupdated-desc+merged%3A>%3D2019-10-14+label%3Acomponent%2Fexpression&utf8=✓) are landed in the expression component

* [Other issues to solve in TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)
* [Other issues to solve in TiKV](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

Last week, we landed [132 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-10-14..2019-10-21+) in the TiDB repository, [6 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-10-14..2019-10-20+) in the TiSpark repository, [45 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-10-14..2019-10-20&type=Issues) in the TiKV and PD repositories.

### Critical PRs

TiDB:

* [Fix bugs for the shallow copy](https://github.com/pingcap/tidb/pull/12691)
* [Fix the issue that KV requests might be processed slower because the connection to some KV servers is slow to establish](https://github.com/pingcap/tidb/pull/12733)
* [Refactor the `ResolveLocks()` function for the implementation of large transactions](https://github.com/pingcap/tidb/pull/11999)
* [Eliminate the unnecessary pessimistic rollback](https://github.com/pingcap/tidb/pull/12561)
* [Make the `IndexHashJoin` support keep the outer order](https://github.com/pingcap/tidb/pull/12349)
* [Fix the permanent hanging when `HashAgg` is called by `Apply`](https://github.com/pingcap/tidb/pull/12760)
* [Support `IndexLookUpMergeJoin` in the executor](https://github.com/pingcap/tidb/pull/12024)
* [Support splitting Regions for the partition table](https://github.com/pingcap/tidb/pull/12213)
* [Add the `json_valid` built-in function](https://github.com/pingcap/tidb/pull/12596)
* [Make the selection executor support the vectorized expression evaluation](https://github.com/pingcap/tidb/pull/12220)
* [Record and print the plan in slow logs](https://github.com/pingcap/tidb/pull/12179)
* [Support automatically creating SQL baselines](https://github.com/pingcap/tidb/pull/12434)
* [Disable the constant propagation for `AntiSemiJoin`](https://github.com/pingcap/tidb/pull/12728)
* [Introduce the `preprocessing` phase in the cascades planner](https://github.com/pingcap/tidb/pull/12649)
* [Fix a compatibility issue that if the foreign key constraint in the `CREATE TABLE` statement has no schema, schema of the created table should be used instead of returning the `No Database selected` error](https://github.com/pingcap/tidb/pull/12548)
* [Check whether the column type in the range column partitioning table and the value type of the `less than xxx` expression in partition are consistent](https://github.com/pingcap/tidb/pull/12664)
* [Fix the `CREATE TABLE` check for the range column partition](https://github.com/pingcap/tidb/pull/12622)
* [Avoid writing the untouched index in the auto-commit transaction and avoid getting the untouched index key from TiKV](https://github.com/pingcap/tidb/pull/12609)

TiSpark:

* [Fix a bug in the default value of the `Bit` type](https://github.com/pingcap/tispark/pull/1148)
* [Fix the cost model](https://github.com/pingcap/tispark/pull/1150)

TiKV and PD:

* [Fix the issue that the blob file is missing in Titan](https://github.com/tikv/tikv/pull/5668)
* [Fix the issue that `check_txn_status` does not write the rollback record when the key does not exist](https://github.com/tikv/tikv/pull/5673)
* [Protect the primary locks of pessimistic transactions from being collapsed](https://github.com/tikv/tikv/pull/5575)
* [Decouple the GC worker from storage](https://github.com/tikv/tikv/pull/5663)
* [Fix the data race issue when cloning `StoreInfo`](https://github.com/pingcap/pd/pull/1802)
* [Support the balance leader according to the leader count](https://github.com/pingcap/pd/pull/1743)

## Upcoming TiDB events

[TiDB Hackathon 2019 (in Chinese)](https://github.com/pingcap/presentations/tree/master/hackathon-2019/)

* Time: 26th to 27th October, 2019 (UTC/GMT+08:00)
* Location: PingCAP offices in Beijing, Shanghai and Guangzhou
