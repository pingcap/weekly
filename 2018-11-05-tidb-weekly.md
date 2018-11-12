---
title: Weekly update (October 29 ~ November 04, 2018)
date: 2018-11-05
summary: Last week, we landed 49 PRs in the TiDB repository, 5 PRs in the TiSpark repository, and 5 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [49 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-10-29..2018-11-04+) in the TiDB repository.

## Added

* [Propose the window function design](https://github.com/pingcap/tidb/pull/8117)
* [Introduce a new join reorder framework in the DP-subset algorithm](https://github.com/pingcap/tidb/pull/8025)
* [Add a document about online DDL architecture](https://github.com/pingcap/tidb/pull/7845)


## Improved

* [Try `PointGetPlan` when the plan cache is enabled](https://github.com/pingcap/tidb/pull/8108)
* [Make a query plan containing non-deterministic functions cacheable](https://github.com/pingcap/tidb/pull/8105)
* [Add validation check when setting the `max_allowed_packet` system variable](https://github.com/pingcap/tidb/pull/8090)
* [Use `module` of Go 1.11 for dependency management](https://github.com/pingcap/tidb/pull/8054)
* [Impose check when adding the foreign key](https://github.com/pingcap/tidb/pull/8050)
* [Eliminate `ifnull()` if the argument can never be null](https://github.com/pingcap/tidb/pull/7996)
* [Convert `IN subquery` to `Aggregation` with the inner join](https://github.com/pingcap/tidb/pull/7531)

## Fixed

* [Specially handle `HOUR` in date arithmetic functions](https://github.com/pingcap/tidb/pull/8146)
* [Treat `_tidb_rowid` conditions of index scan as index filters](https://github.com/pingcap/tidb/pull/8143)
* [Avoid using `columnEvaluator` for `Projection` built by `buildProjtion4Union`](https://github.com/pingcap/tidb/pull/8142)
* [Fix selectivity estimation inaccuracy for non-integer primary key](https://github.com/pingcap/tidb/pull/8134)
* [Fix wrong index resolution for `PhysicalIndexReader`](https://github.com/pingcap/tidb/pull/8118)
* [Fix a panic caused by the wrong default value for table `information_schema.profiling`](https://github.com/pingcap/tidb/pull/8092)
* [Fix a panic caused by nil `Backoff.vars`](https://github.com/pingcap/tidb/pull/8089)
* [Fix a panic caused by type mismatch in `SHOW COLUMNS`](https://github.com/pingcap/tidb/pull/8082)
* [Refine `ResolveIndices` for sequential `Projection`s to avoid panics](https://github.com/pingcap/tidb/pull/8073)
* [Fix a panic caused by type mismatch in `UPDATE`](https://github.com/pingcap/tidb/pull/8045)
* [Avoid precision loss when casting JSON to decimal](https://github.com/pingcap/tidb/pull/8030)
* [Reset the statement context before `PREPARE` to avoid panics](https://github.com/pingcap/tidb/pull/7956)
* [Change the privilege component to use `Auth*` portion of identity](https://github.com/pingcap/tidb/pull/7954)

# Weekly update in TiSpark

Last week, we landed [5 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-10-29..2018-11-04+) in the TiSpark repository.

## Added

- [Support cache table commands](https://github.com/pingcap/tispark/pull/467)

# Weekly update in TiKV and PD

Last week, we landed [5 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-10-29..2018-11-04&type=Issues) in the TiKV and PD repositories.

## Added

- [Support the `SubstringIndex` function in Coprocessor](https://github.com/tikv/tikv/pull/3717)

## Improved

- [Make pdctl escape the key before querying the corresponding Region](https://github.com/pingcap/pd/pull/1299)

# New contributors (Thanks!)

tidb:

- [iamzhoug37](https://github.com/iamzhoug37)
- [imiskolee](https://github.com/imiskolee)

docs:

- [ppiao](https://github.com/ppiao)

docs-cn:

- [exialin](https://github.com/exialin)

tidb-operator:

- [anywhy](https://github.com/anywhy)
