---
layout: post
title: TiDB Weekly
---

Last week, we landed [18 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-09-12..2016-09-18%20) in the TiDB repositories.

## Notable changes to `TiDB`
+ Add the  [Prometheus](https://prometheus.io/) [metrics](https://github.com/pingcap/tidb/pull/1729) and support [push](https://github.com/pingcap/tidb/pull/1733).
+ Support the [streaming aggregation operator](https://github.com/pingcap/tidb/pull/1730).
+ [Rename xapi to distsql](https://github.com/pingcap/tidb/pull/1725) to improve readability.
+ Add [git hash](https://github.com/pingcap/tidb/pull/1724) to the TiDB server status API.
+ [Improve test coverage](https://github.com/pingcap/tidb/pull/1723) in the abstract syntax tree (AST).
+ Enable the [division operator](https://github.com/pingcap/tidb/pull/1727) for the distributed SQL statements.
+ Fix several bugs.