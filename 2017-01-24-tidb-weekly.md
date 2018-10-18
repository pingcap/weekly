---
title: Weekly update (January 09 ~ January 22, 2017)
date: 2017-01-24
summary: Last two weeks, we landed 87 PRs in the TiDB repositories and 50 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV']
---

# Weekly update in TiDB

Last two weeks, we landed [87 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-01-09..2017-01-22%20) in the TiDB repositories.

## Added

* [Support statistic on index data](https://github.com/pingcap/tidb/pull/2349)

* [Support file sort operator](https://github.com/pingcap/tidb/pull/2377)

* [Add key prefix length limitation on index](https://github.com/pingcap/tidb/pull/2380)

* [Support the `TIMESTAMPDIFF` built-in function.](https://github.com/pingcap/tidb/pull/2386)

* [Support the `CONV` built-in function.](https://github.com/pingcap/tidb/pull/2390)

* [Support the `SUBSTR` built-in function.](https://github.com/pingcap/tidb/pull/2422)

* [Support the `SIGN` built-in function.](https://github.com/pingcap/tidb/pull/2427)

* [Support the `FROM_DAYS` built-in function.](https://github.com/pingcap/tidb/pull/2434)

* [Support the `FIELD` built-in function.](https://github.com/pingcap/tidb/pull/2449)

* [Support the `FLOOR` built-in function.](https://github.com/pingcap/tidb/pull/2484)

* [Support the `SQRT` built-in function.](https://github.com/pingcap/tidb/pull/2493)

* Add some metrics: [#2417](https://github.com/pingcap/tidb/pull/2417), [#2419](https://github.com/pingcap/tidb/pull/2419), [#2435](https://github.com/pingcap/tidb/pull/2435), [#2451](https://github.com/pingcap/tidb/pull/2451), [#2460](https://github.com/pingcap/tidb/pull/2460), [#2477])(https://github.com/pingcap/tidb/pull/2477)

* [Set a limitation about the key-value count and size in a single transaction.](https://github.com/pingcap/tidb/pull/2426)

* [Support `Rename Table` and `Alter Table Rename Table` statement.](https://github.com/pingcap/tidb/pull/2444)



## Fixed

* [Add a length limitation for logging sql statement when meet sytax error.](https://github.com/pingcap/tidb/pull/2415)

* [Fix a bug when binary literal has charset prefix.](https://github.com/pingcap/tidb/pull/2438)

* Fix a few bugs about optimizer: [#2439](https://github.com/pingcap/tidb/pull/2439), [#2440](https://github.com/pingcap/tidb/pull/2440), [#2452](https://github.com/pingcap/tidb/pull/2452)

* [Fix a bug about parsing aggragate function.](https://github.com/pingcap/tidb/pull/2453)

* [Fix a bug about two phrase commit.](https://github.com/pingcap/tidb/pull/2454)

* [Fix a bug about `round` function.](https://github.com/pingcap/tidb/pull/2461)

* [Fix a bug occurs when subquery contains a aggragetion.](https://github.com/pingcap/tidb/pull/2486)

* [Fix a memory leak in Join Executor.](https://github.com/pingcap/tidb/pull/2505)


## Improved

* [Use cache to store privilege info.](https://github.com/pingcap/tidb/pull/2388)

* [Refactor correlated subquery optimization.](https://github.com/pingcap/tidb/pull/2411)

* [Speed up delete statement executor.](https://github.com/pingcap/tidb/pull/2421)

* [Handle raft entry too large error.](https://github.com/pingcap/tidb/pull/2425)

* [Change the argument name for displaying version from `v` to `V`:](https://github.com/pingcap/tidb/pull/2442) keep consistent with pd/tikv.

* [Convert distinct to aggragate.](https://github.com/pingcap/tidb/pull/2515)


## New contributor

* [zhexuany](https://github.com/zhexuany)


# Weekly update in TiKV

Last two weeks, We landed [50 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-01-08..2017-01-21&type=Issues&ref=searchresults) in the TiKV repositories.

## Added

* Add `-V` flag for [PD](https://github.com/pingcap/pd/pull/472) and [TiKV](https://github.com/pingcap/tikv/pull/1499).

* Set a limitation for the [max size](https://github.com/pingcap/tikv/pull/1480) of the raft entry. 

* Make [disabling manual compaction](https://github.com/pingcap/tikv/pull/1491) configurable.

* Add fail reason tag in [raft request](https://github.com/pingcap/tikv/pull/1492) and [coprocessor](https://github.com/pingcap/tikv/pull/1518) metrics. 

* Add [snapshot KV count and size](https://github.com/pingcap/tikv/pull/1493) metrics.

* Add [count of written keys](https://github.com/pingcap/tikv/pull/1496) metric.

* Add raft [log lag](https://github.com/pingcap/tikv/pull/1502) metric.

* Add [thread CPU](https://github.com/pingcap/tikv/pull/1494) collector.

* Support [`compaction_readahead_size`](https://github.com/pingcap/tikv/pull/1510) for spinning disk. 

* Support [getting region with key](https://github.com/pingcap/pd/pull/474) in `pd-ctl` .

* Statistic region write key-value [count and bytes](https://github.com/pingcap/tikv/pull/1517).

## Fixed

* Fix a [pitfall](https://github.com/pingcap/pd/pull/470) when use different context package.

* Count [KV count in other CF](https://github.com/pingcap/tikv/pull/1495) when check splitting.

* [Avoid submitting secondary key](https://github.com/pingcap/tikv/pull/1515) if primary key is locked. 

* Use disk size as storage capacity when [capacity is set to 0](https://github.com/pingcap/tikv/pull/1526).

* [Check locked](https://github.com/pingcap/tikv/pull/1530) for `ResolveLock` in latch.

## Improved

* [Keep large integer precision and check integer overflow](https://github.com/pingcap/tikv/pull/1437).

* Check [promotable](https://github.com/pingcap/tikv/pull/1473) when handle raft MsgTimeoutNow.

* Unify [logger](https://github.com/pingcap/tikv/pull/1476).

* [Resume paused follower](https://github.com/pingcap/tikv/pull/1483) when receive `MsgHeartbeatResp` message.

* [Reset the pending state](https://github.com/pingcap/tikv/pull/1489) when add node. 

* Allow [running one GC command](https://github.com/pingcap/tikv/pull/1497) at the same time.

* Guarantee [replicas are safe](https://github.com/pingcap/pd/pull/473) if possible.

* [Keep leader alive](https://github.com/pingcap/pd/pull/475) before initialization.

* Log slow request for [scheduler](https://github.com/pingcap/tikv/pull/1520). 

* Record [scan efficiency](https://github.com/pingcap/tikv/pull/1521) for coprocessor.

* Make [raft log GC](https://github.com/pingcap/tikv/pull/1535) not depend on PeerStorage. 

* [Accelerate ticks](https://github.com/pingcap/tikv/pull/1544) for new split region leader.
