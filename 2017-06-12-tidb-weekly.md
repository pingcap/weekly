---
date: 2017-06-12T00:00:00Z
title: Weekly Update
url: /2017/06/12/tidb-weekly/
---

## Weekly update in TiDB

2017-06-12

Last week, we landed [52 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-06-04..2017-06-11) in the TiDB repositories.

## Added

* Refactor the optimizer:
  - [Add an `statsProfile` interface to propagate statistic information among plans.](https://github.com/pingcap/tidb/pull/3370)
  - [Implement the `statsProfile` interface for the `Join` plan.](https://github.com/pingcap/tidb/pull/3403)

* JSON type:
  - [Suport `json_set`, `json_insert`, `json_replace` and `json_merge`.](https://github.com/pingcap/tidb/pull/3388)
  - [Support the JSON type in the `cast` expression.](https://github.com/pingcap/tidb/pull/3395)

* [Use gRPC between TiDB and TiKV.](https://github.com/pingcap/tidb/pull/3390)

* [Refactor the `Analyze` executor.](https://github.com/pingcap/tidb/pull/3410)

* [Add the `SubDuration` function in util package.](https://github.com/pingcap/tidb/pull/3415)

* [Support the `generated column` grammar.](https://github.com/pingcap/tidb/pull/3428)

## Fixed

* [Create a session when the current session with etcd expires.](https://github.com/pingcap/tidb/pull/3371)

* [Fix a bug about padding zeros for binary data.](https://github.com/pingcap/tidb/pull/3379)

* [Fix a bug about type inference.](https://github.com/pingcap/tidb/pull/3386)

* [Fix a but about data access race.](https://github.com/pingcap/tidb/pull/3389)

* [Avoid allocating too much memory in the top-n operator.](https://github.com/pingcap/tidb/pull/3392)

* [Add timeout when getting TimeStamp.](https://github.com/pingcap/tidb/pull/3393)

* [Make the behavior of read-only transactions using the `SelectForUpdate` statement consistent with MySQL.](https://github.com/pingcap/tidb/pull/3402)


## Improved

* Refactor expression evaluation:
  - [Add `builtinAddTimeSig`](https://github.com/pingcap/tidb/pull/3290)
  - [Correct cast function implementation.](https://github.com/pingcap/tidb/pull/3387)
  - [Clean up code and prepare to add test cases.](https://github.com/pingcap/tidb/pull/3398)
  - [Implement wrap expression with the `cast` expression.](https://github.com/pingcap/tidb/pull/3419)

* Speed up DDL process: 
  - [Extract interfaces for `OwnerManger` and `SchemaSyncer`. Add mock implementation for unit test.](https://github.com/pingcap/tidb/pull/3359)
  - [Add TTL for DDL related keys on etcd.](https://github.com/pingcap/tidb/pull/3440)

* [Code style clean up.](https://github.com/pingcap/tidb/pull/3407)

## Weekly update in TiKV


Last week, We landed [25 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-06-04..2017-06-10&type=Issues) in the TiKV repositories.

## Added

* Add the [bloom filter](https://github.com/pingcap/tikv/pull/1887) for Lock CF meltable.
* Introduce gRPC, see [1892](https://github.com/pingcap/tikv/pull/1892), [1894](https://github.com/pingcap/tikv/pull/1894), [1896](https://github.com/pingcap/tikv/pull/1896), [1903](https://github.com/pingcap/tikv/pull/1903)
* Use [SST based bloom filter](https://github.com/pingcap/tikv/pull/1900) by default.
* [Remove the bloom filter](https://github.com/pingcap/tikv/pull/1904) for Raft CF.
* Provide the [GetTSAsync](https://github.com/pingcap/pd/pull/658) API.

## Fixed

* [Delete idle snapshot](https://github.com/pingcap/tikv/pull/1883) only on GC.
* Notify the [blocked goroutines](https://github.com/pingcap/pd/pull/656) when get stream error.
* Fix a bug in [`get_txn_commit_info`](https://github.com/pingcap/tikv/pull/1911) for concurrent `prewrite`.
* [Check the leader](https://github.com/pingcap/pd/pull/659) again when fail to create TSO stream.
* Fix a [data race](https://github.com/pingcap/pd/pull/659) problem in PD client.

## Improved

* Optimize the [Raft log entry](https://github.com/pingcap/tikv/pull/1864) fetching.
* Capture the [SIGHUP](https://github.com/pingcap/tikv/pull/1889) and close gracefully.
* Avoid [allocating lots of memory](https://github.com/pingcap/tikv/pull/1897) in `topn`  function.
* Use [SST snapshot format](https://github.com/pingcap/tikv/pull/1898) by default to speed up Raft snapshot applying.