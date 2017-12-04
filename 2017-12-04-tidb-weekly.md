---
title: Weekly update (November 27 ~ December 03, 2017)
date: 2017-12-04
summary: Last week, we landed 43 PRs in the TiDB repositories, 6 PRs in the TiSpark repositories, and 17 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [43 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is:pr%20is:merged%20merged:2017-11-27..2017-12-03) in the TiDB repositories.

## Added

* [Add an option to disable `Chunk`.](https://github.com/pingcap/tidb/pull/5268)
* [Add the schema info API of the http status server.](https://github.com/pingcap/tidb/pull/5256)

## Removed

* [Remove the `Align` method of `IndexRange`.](https://github.com/pingcap/tidb/pull/5240)

## Fixed

* [Set the priority for `IndexLookupExecutor` when reading the table.](https://github.com/pingcap/tidb/pull/5288)
* [Fix the length metadata of the decimal column returned to the client.](https://github.com/pingcap/tidb/pull/5249)
* [Fix the bug about auto-increment key after renaming a table from the old DB to another DB.](https://github.com/pingcap/tidb/pull/5248)
* [Fix large `float64` to bigint.](https://github.com/pingcap/tidb/pull/5247)
* [Notify TiDB of updating privileges after `Alter User` and `Drop user`.](https://github.com/pingcap/tidb/pull/5226)

## Improved

* [Refine codes and make `backoffer` the `is-a` go context.](https://github.com/pingcap/tidb/pull/5276)
* [Refactor `NewDomain`.](https://github.com/pingcap/tidb/pull/5270)
* [Speed up loading full stats info.](https://github.com/pingcap/tidb/pull/5266)
* [Speed up loading stats info when the server is started.](https://github.com/pingcap/tidb/pull/5215)
* [Remvove the `hasGby` field.](https://github.com/pingcap/tidb/pull/5265)
* [Limit the `Chunk` size to `MaxChunkSize`.](https://github.com/pingcap/tidb/pull/5252/files)
* [Remove the useless object clone.](https://github.com/pingcap/tidb/pull/5283)
* [Split `Selection` to the logical plan and physical plan.](https://github.com/pingcap/tidb/pull/5235)
* [Move `Range` to the package ranger.](https://github.com/pingcap/tidb/pull/5231)
* [No longer treat DML as a logical/physical plan.](https://github.com/pingcap/tidb/pull/5230)
* Support `Chunk` in: 
    - [`LimitExec`](https://github.com/pingcap/tidb/pull/5200)
    - [`Sort`](https://github.com/pingcap/tidb/pull/5221)
    - [`SelectionExec`](https://github.com/pingcap/tidb/pull/5211)

# Weekly update in TiSpark

Last week, we landed [6 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2017-11-27..2017-12-04) in the TiSpark repositories.

## Added

* [Support the version print for both the client and TiSpark.](https://github.com/pingcap/tispark/pull/104)

## Fixed

* [Fix the inconsistent timezone behavior of Datetime.](https://github.com/pingcap/tispark/pull/99)
* [Fix wrongly folded common aggregation expressions.](https://github.com/pingcap/tispark/pull/97)
* [Fix the inconsistent PD cache eviction and add capture for leaked exception.](https://github.com/pingcap/tikv-client-lib-java/pull/170)

# Weekly update in TiKV

Last week, we landed [17 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-11-27..2017-12-03) in the TiKV and PD repositories.

## Added

* [Implement the count-min sketch in TiKV Coprocessor.](https://github.com/pingcap/tikv/pull/2463)
* [Add the fake TiKV client.](https://github.com/pingcap/pd/pull/864)
* Add TLS support in [TiKV](https://github.com/pingcap/tikv/pull/2506) and [PD](https://github.com/pingcap/pd/pull/868).

## Fixed

* [Fix weird leader distribution after adding a new node and restarting.](https://github.com/pingcap/pd/pull/869)
* [Fix wrong key range generation in tests.](https://github.com/pingcap/tikv/pull/2527)
* [Fix wrong default features.](https://github.com/pingcap/tikv/pull/2544)

## Improved

* [Limit the generation IO of region snapshot.](https://github.com/pingcap/tikv/pull/2446)
* [Update to protobuf 3.](https://github.com/pingcap/pd/pull/859)
* Reduce the slow log in [endpoint](https://github.com/pingcap/tikv/pull/2523) and [scheduler](https://github.com/pingcap/tikv/pull/2525).
* [Use `readyNotify` of etcd.](https://github.com/pingcap/pd/pull/871)
* [Always link to RocksDB statically.](https://github.com/pingcap/tikv/pull/2532)
* [Use the latest rust-prometheus.](https://github.com/pingcap/tikv/pull/2539)
* [Update RocksDB to 5.8.](https://github.com/pingcap/tikv/pull/2543)

# New contributors (Thanks!)

- TiDB: [Johnny Bergström](https://github.com/balboah)
- Docs: [Du Chuan](https://github.com/spongedu)
