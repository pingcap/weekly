---
layout: post
title: TiDB Weekly
---

Last week, we landed [20 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-08-05..2016-08-12%20) in the TiDB repositories.

## Notable changes to `TiDB`

+ Rewrite Lexer and improve the speed of parsing SQL texts by 40%.
+ Add a command line flag for log output file and rotate log files regularly.
+ Optimize the 2 phase commit process and adopt faster methods to clear locks.
+ Optimize the execution speed of the `Insert On Duplicate Update` statement.
+ Update the  [Documents](https://github.com/pingcap/docs) repository.
+ Fix several bugs.
