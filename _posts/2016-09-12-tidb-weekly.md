---
layout: post
title: TiDB Weekly
---

Last week, we landed [20 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-09-05..2016-09-11%20) in the TiDB repositories.

## Notable changes to `TiDB`

+ Support [mydumper](https://launchpad.net/mydumper)
+ Use MySQL standard [error code](https://github.com/pingcap/tidb/pull/1700) in the DDL execution results
+ Use [heap sort](https://github.com/pingcap/tidb/pull/1697) operator to handle the statements with Limit and Orderby
+ Add support for the [CLIENT\_CONNECT\_ATTRS](https://github.com/pingcap/tidb/pull/1684)
+ Add the [constant propagation](https://github.com/pingcap/tidb/pull/1652) support to the SQL optimizer
+ Optimize the [index scan executor] (https://github.com/pingcap/tidb/pull/1696) to improve the performance
+ Optimize the distributed SQL API protocol to improve the performance
+ Fix several bugs.