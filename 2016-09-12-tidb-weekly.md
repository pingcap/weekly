---
date: 2016-09-12T00:00:00Z
title: Weekly Update
url: /2016/09/12/tidb-weekly/
---

Last week, we landed [20 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-09-05..2016-09-11%20) in the TiDB repositories and [32 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2016-09-05..2016-09-11&type=Issues&ref=searchresults) in the TiKV repositories..

## Notable changes to `TiDB`

+ Support [mydumper](https://launchpad.net/mydumper)
+ Use MySQL standard [error code](https://github.com/pingcap/tidb/pull/1700) in the DDL execution results
+ Use [heap sort](https://github.com/pingcap/tidb/pull/1697) operator to handle the statements with Limit and Orderby
+ Add support for the [CLIENT\_CONNECT\_ATTRS](https://github.com/pingcap/tidb/pull/1684)
+ Add the [constant propagation](https://github.com/pingcap/tidb/pull/1652) support to the SQL optimizer
+ Optimize the [index scan executor] (https://github.com/pingcap/tidb/pull/1696) to improve the performance
+ Optimize the distributed SQL API protocol to improve the performance
+ Fix several bugs.

## Notable changes to `TiKV`

+ Add the [divide operation](https://github.com/pingcap/tikv/pull/1009) support to Coprocessor.
+ Switch to the [prometheus metrics](https://github.com/pingcap/tikv/pull/1017) from the statsd metrics. 
+ [Abort](https://github.com/pingcap/tikv/pull/1020) applying the snapshot if it conflicts with a new one to fix [1014](https://github.com/pingcap/tikv/issues/1014).
+ Ensure that the data from the last `write` before the GC Safe-Point time [can't be removed](https://github.com/pingcap/tikv/pull/1022) to fix [1021](https://github.com/pingcap/tikv/issues/1021).
+ Add the [document](https://github.com/pingcap/tikv/pull/1023) for `Scheduler`.
+ Calculate the [used space](https://github.com/pingcap/tikv/pull/1026) correctly.
+ [Stop GC scan](https://github.com/pingcap/tikv/pull/1036) if there are no keys left to fix the endless-loop problem.

## Notable changes to `Placement Driver`

+ Support [store removing](https://github.com/pingcap/pd/pull/306) gracefully.
+ Add the [Admin API](https://github.com/pingcap/pd/pull/308).
+ [Reduce the default `min-capacity-used-ratio`](https://github.com/pingcap/pd/pull/314) value for an earlier auto-balance.
