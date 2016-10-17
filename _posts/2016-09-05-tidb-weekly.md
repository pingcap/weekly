---
layout: post
title: TiDB Weekly
---

Last week, we landed [29 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-08-29..2016-09-04%20) in the TiDB repositories.

## Notable changes to `TiDB`

+ Support the [unhex](https://github.com/pingcap/tidb/pull/1675) and the [ceiling/ceil](https://github.com/pingcap/tidb/pull/1666) functions
+ Improve the Parser to handle `\r\n`.
+ Solve the potential [concurrency issues](https://github.com/pingcap/tidb/pull/1669)
+ Support [Load Data](https://github.com/pingcap/tidb/pull/1634)
+ Use the [Pipeline model](https://github.com/pingcap/tidb/pull/1622) to filter data through indexes to improve the performance
+ Improve the code to [reduce memory allocation](https://github.com/pingcap/tidb/pull/1663) and improve the performance
+ Fix several bugs.