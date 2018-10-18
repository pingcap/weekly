---
title: Weekly update (November 06 ~ November 12, 2017)
date: 2017-11-13
summary: Last week, we landed 45 PRs in the TiDB repositories, 5 PRs in the TiSpark repositories, and 18 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV']
---

# Weekly update in TiDB

2017-11-13

Last week, we landed [45 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is:pr%20is:merged%20merged:2017-11-06..2017-11-12) in the TiDB repositories.

## Added
* Support more SQL modes in TiDB:
    - [the `NO_UNSIGNED_SUB` sql_mode](https://github.com/pingcap/tidb/pull/5030)
    - [the `REAL_AS_FLOAT` sql_mode](https://github.com/pingcap/tidb/pull/5029)
    - [the `PIPES_AS_CONCAT` sql_mode](https://github.com/pingcap/tidb/pull/5012)
    - [the `high_not_precedence` sql_mode](https://github.com/pingcap/tidb/pull/5011)
    - [the `ONLY_FULL_GROUP_BY` sql_mode](https://github.com/pingcap/tidb/pull/4613)
* [Parse more privilege types like `RELOAD`, `EVENT` and so on.](https://github.com/pingcap/tidb/pull/5013)
* [Support part of window function AST.](https://github.com/pingcap/tidb/pull/5002)

## Removed
* [Remove `joinBuilder`.](https://github.com/pingcap/tidb/pull/5019)
* [Remove `resolver.go`.](https://github.com/pingcap/tidb/pull/4988)

## Fixed
* [Return error instead of panic if a subquery in `JOIN ON` condition.](https://github.com/pingcap/tidb/pull/5062)
* [Set the error to be `undetermined` error if not recovered from an RPC error.](https://github.com/pingcap/tidb/pull/5043)
* [Fix the issue that DDL is always running and saves the `reorg doneHandle` regularly.](https://github.com/pingcap/tidb/pull/5041)
* [Let the `in` clause handle more cases.](https://github.com/pingcap/tidb/pull/4969)

## Improved
* [Use `types.Row` to write the result set and prepare to use Chunk.](https://github.com/pingcap/tidb/pull/5056/files)
* [Support the `alter table add column(col_name column_definition)` syntax.](https://github.com/pingcap/tidb/pull/5054)
* [Build and use the `Count-Min` sketch.](https://github.com/pingcap/tidb/pull/5042)
* [Stop reusing the Executor in `IndexLookUpJoin` and remove `doRequestForDatums()`.](https://github.com/pingcap/tidb/pull/5031)
* [Begin `OpenTracing` from `dispatch()` and change the interface to `Execute(ctx, sql)` to avoid too many noises.](https://github.com/pingcap/tidb/pull/5027)
* [Remove the read-only statement from transaction auto retry.](https://github.com/pingcap/tidb/pull/5026)
* [Make the batch size of index join increase slowly.](https://github.com/pingcap/tidb/pull/5022)
* [Let `select` push across projects to support generated column index.](https://github.com/pingcap/tidb/pull/5016)
* [Support `insert into from selectStmt that has brackets`.](https://github.com/pingcap/tidb/pull/5008)
* [Remove the type assertion on `types.DatumRow`.](https://github.com/pingcap/tidb/pull/5005)
* [Improve hash join to support all the join types.](https://github.com/pingcap/tidb/pull/4987)
* [Implement the `Count-Min` Sketch.](https://github.com/pingcap/tidb/pull/4970)
* [Enable `OpenTracing` for the `TableReader`, `IndexReader`, `IndexLookup` executor.](https://github.com/pingcap/tidb/pull/4937)

# Weekly update in TiSpark

## Added
* Add [R language support](https://github.com/pingcap/tispark/pull/65).
* Add [Python language support](https://github.com/pingcap/tispark/pull/78).
* Add [Index Read Support and related task concurrent read](https://github.com/pingcap/tispark/pull/53).

## Improved
* Improve [integration tests and frameworks](https://github.com/pingcap/tispark/pull/64).

## Fixed
* Fix [racing condition in thread pool allocation](https://github.com/pingcap/tikv-client-lib-java/pull/135).

# Weekly update in TiKV

Last week, We landed [18 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-11-06..2017-11-12&type=Issues) in the TiKV repositories.

## Added

* Support [splitting table](https://github.com/pingcap/tikv/pull/2378)
* Support [resolving multiple locks in a batch](https://github.com/pingcap/tikv/pull/2389).
* Use [size as a factor of score](https://github.com/pingcap/pd/pull/830) when scheduling.
* Support [`OpenTracing`](https://github.com/pingcap/pd/pull/831) for `pd-client`.
* Support [set namespace for meta](https://github.com/pingcap/pd/pull/834). 
* Support checking the [region stats](https://github.com/pingcap/pd/pull/840) using API.

## Fixed

* [Verify](https://github.com/pingcap/tikv/pull/2450) before destroying a peer.
* Fix [the `LIKE` behavior](https://github.com/pingcap/tikv/pull/2455) for coprocessor.
* Fix [the `do_div_mod`](https://github.com/pingcap/tikv/pull/2456) bug.
* Fix a [nil pointer dereference](https://github.com/pingcap/pd/pull/838) bug in `pd-client`.
* [Clear hot region related gauges](https://github.com/pingcap/pd/pull/843) if a region is not hot any more.

## Improved

* Add [meta decoding](https://github.com/pingcap/pd/pull/827) for tables.
* Better region key [output API](https://github.com/pingcap/pd/pull/836).
* [Unify `ApplyContext` and `ExecContext`](https://github.com/pingcap/tikv/pull/2457).
* Use [`recover_safe!`](https://github.com/pingcap/tikv/pull/2462) to hide the panic stack trace. 
* [Remove the pending peers](https://github.com/pingcap/pd/pull/844) before adding a new peer. 

## New contributers (Thanks!)

* [wudi](https://github.com/foxmailed)
* [xiaojian cai](https://github.com/mccxj)
