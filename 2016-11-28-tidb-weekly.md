---
title: Weekly update (November 21 ~ November 27, 2016)
date: 2016-11-28
summary: Last week, we landed 44 PRs in the TiDB repositories, 3 PRs in the TiDB docs repositories, and 20 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV']
---

# Weekly update in TiDB

Last week, we landed [44 PRs](https://github.com/pingcap/tidb/pulls?utf8=✓&q=is%3Apr%20is%3Amerged%20merged%3A2016-11-21..2016-11-27%20) in the TiDB repositories and [3 PRs](https://github.com/pingcap/docs/pulls?utf8=✓&q=is%3Apr%20is%3Amerged%20merged%3A2016-11-21..2016-11-27%20) in the TiDB docs repositories.

## Added

+ [Support creating anonymous index.](https://github.com/pingcap/tidb/pull/2075)

+ [Add the mailing list for TiDB users.](https://github.com/pingcap/tidb/pull/2090)

+ [Support the `show events` syntax.](https://github.com/pingcap/tidb/pull/2099)

## Fixed

+ [Enlarge the ](https://github.com/pingcap/tidb/pull/2004)[Time To Live (TTL)](https://github.com/pingcap/tidb/pull/2004)[ for large transactions.](https://github.com/pingcap/tidb/pull/2004)

+ [Parse float literal using the decimal parser.](https://github.com/pingcap/tidb/pull/2044)

+ [Prevent panic for malformed packets.](https://github.com/pingcap/tidb/pull/2048)

+ [Fix the behavior in the aggregate operator:](https://github.com/pingcap/tidb/pull/2057) for the `select a, c from t groupby t.b` statement, `a` and `c` should use the first row in the group.

+ [ Add sequence number in binlog](https://github.com/pingcap/tidb/pull/2060) to preserve the original mutation order.

+ [Reset the current database after dropping the current database.](https://github.com/pingcap/tidb/pull/2089)

## Improved

+ [Prevent loading schema by multiple threads.](https://github.com/pingcap/tidb/pull/1984)

+ [Make unit test run faster.](https://github.com/pingcap/tidb/pull/2010)

+ [Make explain result clearer.](https://github.com/pingcap/tidb/pull/2063)

+ [Remove `driver.go` from the TiDB project](https://github.com/pingcap/tidb/pull/2066) to enable users to use the MySQL official driver.

## Document change

Add the following new guides:

* [TiDB Cluster Troubleshooting Guide](https://github.com/pingcap/docs/blob/master/trouble-shooting.md)
* [TiKV Tuning Guide](https://pingcap.com/docs/dev/reference/performance/tune-tikv/)

# Weekly update in TiKV

Last week, we landed [20 PRs](https://github.com/search?p=1&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2016-11-20..2016-11-26&ref=searchresults&type=Issues&utf8=%E2%9C%93) in the TiKV repositories.

## Added

+ Add and report the [store labels](https://github.com/pingcap/tikv/pull/1349) to Placement Driver (PD).

+ Add [pending task metrics](https://github.com/pingcap/tikv/pull/1354) for Worker. 

+ Dump all the statistics about [Column Family compaction and Database](https://github.com/pingcap/tikv/pull/1357).

## Fixed

+ Use [`fs2`](https://github.com/pingcap/tikv/pull/1323) to get disk states to fix [#1318](https://github.com/pingcap/tikv/issues/1318)

+ Use the [monotonic clock time](https://github.com/pingcap/tikv/pull/1327) to improve the safety of leader lease read, to fix [#964](https://github.com/pingcap/tikv/issues/964).

+ Check the format of the [listening and advertise address](https://github.com/pingcap/tikv/pull/1335) to fix [#1332](https://github.com/pingcap/tikv/issues/1332).

+ [Get the first value](https://github.com/pingcap/tikv/pull/1339) no matter if it is Null in aggregation. 

+ [Fix a Garbage Collection bug](https://github.com/pingcap/tikv/pull/1350) which deletes the latest deleted key before SafePoint. 

+ [Stop attaching term to the MsgReadIndex message](https://github.com/pingcap/tikv/pull/1353) to fix [#1240](https://github.com/pingcap/tikv/issues/1240).

## Improved

+ Clean up the [command flags and configurations](https://github.com/pingcap/tikv/pull/1307) parsing. 

+ [Abstract a Selector](https://github.com/pingcap/pd/pull/389) to schedule region peer.

+ Split the `Raft Ready` handle to two handles: `Append` and `Apply`. 

+ Use [larger Heartbeat and Election timeout](https://github.com/pingcap/pd/pull/391) to reduce the network pressure. 

+ [Ignore outdated tasks](https://github.com/pingcap/tikv/pull/1324) in Coprocessor to fix [#1305](https://github.com/pingcap/tikv/issues/1305).
