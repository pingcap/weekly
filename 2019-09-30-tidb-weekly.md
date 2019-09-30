---
title: Weekly update (September 23 ~ September 29, 2019)
date: 2019-09-30
summary: Last week, we landed 126 PRs in the TiDB repository, 15 PRs in the TiSpark repository, and 54 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## Community

### New contributors

tidb:

- [tangwz](https://github.com/tangwz)
- [polyrabbit](https://github.com/polyrabbit)
- [k-ye](https://github.com/k-ye)
- [PiotrNewt](https://github.com/PiotrNewt)
- [hellojujian](https://github.com/hellojujian)
- [shihongzhi](https://github.com/shihongzhi)
- [luyunyyyyy](https://github.com/luyunyyyyy)
- [Handora](https://github.com/Handora)

tikv:

- [wshwsh12](https://github.com/wshwsh12)

raft-rs:

- [psinghal20](https://github.com/psinghal20)

## Call for participation

TiDB:

- [Issues to solve](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)

TiKV:

- [Issues to solve](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

TiDB:

Last week, we landed [126 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-09-23..2019-09-29+) in the TiDB repository.

TiSpark:

Last week, we landed [15 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-09-23..2019-09-29+) in the TiSpark repository.

TiKV and PD:

Last week, we landed [54 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-09-23..2019-09-29&type=Issues) in the TiKV and PD repositories.

### Critical PRs

TiDB:

- [Fix the error occurred when converting the subqueries contained in the `UPDATE` statement](https://github.com/pingcap/tidb/pull/12476)
- [Fix the `ttlManager` race](https://github.com/pingcap/tidb/pull/12398)
- [Fix the wrong `Flen` when processing `Decimal` and `Int`](https://github.com/pingcap/tidb/pull/12312)
- [Update the `kvrpc.Cleanup` protocol and change its behavior](https://github.com/pingcap/tidb/pull/12212)
- [Implement the disk-based hash join](https://github.com/pingcap/tidb/pull/12067)
- [Enable Region requests to be sent to TiFlash stores](https://github.com/pingcap/tidb/pull/11652)

TiSpark:

- [Fix the `fastxml` security alert](https://github.com/pingcap/tispark/pull/1127)

TiKV and PD:

- [Fix the issue that the commit index is not forwarded when the merge entry is empty](https://github.com/tikv/tikv/pull/5512)
- [Support the memory quota](https://github.com/tikv/tikv/pull/5524)
- [Enable RocksDB `force_consistency_checks` for all CFs](https://github.com/tikv/tikv/pull/5491)
- [Check lock's TTL when doing cleanup](https://github.com/tikv/tikv/pull/5471)
- [Fix the panic caused by `GetLeader`](https://github.com/pingcap/pd/pull/1766)
- [Return the chunk-encoded data when the requested `EncodeType` is `TypeArrow`](https://github.com/tikv/tikv/pull/5461)
- [Replace the pending peers instead of removing them directly](https://github.com/pingcap/pd/pull/1607)
