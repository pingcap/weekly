---
title: Weekly update (January 01 ~ January 07, 2018)
date: 2018-01-08
summary: Last week, we landed 37 PRs in the TiDB repositories, 4 PRs in the TiSpark repositories, and 10 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [37 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is:pr+is:merged+merged:2018-01-01..2018-01-07) in the TiDB repositories.

## Added

* [Support the `PACK_KEYS` option in the `CreateTable` statement.](https://github.com/pingcap/tidb/pull/5554)
* [Show job's start time in the result of `admin show ddl ...`.](https://github.com/pingcap/tidb/pull/5517)

## Fixed

* [Fix a bug when initializing HTTP stats handler.](https://github.com/pingcap/tidb/pull/5555)
* [Fix a bug when estimating row count for outdated histograms.](https://github.com/pingcap/tidb/pull/5552)
* [Consider time zone for builtin functions `curtime/sysdate/curdate`.](https://github.com/pingcap/tidb/pull/5548)

## Improved

* [Refactor `Chunk.AppendRow` to handle virtual.](https://github.com/pingcap/tidb/pull/5563)
* [Refactor hybrid type expressions.](https://github.com/pingcap/tidb/pull/5550)
* [Only do a shallow copy when evaluating a "Column" expression.](https://github.com/pingcap/tidb/pull/5542)
* [Refine the design of schema.](https://github.com/pingcap/tidb/pull/5541)
* [Use more compact structure for histograms.](https://github.com/pingcap/tidb/pull/5539)
* [Convert the aggregation operator `max/min` to `topN`.](https://github.com/pingcap/tidb/pull/5516)
* [Shard the implicit row ID to avoid hot spot.](https://github.com/pingcap/tidb/pull/5513)
* [Support `Chunk` for `StreamAggExec`.](https://github.com/pingcap/tidb/pull/5490)
* [Support `Chunk` for `HashAggExec`.](https://github.com/pingcap/tidb/pull/5244)

# Weekly update in TiSpark

Last week, we landed [4 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-01-01..2018-01-07) in the TiSpark repositories.

## Improved

* [Add potential missing test cases.](https://github.com/pingcap/tispark/pull/199)
* [Simplify `Aggregation` pushdown.](https://github.com/pingcap/tispark/pull/153)

## Fixed

* [Fix the dependency for `jackson` and `joda-time`.](https://github.com/pingcap/tispark/pull/195)
* [Fix the error handling logic.](https://github.com/pingcap/tispark/pull/191)

# Weekly update in TiKV and PD

Last week, we landed [10 PRs](https://github.com/search?q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-01-01..2018-01-07) in the TiKV and PD repositories.

## Added

* [Add timer to support worker timeout later.](https://github.com/pingcap/tikv/pull/2564)
* [tikv-ctl: add `bad-regions` subcommand.](https://github.com/pingcap/tikv/pull/2624)
* [coprocessor/endpoint: initialize runtime in response.](https://github.com/pingcap/tikv/pull/2638)

## Fixed

* [tests: fix some failpoints name.](https://github.com/pingcap/tikv/pull/2634)
* [scheduler: fix hot region scheduler select store problem.](https://github.com/pingcap/pd/pull/898)
* [Fix the score when region size is zero.](https://github.com/pingcap/pd/pull/899)

## Improved

* [raftstore: add `Lease`.](https://github.com/pingcap/tikv/pull/2582)
* [util: remove `BatchRunnable` and use `Runnable` instead.](https://github.com/pingcap/tikv/pull/2645)
* [tests: remove redundant storage tests.](https://github.com/pingcap/tikv/pull/2646)
* [Change `github.com/Sirupsen/logrus` to `github.com/sirupsen/logrus`.](https://github.com/pingcap/pd/pull/902)

# New contributor (Thanks!)

* TiDB: [Cruth kvinc](https://github.com/oiooj)