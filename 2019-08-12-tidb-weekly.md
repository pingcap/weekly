---
title: Weekly update (August 05 ~ August 11, 2019)
date: 2019-08-12
summary: Last week, we landed 73 PRs in the TiDB repository, 12 PRs in the TiSpark repository, and 42 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [73 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-08-05..2019-08-11+) in the TiDB repository.

## Added

- [Add the methods of vectorized access for `time.Duration` stored in `Column`](https://github.com/pingcap/tidb/pull/11677)
- [Implement `Projection` and `Tabledual` in cascades](https://github.com/pingcap/tidb/pull/11664)
- [Add `opt_rule_blacklist` in MySQL tables](https://github.com/pingcap/tidb/pull/11658)
- [Add the `TIDB_HASHAGG` and `TIDB_STREAMAGG` aggregation hints](https://github.com/pingcap/tidb/pull/11364)

## Improved

- [Use `HistColl` that contains all columns for the estimation of row width](https://github.com/pingcap/tidb/pull/11689)
- [Use `make testSuite` to ensure that all `testSuites`s are enabled](https://github.com/pingcap/tidb/pull/11687)
- [Replace the `context.WithValue` string key with the typed `struct{}` key](https://github.com/pingcap/tidb/pull/11675)
- [Display the tree-like format of the `TRACE` statement](https://github.com/pingcap/tidb/pull/11633)
- [Support the `PointGet` plan when a table has an alias name](https://github.com/pingcap/tidb/pull/11270)

## Fixed

- [Fix the issue that `last_day` is incompatible with MySQL](https://github.com/pingcap/tidb/pull/11704)
- [Fix a bug when comparing a bit with a string](https://github.com/pingcap/tidb/pull/11654)
- [Control the sending rate of `copIteratorTaskSender` if `keepOrder` is `true`](https://github.com/pingcap/tidb/pull/11578)
- [Deduce the result type for the multi-value functions like `IF` that go wrong in some cases](https://github.com/pingcap/tidb/pull/11605)
- [Merge ranges for`BuildColumnRange` when the column has the `length` prefix](https://github.com/pingcap/tidb/pull/11565)
- [Fix the bug that a generated column can refer only to the generated columns defined prior to it](https://github.com/pingcap/tidb/pull/11549)
- [Fix the `date_add` function in `SECOND INTERVAL`](https://github.com/pingcap/tidb/pull/11312)

# Weekly update in TiSpark

Last week, we landed [12 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-08-05..2019-08-11+) in the TiSpark repository.

## Fixed

- [Fix a bug when doing index scan](https://github.com/pingcap/tispark/pull/995)

## Improved

- [Bump the gRPC version to 1.17](https://github.com/pingcap/tispark/pull/982)

# Weekly update in TiKV and PD

Last week, we landed [42 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-08-05..2019-08-11&type=Issues) in the TiKV and PD repositories.

## Added

- [Add `SstWriterBuilder`](https://github.com/tikv/tikv/pull/5211)
- [Add `RealDivide` for the `RPN` function framework](https://github.com/tikv/tikv/pull/5182)

## Improved

- [Change the error type produced by the `Duration` parser](https://github.com/tikv/tikv/pull/5219)
- [Make `codec::Error` more ergonomic](https://github.com/tikv/tikv/pull/5216)
- [Unify the way of using the `tikv_util` crate](https://github.com/tikv/tikv/pull/5214)
- [Move PD to an independent crate](https://github.com/tikv/tikv/pull/5210)
- [Update `rust-rocksdb` to improve the efficiency of Titan GC](https://github.com/tikv/tikv/pull/5196)
- [Deny unknown fields when deserializing the `TOML` configuration](https://github.com/tikv/tikv/pull/5190)
- [Make the PD module more independent](https://github.com/tikv/tikv/pull/5189)
- [Adjust the level of storage logs](https://github.com/tikv/tikv/pull/5184)
- [Upgrade Rust to `nightly-2019-07-19`](https://github.com/tikv/tikv/pull/5137)
- [Refactor the cluster-related logic](https://github.com/pingcap/pd/pull/1654)

## Fixed

- [Use the master branch of the Raft library](https://github.com/tikv/tikv/pull/5228)
- [Fix the unstable `test_auto_gc` integration test](https://github.com/tikv/tikv/pull/5212)
- [Fix the `region size` command](https://github.com/tikv/tikv/pull/5194)
- [Fix the `STORE_ENGINE_SIZE` metrics](https://github.com/tikv/tikv/pull/5187)
- [Handle requests with multiple handle columns correctly](https://github.com/tikv/tikv/pull/5180)
- [Fix the information of lost panic and other logs](https://github.com/tikv/tikv/pull/5174)

# New contributors (Thanks!)

tidb:

- [TennyZhuang](https://github.com/TennyZhuang)
- [lauhg](https://github.com/lauhg)
