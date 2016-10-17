---
layout: post
title: TiDB Weekly
---

Last week, we landed [26 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-08-22..2016-08-28%20) in the TiDB repositories.

## Notable changes to `TiDB`
+ Support [the MySQL SetOption Command and Multiple Statements](https://github.com/pingcap/tidb/pull/1628).
+ Support filter push-down for the [Time](https://github.com/pingcap/tidb/pull/1629)/[Decimal](https://github.com/pingcap/tidb/pull/1651) type.
+ Support converting OuterJoin to InnerJoin by using [Null Reject](https://github.com/pingcap/tidb/pull/1630).
+ Support [multiple-thread Hash Join](https://github.com/pingcap/tidb/pull/1591).
+ Support [Garbage Collector](https://github.com/pingcap/tidb/pull/1577).
+ Optimize the code to improve the [Performance](https://github.com/pingcap/tidb/pull/1641).
+ Fix several bugs.