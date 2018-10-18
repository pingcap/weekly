---
title: Weekly update (September 19 ~ September 25, 2016)
date: 2016-09-26
summary: Last week, we landed 20 PRs in the TiDB repositories and 24 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV', 'Placement Driver']
---

# Weekly update (September 19 ~ September 25, 2016)

Last week, we landed [20 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-09-19..2016-09-25%20) in the TiDB repositories and [24 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2016-09-19..2016-09-25&type=Issues&ref=searchresults) in the TiKV repositories.

## Notable changes to `TiDB`

+ Support [DML binlog](https://github.com/pingcap/tidb/pull/1660).
+ Support [reading the history data](https://github.com/pingcap/tidb/pull/1734).
+ Add more metrics to [distsql](https://github.com/pingcap/tidb/pull/1737), [DDL](https://github.com/pingcap/tidb/pull/1738), and [store](https://github.com/pingcap/tidb/pull/1741).
+ [Replace the vendor tool with glide](https://github.com/pingcap/tidb/pull/1743).
+ [Improve test coverage](https://github.com/pingcap/tidb/pull/1723).
+ [Code cleanup](https://github.com/pingcap/tidb/pull/1745).
+ Improve the test code by [splitting a big test file into smaller files](https://github.com/pingcap/tidb/pull/1757).

## Notable changes to `TiKV`

+ Port the [`read index`](https://github.com/pingcap/tikv/pull/1032) feature from etcd.
+ Add the [upper bound mod](https://github.com/pingcap/tikv/pull/1060) support to the iterator to improve the `seek` performance.
+ Support the [recovery mode](https://github.com/pingcap/tikv/pull/1069) for RocksDB.
+ Support [adding/removing column families](https://github.com/pingcap/tikv/pull/1098) dynamically.


## Notable changes to `Placement Driver (PD)`

+ Remove the [`watch` leader](https://github.com/pingcap/pd/pull/327) mechanism for the clients becausse the PD server can proxy requests to the leader.
+ Add the [`GetRegionByID`](https://github.com/pingcap/pd/pull/329) command.
