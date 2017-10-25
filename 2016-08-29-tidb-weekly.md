---
date: 2016-08-29T00:00:00Z
title: Weekly Update
url: /2016/08/29/tidb-weekly/
---

Last week, we landed [26 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-08-22..2016-08-28%20) in the TiDB repositories and [26 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2016-08-22..2016-08-28&type=Issues&ref=searchresults) in the TiKV repositories.

## Notable changes to `TiDB`
+ Support [the MySQL SetOption Command and Multiple Statements](https://github.com/pingcap/tidb/pull/1628).
+ Support filter push-down for the [Time](https://github.com/pingcap/tidb/pull/1629)/[Decimal](https://github.com/pingcap/tidb/pull/1651) type.
+ Support converting OuterJoin to InnerJoin by using [Null Reject](https://github.com/pingcap/tidb/pull/1630).
+ Support [multiple-thread Hash Join](https://github.com/pingcap/tidb/pull/1591).
+ Support [Garbage Collector](https://github.com/pingcap/tidb/pull/1577).
+ Optimize the code to improve the [Performance](https://github.com/pingcap/tidb/pull/1641).
+ Fix several bugs.

## Notable changes to `TiKV`

+ Coprocessor supports the [time type](https://github.com/pingcap/tikv/pull/949).
+ Output the [version information](https://github.com/pingcap/tikv/pull/952) when TiKV starts.
+ Append the [write column family](https://github.com/pingcap/tikv/pull/954) when committing lock-only keys to fix bug [#921](https://github.com/pingcap/tikv/issues/921).
+ Use randomized Placement Driver (PD) server and [remove getting PD leader](https://github.com/pingcap/tikv/pull/976) to solve issues [#942](https://github.com/pingcap/tikv/issues/942) and [#956](https://github.com/pingcap/tikv/issues/956).
+ Support the [Debug traits](https://github.com/pingcap/tikv/pull/986) for messages in the sending channel. 
+ Coprocessor uses [configuration](https://github.com/pingcap/tikv/pull/985) to make the endpoint threadpool size configurable.

## Notable changes to `Placement Driver`

+ Output the [version information](https://github.com/pingcap/pd/pull/279) when PD starts.
+ Save the [next timestamp oracle(TSO)](https://github.com/pingcap/pd/pull/290) to solve issue [#191](https://github.com/pingcap/pd/issues/191).
