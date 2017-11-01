---
title: Weekly update (November 07 ~ November 13, 2016)
date: 2016-11-14
summary: Last week, we landed 25 PRs in the TiDB repositories, 5 PRs in the TiDB docs repositories，and 23 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV']
---

Last week, we landed [25 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-11-07..2016-11-13) in the TiDB repositories and [5 PRs]([https://github.com/pingcap/docs/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-11-07..2016-11-13](https://github.com/pingcap/docs/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-11-07..2016-11-13)) in the TiDB docs repositories.

# Weekly update in TiDB

## Added

+ [Support the `Alter table modify column` statement.](https://github.com/pingcap/tidb/pull/1930)

+ [Support the `Drop view` statement](https://github.com/pingcap/tidb/pull/1969): parsed but ignored.

+ Add [metrics for the transaction size](https://github.com/pingcap/tidb/pull/1982).

+ [A tool for testing the SQL performance.](https://github.com/pingcap/tidb/pull/1920)

## Fixed

+ [A bug in the `show create table` statement.](https://github.com/pingcap/tidb/pull/1968)

+ A few bugs in optimizer: [#1962](https://github.com/pingcap/tidb/pull/1962), [#1963](https://github.com/pingcap/tidb/pull/1963), [#1966](https://github.com/pingcap/tidb/pull/1966), [#1975](https://github.com/pingcap/tidb/pull/1975), [#1977](https://github.com/pingcap/tidb/pull/1977).

## Improved

+ [Improve the cost-based optimizer.](https://github.com/pingcap/tidb/pull/1961)

## Document change

+ Adjust the [README](https://github.com/pingcap/docs) structure to include the document list

+ Add the following new guides:

	* [Data migration from MySQL to TiDB](https://github.com/pingcap/docs/blob/master/op-guide/migration.md)

	* [Overview of the monitoring framework](https://github.com/pingcap/docs/blob/master/op-guide/monitor-overview.md)

	* [Monitoring a TiDB cluster](https://github.com/pingcap/docs/blob/master/op-guide/monitoring-tidb.md)

	* [Compatibility with MySQL](https://github.com/pingcap/docs/blob/master/op-guide/mysql-compatibility.md)


# Weekly update in TiKV

Last week, we landed [23 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2016-11-06..2016-11-12&type=Issues&ref=searchresults) in the TiKV repositories.

## Added

+ [Resolve locks](https://github.com/pingcap/tikv/pull/1271) in batches to avoid generating a huge Raft log when a transaction rolls back. 

+ Add applying snapshot count to enhance the Placement Driver (PD) balance, with PR [1278](https://github.com/pingcap/tikv/pull/1278), [381](https://github.com/pingcap/pd/pull/381).

+ Check [the system configuration](https://github.com/pingcap/tikv/pull/1289) before startup.  

## Fixed

+ Add a [start flag](https://github.com/pingcap/pd/pull/374) to check whether a balance starts or not to fix issue [343](https://github.com/pingcap/pd/issues/343).

+ Fix [the data inconsistency](https://github.com/pingcap/tikv/pull/1287) bug when applying snapshot and committed logs at same time.

## Improved

+ Refactor cache to access easily, with PR [359](https://github.com/pingcap/pd/pull/359), [379](https://github.com/pingcap/pd/pull/379).

+ Update [RocksDB config](https://github.com/pingcap/tikv/pull/1270) to let user configure it more easily. 

+ Slow down Raft [heartbeat and election interval](https://github.com/pingcap/tikv/pull/1275) to reduce the system pressure.

+ Check [the PD list](https://github.com/pingcap/tikv/pull/1282) to ensure the address has a valid format. 

+ Improve `tikv-ctl`, with PR [1273](https://github.com/pingcap/tikv/pull/1273), [1281](https://github.com/pingcap/tikv/pull/1281), [1295](https://github.com/pingcap/tikv/pull/1295).
