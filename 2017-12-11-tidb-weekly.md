---
title: Weekly update (December 04 ~ December 10, 2017)
date: 2017-12-11
summary: Last week, we landed 45 PRs in the TiDB repositories, 12 PRs in the TiSpark repositories, and 21 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [45 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is:pr%20is:merged%20merged:2017-12-04..2017-12-11) in the TiDB repositories.

## Added

* [Add hints to force to choose `HashJoin`.](https://github.com/pingcap/tidb/pull/5315)
* [Provide the HTTP API of table disk usage for tidb-ctl.](https://github.com/pingcap/tidb/pull/5309)

## Fixed

* [Fix a bug when updating the `JSON` field.](https://github.com/pingcap/tidb/pull/5345)
* [Delete the auto ID key when renaming the table.](https://github.com/pingcap/tidb/pull/5333)
* [Fix a bug in `JoinResultGenerator`.](https://github.com/pingcap/tidb/pull/5332)
* [Fix a bug when backfilling the index with nil.](https://github.com/pingcap/tidb/pull/5319)
* [The value of a session variable should not be modified when getting a global variable.](https://github.com/pingcap/tidb/pull/5317)

## Improved

* [Move the `Cancel` function from session to clientConn.](https://github.com/pingcap/tidb/pull/5346)
* [Reduce a comparison in the union scan.](https://github.com/pingcap/tidb/pull/5336/files)
* [Move the binary-tree library from petar/GoLLRB to google/btree.](https://github.com/pingcap/tidb/pull/5335)
* [Add the `Format` interface on `ExprNode` to convert AST back to string.](https://github.com/pingcap/tidb/pull/5299)
* [Improve the performance of `ShowVariables`.](https://github.com/pingcap/tidb/pull/5297)
* [Add `Chunk`/`List` to hold a slice of `Chunk`.](https://github.com/pingcap/tidb/pull/5290)
* [Add the explain info for `TopN`.](https://github.com/pingcap/tidb/pull/5287)
* [Support coprocessor streaming API for the TiKV client.](https://github.com/pingcap/tidb/pull/5254)
* [Support sql_mode `IGNORE SPACE`.](https://github.com/pingcap/tidb/pull/5106)
* [Support the builtin aggregation function `bit_xor`.](https://github.com/pingcap/tidb/pull/5090)
* Refactor SQL query optimizer:
    - [Replace `Sort` with `LogicalSort` and `PhysicalSort`.](https://github.com/pingcap/tidb/pull/5298)
    - [Add `Physical` operator for `Lock`, `Limit` and `UnionAll`.](https://github.com/pingcap/tidb/pull/5301)
    - [Make `Show` no longer a logical/physical plan.](https://github.com/pingcap/tidb/pull/5321)
    - [Add `Physical` plan for `MaxOneRow`, `Dual` and `Exists`.](https://github.com/pingcap/tidb/pull/5324)
    - [Add `Physical` plan for `Projection` and `TopN`.](https://github.com/pingcap/tidb/pull/5316)
    - [Extract `getChildrenPossibleProp` to a file.](https://github.com/pingcap/tidb/pull/5286)
    - [Add `PhysicalStreamAgg` and remove `AggType`.](https://github.com/pingcap/tidb/pull/5274)
* Support `Chunk` in executors: 
    - [`InsertExec`](https://github.com/pingcap/tidb/pull/5352)
    - [`MaxOneRowExec`](https://github.com/pingcap/tidb/pull/5281)
    - [`TopN`](https://github.com/pingcap/tidb/pull/5260)
    - [`UnionExec`](https://github.com/pingcap/tidb/pull/5229)

# Weekly update in TiSpark

Last week, we landed [12 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2017-12-04..2017-12-10) in the TiSpark repositories.

## Added

* [Implement the Coprocessor DAG mode reading.](https://github.com/pingcap/tispark/pull/105)
* [Implement `TopN` pushdown.](https://github.com/pingcap/tispark/pull/110)
* [Add the switch for disabling a specific expression pushdown for old versions of TiKV.](https://github.com/pingcap/tispark/pull/117)
* [Add the Cache invalidation notification for the client.](https://github.com/pingcap/tikv-client-lib-java/pull/185)

## Fixed

* [Fix the reading error when all values in group aggregate to null.](https://github.com/pingcap/tikv-client-lib-java/pull/183)
* [Fix a potential error escape from Handler.](https://github.com/pingcap/tikv-client-lib-java/pull/182)
* [Fix inconsistent PD cache eviction and add capture for leaked exception.](https://github.com/pingcap/tikv-client-lib-java/pull/170)
* [Fix the pushdown type problem of timestamp.](https://github.com/pingcap/tikv-client-lib-java/pull/181)

# Weekly update in TiKV and PD

Last week, we landed [21 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-12-04..2017-12-10) in the TiKV and PD repositories.

## Added

* [Add `TiltCase` and `Main`.](https://github.com/pingcap/pd/pull/842)
* [Support `lower_bound` for iterator.](https://github.com/pingcap/tikv/pull/2504)
* [Add `on_tick` for `BatchRunnable`.](https://github.com/pingcap/tikv/pull/2524)
* [Support getting the unique index.](https://github.com/pingcap/tikv/pull/2526)
* [Add `role_observer` in the coprocessor.](https://github.com/pingcap/tikv/pull/2551)
* [Record the wait time of `APPLY_TASK`.](https://github.com/pingcap/tikv/pull/2552)
* [Support disabling the block cache for test.](https://github.com/pingcap/tikv/pull/2554)
* [Support setting `bytes_per_sync` and `wal_bytes_per_sync`.](https://github.com/pingcap/tikv/pull/2555)

## Fixed

* [Use the same configuration for tikv-ctl and tikv-server.](https://github.com/pingcap/tikv/pull/2538)
* [Fix zero truncation in decimal decoding.](https://github.com/pingcap/tikv/pull/2547)
* [Call the `post_apply` hook.](https://github.com/pingcap/tikv/pull/2561)
* [Support the TLS connection in pd-recover.](https://github.com/pingcap/pd/pull/877)

## Improved

* [Improve scheduler metrics.](https://github.com/pingcap/tikv/pull/2522)
* [Avoid cloning `prs` in Raft.](https://github.com/pingcap/tikv/pull/2546)
* [Update `Limiter` using all pending operators.](https://github.com/pingcap/pd/pull/874)
* [Use a bit field to present the operator kind.](https://github.com/pingcap/pd/pull/875)
* [Update RocksDB with optimized ingesting SST.](https://github.com/pingcap/tikv/pull/2549)
* [Reduce the log in the MVCC layer.](https://github.com/pingcap/tikv/pull/2550)
* [Refactor tests for the RPC client.](https://github.com/pingcap/tikv/pull/2558)
* [Optimize the dev build and fix typo.](https://github.com/pingcap/tikv/pull/2566)

# New contributors (Thanks!)

+ TiDB: 
    - [Evgeniy Kulikov](https://github.com/im-kulikov)
    - [denofiend](https://github.com/denofiend)
+ docs-cn:
    - [Guangkuo Bian](https://github.com/limitless083)
