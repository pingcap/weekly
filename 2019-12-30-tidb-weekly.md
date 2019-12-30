---
title: Weekly update (December 23 ~ December 29, 2019)
date: 2019-12-30
summary: Last week, we landed 70 PRs in the TiDB repository, 7 PRs in the TiSpark repository, and 46 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog post

The fast advancement of AI and machine learning (ML) technologies are reshaping the way people manage and tune databases. Inspired by the pioneering breakthroughs of automatic tuning, we developed AutoTiKV, a machine-learning-based tuning tool that automatically recommends optimal knobs for TiKV. So far, our exploration of automatic tuning has been rewarding.

Last week, we published a post that discusses AutoTiKV's design, its machine learning model, and the automatic tuning workflow. The post also shares the results of experiments we ran to verify whether the tuning results are optimal and as expected, with some interesting and unexpected findings.

The full post is here:

[AutoTiKV: TiKV Tuning Made Easy by Machine Learning](https://pingcap.com/blog/autotikv-tikv-tuning-made-easy-by-machine-learning/)

## Community

### New contributors

tidb:

* [waynexia](https://github.com/waynexia)
* [Icemap](https://github.com/Icemap)

tikv:

* [fky2015](https://github.com/fky2015)

docs-cn:

* [20100507](https://github.com/20100507)

parser:

* [githubFZX](https://github.com/githubFZX)

## Call for participation

* Coprocessor SIG:
    * [Improve the performance of Chunk Encoder](https://github.com/tikv/tikv/issues/5729)
    * [Port `BinaryJSON`](https://github.com/tikv/tikv/issues/5715)
    * [Tracing](https://github.com/tikv/tikv/issues/5714)
    * [The maximum execution time of Per-request](https://github.com/tikv/tikv/issues/5712)

* [More issues to solve for TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)
* [More issues to solve for TiKV](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

Last week, we landed [70 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-12-23..2019-12-29+) in the TiDB repository, [7 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-12-23..2019-12-29+) in the TiSpark repository, and [46 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-12-23..2019-12-29&type=Issues) in the TiKV and PD repositories.

### Critical PRs

TiDB:

* [Support the `show extended columns` statement](https://github.com/pingcap/tidb/pull/14262)
* [Add the rollback in `releaseSysSession`](https://github.com/pingcap/tidb/pull/14269)
* [Add the `ClusterEventsStatementsSummary` table](https://github.com/pingcap/tidb/pull/14259)
* [Add the `PushTopNDownTiKVSingleGather` transformation rule in the cascades planner](https://github.com/pingcap/tidb/pull/14242)
* [Fix the row count estimation for the unique composite `IndexScan` of `IndexJoin`](https://github.com/pingcap/tidb/pull/14167)
* [Support the read consistency isolation level in the pessimistic transactions](https://github.com/pingcap/tidb/pull/14087)
* [Support the certificate-based authentication](https://github.com/pingcap/tidb/pull/13955)

TiSpark:

* [Remove the unexpected Spark version output in release 2.1](https://github.com/pingcap/tispark/pull/1331)
* [Fix the issue that the prefix index might be incorrect when the charset is not `UTF8`](https://github.com/pingcap/tispark/pull/1333)

TiKV and PD:

* [Upgrade etcd to v3.4.3](https://github.com/pingcap/pd/pull/2058)
* [Use `Commit` to clean up the pessimistic locks](https://github.com/tikv/tikv/pull/6353)
* [Support `split check` in the online change configuration](https://github.com/tikv/tikv/pull/6294)
* [Support the lock manager in the online change configuration](https://github.com/tikv/tikv/pull/6338)
* [Fix the error handling about the RocksDB iterator](https://github.com/tikv/tikv/pull/6325)
* [Support deleting the store label by setting it to `empty`](https://github.com/pingcap/pd/pull/2044)
* [Skip the notification for synchronous `destroy`](https://github.com/tikv/tikv/pull/6299)
* [Add `ApplySnapshotObserver`](https://github.com/tikv/tikv/pull/6015)
* [Add the `keyvisual` service](https://github.com/pingcap/pd/pull/1948)
