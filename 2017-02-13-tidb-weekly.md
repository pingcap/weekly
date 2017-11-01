---
title: Weekly update (February 6 ~ February 12, 2016)
date: 2017-02-13
summary: Last two weeks, we landed 25 PRs in the TiDB repositories and 14 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV']
---

# Weekly update in TiDB

Last two weeks, we landed [25 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-02-06..2017-02-12%20) in the TiDB repositories.

## Added

* Support basic privilege framework: [#2423](https://github.com/pingcap/tidb/pull/2423), [#2557](https://github.com/pingcap/tidb/pull/2557), [#2603](https://github.com/pingcap/tidb/pull/2603), [#2607](https://github.com/pingcap/tidb/pull/2607),

* [Support `ALTER [COLUMN] col_name SET DEFAULT` statement.](https://github.com/pingcap/tidb/pull/2608)

* [Validate column default value when creating table.](https://github.com/pingcap/tidb/pull/2614)

* [Support `ALTER TABLE ... DROP DEFAULT` statement.](https://github.com/pingcap/tidb/pull/2616)

* [Support changing default value and comment in alter table statement.](https://github.com/pingcap/tidb/pull/2621)

## Fixed

* [Fix build on i386.](https://github.com/pingcap/tidb/pull/2591)

* [Fix output format of prometheus interval log.](https://github.com/pingcap/tidb/pull/2594)

* Clean up log: [#2599](https://github.com/pingcap/tidb/pull/2599), [#2601](https://github.com/pingcap/tidb/pull/2601)

* [Fix a bug in HashJoin executor](https://github.com/pingcap/tidb/pull/2605): some errors are ignored.

* [Fix a bug in arithmetic expression type inference.](https://github.com/pingcap/tidb/pull/2610)

* [Fix a bug in builtin function timediff.](https://github.com/pingcap/tidb/pull/2611)


## Improved

* [Speed up unit tests.](https://github.com/pingcap/tidb/pull/2590)

* Make test cases more stable: [#2595](https://github.com/pingcap/tidb/pull/2595), [#2596](https://github.com/pingcap/tidb/pull/2596)

* [Remove useless code in parser package.](https://github.com/pingcap/tidb/pull/2604)

* [Change string default collation to utf8_bin.](https://github.com/pingcap/tidb/pull/2617) We do not support case insensitive comparation yet.

# Weekly update in TiKV

Last week, We landed [14 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-02-05..2017-02-11&type=Issues&ref=searchresults) in the TiKV repositories.

## Added

* Use [`seek_for_prev`](https://github.com/pingcap/tikv/pull/1581) directly.

* Refactor [`cut_row` and `cut_idx_key`](https://github.com/pingcap/tikv/pull/1590) for row value analysis in coprocessor.

* Extract an [interface](https://github.com/pingcap/tikv/pull/1579) to support different snapshot format.

## Fixed

* Fix panic when [stop scheduler](https://github.com/pingcap/tikv/pull/1580) worker.

* Fix [invalid link](https://github.com/pingcap/pd/pull/500) in PD readme.

## Improved

* Evaluate [logic operations](https://github.com/pingcap/tikv/pull/1565) lazily.

* Use [prefix seek](https://github.com/pingcap/tikv/pull/1509) to speed up read for Write CF.

* Separate [`advance` to `advance_ready` and `advance_apply`](https://github.com/pingcap/tikv/pull/1573) for async-apply later.

* Use [`shutdown`](https://github.com/pingcap/tikv/pull/1586)  to do cleanup when stop worker.
