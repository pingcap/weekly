---
layout: post
title: Weekly Update
---

## Weekly update in TiDB

2017-10-30

Last week, we landed [52 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is:pr%20is:merged%20merged:2017-10-23..2017-10-29) in the TiDB repositories.

## Added

* [Support the window function syntax.](https://github.com/pingcap/tidb/pull/4928)

## Fixed

* [Fix an issue when the `values` builtin function meets the null value.](https://github.com/pingcap/tidb/pull/4923)
* [Support the `signed` field option for the numeric type.](https://github.com/pingcap/tidb/pull/4911)
* [Fix an issue of index reader.](https://github.com/pingcap/tidb/pull/4910)
* [Fix an issue that the binlog client is not initialized correctly.](https://github.com/pingcap/tidb/pull/4887)
* [Correct the schema type of `ShowStmt`.](https://github.com/pingcap/tidb/pull/4886)
* [The default value length for Join should be changed for column pruning.](https://github.com/pingcap/tidb/pull/4882)
* [Add retry for `dialPumpClient`.](https://github.com/pingcap/tidb/pull/4879)
* [Parse but ignore the `REPLICATION CLIENT/SLAVE, USAGE` privileges in the `GRANT` statement.](https://github.com/pingcap/tidb/pull/4870)
* [Fix an issue with visibility check.](https://github.com/pingcap/tidb/pull/4867)
* [Fix an issue with renaming tables.](https://github.com/pingcap/tidb/pull/4862)
* [Parse `PARTITION BY RANGE COLUMNS`.](https://github.com/pingcap/tidb/pull/4852)
* [Support the `straight_join` syntax.](https://github.com/pingcap/tidb/pull/4872)
* [Support the `row_count` built-in function.](https://github.com/pingcap/tidb/pull/4853)
* [Load the column histograms as needed.](https://github.com/pingcap/tidb/pull/4847)
* [Start `safePointChecker` before running a worker.](https://github.com/pingcap/tidb/pull/4845)
* [Truncate the information field for `show processlist` and support `show full processlist`.](https://github.com/pingcap/tidb/pull/4739)

## Improved

* [Build the prepared statement plan in the Optimization phase.](https://github.com/pingcap/tidb/pull/4914)
* [Support the `ALTER TABLE t ENGINE = 'string'` syntax.](https://github.com/pingcap/tidb/pull/4904)
* [Remove `reorgTableDeleteLimit`.](https://github.com/pingcap/tidb/pull/4898/files)
* [Fold the true item in the CNF predicator.](https://github.com/pingcap/tidb/pull/4897)
* [Use max uint64 as the start timestamp for the ANALYZE statement .](https://github.com/pingcap/tidb/pull/4892)
* [Improve merge join to support all join types.](https://github.com/pingcap/tidb/pull/4869)
* [Add highlight to log.](https://github.com/pingcap/tidb/pull/4861)
* [Add the Row interface.](https://github.com/pingcap/tidb/pull/4859)
* [Simple improvement for range calculation for Primary Key.](https://github.com/pingcap/tidb/pull/4767)
* [Change the behavior of the the `in` function.](https://github.com/pingcap/tidb/pull/4813)
* [Support a plan cache for prepared statements.](https://github.com/pingcap/tidb/pull/3956)
* [Introduce Chunk to replace the current datum slice Row.](https://github.com/pingcap/tidb/pull/4856)
* Introducing `OpenTracing` into TiDB:
    - [For two phase commit.](https://github.com/pingcap/tidb/pull/4900)
    - [Tracing config and gRPC interceptor middleware.](https://github.com/pingcap/tidb/pull/4877)


## Weekly update in TiSpark

## Added

* Add [redundant aggregation elimination](https://github.com/pingcap/tispark/pull/45).

## Fixed

* Fix [meta deserialize overflow](https://github.com/pingcap/tispark/pull/59).
* Fix [broken integration test](https://github.com/pingcap/tispark/pull/56/files).
* Fix [potential time type NPE](https://github.com/pingcap/tikv-client-lib-java/pull/125).
* Fix and upgrade [Bazel for CI](https://github.com/pingcap/tikv-client-lib-java/pull/119).
* Fix [test dependency in CI](https://github.com/pingcap/tikv-client-lib-java/pull/118).

## New Contributor
* [Ry](https://github.com/RayeRen)

## Weekly update in TiKV

Last week, We landed [21 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-10-23..2017-10-29&type=Issues) in the TiKV repositories.

## Added

* Add [adjacent region](https://github.com/pingcap/pd/pull/780) balancing scheduler.
* Add [WAL bytes per the sync configuration](https://github.com/pingcap/tikv/pull/2407). 
* Flow control based on [total writing bytes](https://github.com/pingcap/tikv/pull/2408).
* Implement the [`in`](https://github.com/pingcap/tikv/pull/2411) function for coprocessor.
* [Filter the stores with lots of pending peers](https://github.com/pingcap/pd/pull/811) when balancing.
* Add region and hot region [scheduling API](https://github.com/pingcap/pd/pull/812).
* Record the [approximate size of a store](https://github.com/pingcap/pd/pull/814) in PD.

## Fixed

* raftstore: fix an issue with [stale peer check](https://github.com/pingcap/tikv/pull/2409).
* Record snapshot metrics in [`SCHED_STAGE_COUNTER_VEC`](https://github.com/pingcap/tikv/pull/2412).
* Fix the [illegal JSON format](https://github.com/pingcap/pd/pull/821) in the hotspot/stores API.

## Improved

* Inline [`get_limit_at_size`](https://github.com/pingcap/tikv/pull/2401).
* [Group the metrics by namespaces](https://github.com/pingcap/pd/pull/810).
* Document [defer macro](https://github.com/pingcap/tikv/pull/2415) LIFO behavior.
* Remove [redundant verbose KV](https://github.com/pingcap/pd/pull/815) for coordinator.
* Adjust [table ID calculation](https://github.com/pingcap/pd/pull/823).
* Set [stack size to 10 MB](https://github.com/pingcap/tikv/pull/2430) for the coprocessor threads.

## New contributor

* [odeits](https://github.com/odeits)
