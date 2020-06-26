---
title: Weekly update (September 16 ~ September 22, 2019)
date: 2019-09-23
summary: Last week, we landed 58 PRs in the TiDB repository, 7 PRs in the TiSpark repository, and 27 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog post

Jepsen is a project to analyze distributed systems under stress and to understand if concurrency problems are going to manifest, not only in applications but in databases and queues. It occupies a particular niche of the correctness testing landscape.

Last week, we published an article that introduces why Jepsen is important to the distributed database industry, how it works, common issues found, how we use Jepsen with TiDB, and a short summary of all problems Jepsen has found.

The full article is here:

[Safety First! Common Safety Pitfalls in Distributed Databases Found by Jepsen Tests](https://pingcap.com/blog/safety-first-common-safety-pitfalls-in-distributed-databases-found-by-jepsen-tests/)

## Community

### New contributors

tidb:

* [jacklightChen](https://github.com/jacklightChen)
* [doggeral](https://github.com/doggeral)
* [ekalinin](https://github.com/ekalinin)
* [tsthght](https://github.com/tsthght)
* [ZoeShaw101](https://github.com/ZoeShaw101)

rust-prometheus：

* [qmx](https://github.com/qmx)

## Call for participation

TiDB:

* [Vectorize all the built-in functions](https://github.com/pingcap/tidb/issues/12058)
* [Issues to solve](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)

TiKV:

[Issues to solve](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

TiDB:

Last week, we landed [58 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-09-16..2019-09-22+) in the TiDB repository.

TiSpark:

Last week, we landed [7 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-09-16..2019-09-22+) in the TiSpark repository.

TiKV and PD:

Last week, we landed [27 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-09-16..2019-09-22&type=Issues) in the TiKV and PD repositories.

### Critical PRs

TiDB:

* [Do not lock the untouched unique key in the pessimistic mode](https://github.com/pingcap/tidb/pull/12256)
* [Support setting `tidb_enable_stmt_summary` in the session scope](https://github.com/pingcap/tidb/pull/12217)
* [Separate the data preparing routine and the commit routine](https://github.com/pingcap/tidb/pull/11533)
* [Add several SQL hints related to the session variables](https://github.com/pingcap/tidb/pull/11809)
* [Make sure that `IndexReaderExecutor` or `TableReaderExecutor` implements the `Executor` interface](https://github.com/pingcap/tidb/pull/12020)

TiSpark:

* [Add `FieldType` in `DAGRequest`](https://github.com/pingcap/tispark/pull/1101)
* [Support reading data from TiDB in the Spark Structured Streaming](https://github.com/pingcap/tispark/pull/1104)
* [Fix the bug that the TiSpark Catalog has 10s to 20s delay](https://github.com/pingcap/tispark/pull/1108)

TiKV and PD:

* [Enable the backup feature](https://github.com/tikv/tikv/pull/5476)
* [Fix a performance issue about `PointGetter`](https://github.com/tikv/tikv/pull/5469)
* [Support specifying keys to split Regions](https://github.com/tikv/tikv/pull/5458)
* [Handle the read index requests with lease](https://github.com/tikv/tikv/pull/5401)

## Upcoming TiDB events

* [TiDB Hackathon 2019 (in Chinese)](https://github.com/pingcap/presentations/tree/master/hackathon-2019/)
* [Paper Reading 0926 (in Chinese)](https://github.com/pingcap/presentations/blob/master/paper-reading.md)
