---
title: Weekly update (April 29 ~ May 05, 2019)
date: 2019-05-06
summary: Last week, we landed 41 PRs in the TiDB repository, 4 PRs in the TiSpark repository, and 21 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [41 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-04-29..2019-05-05+) in the TiDB repository.

## Added

- [Make the `Performance.*`, `OOMAction` and `MemQuotaQuery` config items support hot-reloading](https://github.com/pingcap/tidb/pull/10295)
- [Make SQL bind work when executing `select` and `explain select` statements](https://github.com/pingcap/tidb/pull/10284)
- [Add the memory table to show Region information](https://github.com/pingcap/tidb/pull/10267)
- [Support CMSketch with TopN](https://github.com/pingcap/tidb/pull/10255)

## Improved

- [Change the offset type of `chunk` to int64](https://github.com/pingcap/tidb/pull/10348)
- [Make `tidb_disable_txn_auto_retry` disable retry for explicit transactions](https://github.com/pingcap/tidb/pull/10339)
- [Refine `point get` failpoint](https://github.com/pingcap/tidb/pull/10319)
- [Check time zone when encoding timestamp datum](https://github.com/pingcap/tidb/pull/10303)
- [Check whether the TiKV instance is stopped when recreating connection to it](https://github.com/pingcap/tidb/pull/10301)
- [Add transaction commit time to slow log](https://github.com/pingcap/tidb/pull/10294)
- [Ignore the overflow error when constructing inner keys](https://github.com/pingcap/tidb/pull/10244)
- [Support pre-splitting Region for the partitioned table](https://github.com/pingcap/tidb/pull/10221)
- [Enhance `Index Join`](https://github.com/pingcap/tidb/pull/8471)

## Fixed

- [Fix the issue that TiDB handles leap year incorrectly in some cases](https://github.com/pingcap/tidb/pull/10342)
- [Fix incorrect `Internal` display in the `admin show slow` output](https://github.com/pingcap/tidb/pull/10338)
- [Fix data race of parser in the global handle](https://github.com/pingcap/tidb/pull/10321)
- [Fix the issue that `timestampadd` is not compatible with MySQL](https://github.com/pingcap/tidb/pull/10314)
- [Fix wrong judgment conditions when judging `point get`](https://github.com/pingcap/tidb/pull/10304)
- [Fix the issue that `JSON_CONTAINS` is not compatible with MySQL](https://github.com/pingcap/tidb/pull/10298)
- [Fix the wrong privilege check for `update` in some cases](https://github.com/pingcap/tidb/pull/10281)
- [Fix the wrong error message when granting to a non-existent user](https://github.com/pingcap/tidb/pull/10239)

# Weekly update in TiSpark

Last week, we landed [4 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-04-29..2019-05-05+) in the TiSpark repository.

## Fixed

- [Fix the issue that `tempView` might be unresolved when applying a timestamp to the plan](https://github.com/pingcap/tispark/pull/690)
- [Fix the issue that Catalog is not closed when Session closes](https://github.com/pingcap/tispark/pull/693)

# Weekly update in TiKV and PD

Last week, we landed [21 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-04-29..2019-05-05&type=Issues) in the TiKV and PD repositories.

## Added

* [Share block cache among column families](https://github.com/tikv/tikv/pull/4563)
* [Add the `AVG` batch aggregate function](https://github.com/tikv/tikv/pull/4570)
* [Add the `LogicalAnd` RPN function](https://github.com/tikv/tikv/pull/4575)
* [Enable using Region storage by default in PD config](https://github.com/pingcap/pd/pull/1524)
* [Add the `LogicalOr` RPN function](https://github.com/tikv/tikv/pull/4601)
* [Add the `LTReal`, `LEReal`, `GTReal`, `GEReal`, `NEReal`, `EQReal` RPN functions](https://github.com/tikv/tikv/pull/4602)
* [Add more fuzz tests](https://github.com/tikv/tikv/pull/4608)
* [Add an execution summary framework for non-batch executors](https://github.com/tikv/tikv/pull/4621) 

## Improved

* [Simplify the usage of RpnExpressionBuilder](https://github.com/tikv/tikv/pull/4573)
* [Enhance the error report for fuzzing](https://github.com/tikv/tikv/pull/4593)
* [Rename and move `ExecSummary` to support non-batch executors](https://github.com/tikv/tikv/pull/4596)
* [Simplify the exec summary](https://github.com/tikv/tikv/pull/4597)
* [Support the exec summary for normal table/index scan executor](https://github.com/tikv/tikv/pull/4598)
* [Tune `SstFileWriter` options to reduce CPU usage in Importer](https://github.com/tikv/tikv/pull/4611)

## Fixed

* [Register mailbox before sending in tests](https://github.com/tikv/tikv/pull/4577)
* [Fix read pool names](https://github.com/tikv/tikv/pull/4588)
* [Update Raft to 0.4.2](https://github.com/tikv/tikv/pull/4604)

# New contributors (Thanks!)

tidb:

- [gunjanpatidar](https://github.com/gunjanpatidar)
- [ian-p-cooke](https://github.com/ian-p-cooke)
- [mantuliu](https://github.com/mantuliu)

tikv:

- [yeshengm](https://github.com/yeshengm)

tidb-operator:

- [jlerche](https://github.com/jlerche)
