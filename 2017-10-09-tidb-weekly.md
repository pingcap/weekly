---
title: Weekly update (September 25 ~ October 8, 2017)
date: 2017-10-09
summary: Last two weeks, we landed 62 PRs in the TiDB repositories and 39 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV', 'TiSpark']
---

# Weekly update in TiDB

Last two weeks, we landed [62 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-09-25..2017-10-08) in the TiDB repositories.

## Added
* [Support the `SyncLog` Key-Value request option.](https://github.com/pingcap/tidb/pull/4689)
* [Support the `NotFillCache` Key-Value request option.](https://github.com/pingcap/tidb/pull/4658)
* [Support the combination SQL modes.](https://github.com/pingcap/tidb/pull/4633)

## Removed
* [Close the aggregation pushdown by default and remove the CBO switch.](https://github.com/pingcap/tidb/pull/4696)
* [Remove some useless code.](https://github.com/pingcap/tidb/pull/4672)
* [Remove the usage of `TypeClass` completely.](https://github.com/pingcap/tidb/pull/4654)

## Fixed
* [Change the `like` function to be case sensitive.](https://github.com/pingcap/tidb/pull/4683)
* [Prepare to enforce errcheck, step 1.](https://github.com/pingcap/tidb/pull/4670)
* [Make the `prepare` statement retry when the schema is out-dated.](https://github.com/pingcap/tidb/pull/4669)
* [Revoke etcd on `ctx.Done` to prevent the situation that no owner entry left.](https://github.com/pingcap/tidb/pull/4624)
* [Pre-calculate the lower and upper scalar.](https://github.com/pingcap/tidb/pull/4623)
* [Add length limitation for index comment.](https://github.com/pingcap/tidb/pull/4619)
* [Make `insert` with calculated value behave the same as MySQL.](https://github.com/pingcap/tidb/pull/4603)
* [Drop invalid cached region.](https://github.com/pingcap/tidb/pull/4506)

## Improved
* [Turn on the `analyze` statement pushdown switch.](https://github.com/pingcap/tidb/pull/4698)
* [Upgrade pd-client to fix a bug.](https://github.com/pingcap/tidb/pull/4694)
* [Rewrite the unit test for `Minus` and `Plus` functions.](https://github.com/pingcap/tidb/pull/4691)
* [The `analyze` statement uses `NewSelectResult`.](https://github.com/pingcap/tidb/pull/4667)
* [Remove the usage of `evalExprToXXX` functions to improve performance.](https://github.com/pingcap/tidb/pull/4666)
* [Change structured slow log to friendly JSON output.](https://github.com/pingcap/tidb/pull/4657)
* [Refactor parser step 2: to be compatible with MySQL syntax.](https://github.com/pingcap/tidb/pull/4652)
* [Refactor the `SelectDAG` function parameter.](https://github.com/pingcap/tidb/pull/4645)
* [Speed up the `add index` operation.](https://github.com/pingcap/tidb/pull/4632)
* [Optimize the `SortExec` executor.](https://github.com/pingcap/tidb/pull/4622)
* [Split separated region for newly created table.](https://github.com/pingcap/tidb/pull/4592)
* [Change the schema validator data structure to queue.](https://github.com/pingcap/tidb/pull/4578)
* [Change the way of transferring the handle.](https://github.com/pingcap/tidb/pull/4348)
* [Support more signatures pushdown.](https://github.com/pingcap/tidb/pull/4495)


# Weekly update in TiSpark

## Added
* Add the [Configuration Framework](https://github.com/pingcap/tikv-client-lib-java/pull/102)

## Fixed
* Fix [invalid leader store ID cases](https://github.com/pingcap/tikv-client-lib-java/pull/113)
* Remove [unused parameter for TiSpark context during the startup](https://github.com/pingcap/tispark/pull/46)

# Weekly update in TiKV

Last two weeks, We landed [39 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-09-25..2017-10-08&type=Issues) in the TiKV repositories.

## Added

* Use [expression](https://github.com/pingcap/tikv/pull/2261) in DAG.
* Namespace isolation: [http interface and classifier](https://github.com/pingcap/pd/pull/747).
* Report [read statistics](https://github.com/pingcap/tikv/pull/2307) to PD.
* Pushdown sampling: implement [histogram](https://github.com/pingcap/tikv/pull/2331).
* Support [`ppc64le`](https://github.com/pingcap/tikv/pull/2334).
* Pushdown the [`analyze` request](https://github.com/pingcap/tikv/pull/2340).
* Support the [`must_sync` flag](https://github.com/pingcap/tikv/pull/2352) for raft ready.
* Introduce [Disconnected and LowSpace states](https://github.com/pingcap/pd/pull/775) for store.
* Add an API to [compact a range](https://github.com/pingcap/tikv/pull/2357) for the specified column family.

## Fixed

* [Stop the thread pool](https://github.com/pingcap/tikv/pull/2311) on shutdown.
* Fix [block send problem](https://github.com/pingcap/pd/pull/768) in grpc.
* Fix potential [unreachable drop](https://github.com/pingcap/tikv/pull/2343).
* Fix [tablecodec](https://github.com/pingcap/pd/pull/773).

## Improved

* Select response of DAG [don’t need row meta](https://github.com/pingcap/tikv/pull/2302).
* Add [drop message metrics](https://github.com/pingcap/tikv/pull/2316).
* Debug: [implement size](https://github.com/pingcap/tikv/pull/2329).
* Debug: [implement region information](https://github.com/pingcap/tikv/pull/2332).
* Add [slow log](https://github.com/pingcap/tikv/pull/2333) for applying.
* Update [gRPC to 1.6.1](https://github.com/pingcap/tikv/pull/2336).
* Check whether peers need to [split after initialization](https://github.com/pingcap/tikv/pull/2339).
* [Refactor Key-Value](https://github.com/pingcap/pd/pull/771) for PD.
* Config: change all the names to kebab-case](https://github.com/pingcap/pd/pull/772).
* [Flush the leader message](https://github.com/pingcap/tikv/pull/2345) as soon as possible.
* Return [error instead of panic](https://github.com/pingcap/tikv/pull/2347) if an expression is illegal.
* Update [etcd to v3.2.6](https://github.com/pingcap/pd/pull/774) for PD.
* [Synchronize data](https://github.com/pingcap/tikv/pull/2353) before applying snapshots.
* [Update the client URLs](https://github.com/pingcap/pd/pull/777) continuously. 
* Adjust the [region heartbeat metrics](https://github.com/pingcap/pd/pull/779).

## New contributors
* [Priya Seth](https://github.com/seth-priya)
