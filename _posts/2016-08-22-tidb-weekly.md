---
layout: post
title: TiDB Weekly
---

Last week, we landed [26 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-08-13..2016-08-21%20) in the TiDB repositories.

## Notable changes to `TiDB`

+ Upgrade the [query optimizer](https://github.com/pingcap/tidb/pull/1609).
+ Upgrade the [lexer](https://github.com/pingcap/tidb/pull/1566).
+ Replace golang protobuf with [gogo protobuf](https://github.com/pingcap/tidb/pull/1610).
+ Optimize the [distributed executor](https://github.com/pingcap/tidb/pull/1599).
+ Repair the [Time](https://github.com/pingcap/tidb/pull/1592) and [Decimal](https://github.com/pingcap/tidb/pull/1598) types to improve the compatibility with MySQL.
+ Support the [Set names binary](https://github.com/pingcap/tidb/pull/1578) statement.
+ Support [Covering Index](https://github.com/pingcap/tidb/pull/1567).
+ Optimize the table scanning when the condition is [false constant](https://github.com/pingcap/tidb/pull/1589).
+ Fix several bugs.
