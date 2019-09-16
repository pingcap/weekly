---
title: Weekly update (September 09 ~ September 15, 2019)
date: 2019-09-16
summary: Last week, we landed 92 PRs in the TiDB repository and 39 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## Community

### New contributors

tidb:

* [hey-kong](https://github.com/hey-kong)
* [lizhenda](https://github.com/lizhenda)

raft-rs:

* [MaiCw4J](https://github.com/MaiCw4J)

raft-prometheus:

* [ekse](https://github.com/ekse)

## Call for participation

TiDB:

* [Vectorize all the built-in functions](https://github.com/pingcap/tidb/issues/12058)
* [Issues to solve](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)

TiKV:

* [Check code for common misspellings](https://github.com/tikv/tikv/issues/5456)
* [Issues to solve](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

TiDB:

Last week, we landed [92 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-09-09..2019-09-15+) in the TiDB repository.

* Release TiDB [v2.1.17](https://pingcap.com/docs/v3.0/releases/2.1.17/)
* Support generating hints from physical plans
* Introduce the cascades adapter model and implement the `handle range` scan

TiKV and PD:

Last week, we landed [39 PRs](https://github.com/search?p=3&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-09-09..2019-09-15&type=Issues) in the TiKV and PD repositories.

* Release TiKV and PD [v2.1.17](https://pingcap.com/docs/v3.0/releases/2.1.17/)
* Enable `DoublySkiplist` by default

### Critical PRs

TiDB:

* [Support generating hints from physical plans](https://github.com/pingcap/tidb/pull/11936)
* [Implement the `CheckTxnStatus` API for the large transaction](https://github.com/pingcap/tidb/pull/11974)
* [Introduce the cascades adapter model and implement the `handle range` scan](https://github.com/pingcap/tidb/pull/11566)
* [Improve the row count estimation of `IndexJoin`'s inner scan](https://github.com/pingcap/tidb/pull/12085)
* [Support the `unix_timestamp()` function in partition pruning](https://github.com/pingcap/tidb/pull/12035)
* [Fix the issue that `MaxUint64` and `MaxInt64 autoID` are incorrectly allocated](https://github.com/pingcap/tidb/pull/12119)
* [Fix the invalid snapshot cache under the pessimistic transaction](https://github.com/pingcap/tidb/pull/12147)

TiKV and PD:

* [Enable `DoublySkiplist` by default](https://github.com/tikv/tikv/pull/5430)
* [Introduce `PointGetter`](https://github.com/tikv/tikv/pull/5424)
* [Support backup with the rate limit](https://github.com/tikv/tikv/pull/5451)
* [Fix the calculation of Region flow](https://github.com/pingcap/pd/pull/1688)
* [Fix the TiKV panic when the `aggregation expr` type is invalid](https://github.com/tikv/tikv/pull/5429)

## Upcoming TiDB events

* [TiDB Hackathon 2019 (in Chinese)](https://pingcap.com/community-cn/hackathon2019/)
* [Paper Reading 0918 (in Chinese)](https://github.com/pingcap/presentations/blob/master/paper-reading.md)
