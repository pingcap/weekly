---
title: Weekly update (October 30 ~ November 05, 2017)
date: 2017-11-06
summary: Last week, we landed 51 PRs in the TiDB repositories and 16 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV']
---

# Weekly update in TiDB

Last week, we landed [51 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-10-30..2017-11-05) in the TiDB repositories.

## Added
* [Provide the command option and log the success/fail information for slow-query.](https://github.com/pingcap/tidb/pull/4934)

## Removed
* [Remove the old planner.](https://github.com/pingcap/tidb/pull/4979)
* [Remove `xeval`.](https://github.com/pingcap/tidb/pull/4978)
* [Remove the `localstore` storage engine.](https://github.com/pingcap/tidb/pull/4976)

## Fixed
* [Change the selection plan to dual plan directly if the condition is always false.](https://github.com/pingcap/tidb/pull/4980)
* [Insert column char(4) with latin1 charset by incorrect padding.](https://github.com/pingcap/tidb/pull/4962)
* [Remove the check of initialized auto ID.](https://github.com/pingcap/tidb/pull/4971)
* [Support `alter table add column(...)`.](https://github.com/pingcap/tidb/pull/4963)
* [Fix a bug in JSON decoding.](https://github.com/pingcap/tidb/pull/4949)
* [Use `utf8_bin` for unsupported column collation.](https://github.com/pingcap/tidb/pull/4939)
* [Fix the bug of `alter table table_options, other_alter_specification`.](https://github.com/pingcap/tidb/pull/4931)

## Improved
* [Move the safepoint checker to `tikvStore`.](https://github.com/pingcap/tidb/pull/4998)
* [Enable pushing float down to TiKV.](https://github.com/pingcap/tidb/pull/4967)
* [Fix estimation in index point query.](https://github.com/pingcap/tidb/pull/4956)
* [No longer add enforcer.](https://github.com/pingcap/tidb/pull/4955)
* [Improve index join to support all join types.](https://github.com/pingcap/tidb/pull/4944)
* [Extract the process of getting full CMP type to method.](https://github.com/pingcap/tidb/pull/4935)
* [Opentracing for `Execute`, `ParseSQL`, `Compile`, and `runStmt`.](https://github.com/pingcap/tidb/pull/4929)
* [Reduce `growslice` in `dumpRowValuesBinary`.](https://github.com/pingcap/tidb/pull/4916)

## New Contributor (Thanks!)
* [wudi](https://github.com/foxmailed)


# Weekly update in TiKV

Last week, We landed [16 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-10-30..2017-11-05&type=Issues) in the TiKV repositories.

## Added

* Add [recursion limit check](https://github.com/pingcap/tikv/pull/2432) for coprocessor.
* [Reset the RocksDB statistics](https://github.com/pingcap/tikv/pull/2443) periodically.

## Fixed

* [Save the region meta information to cache](https://github.com/pingcap/pd/pull/825) even if it is failed to be written to the disk.
* Fix the [read statistics](https://github.com/pingcap/tikv/pull/2436).
* [Clear the hot store related gauges](https://github.com/pingcap/pd/pull/833) when store is not hot any more.
* Fix the [LIKE](https://github.com/pingcap/tikv/pull/2442) behavior.

## Improved

* Move [operator influence into `ShouldBalance`](https://github.com/pingcap/pd/pull/822).
* [Reduce allocation](https://github.com/pingcap/tikv/pull/2434).
* [Remove the pending peer](https://github.com/pingcap/pd/pull/826) before adding a new peer.
* Refactor the [split check](https://github.com/pingcap/tikv/pull/2440).
* Add limitation for [key size](https://github.com/pingcap/tikv/pull/2445). 

## New Contributor (Thanks!)
* [wudi](https://github.com/foxmailed)
