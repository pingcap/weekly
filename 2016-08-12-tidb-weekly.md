---
title: Weekly update (August 5 ~ August 12, 2016)
date: 2016-08-12
summary: Last week, we landed 20 PRs in the TiDB repositories and 11 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV']
---

Last week, we landed [20 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-08-05..2016-08-12%20) in the TiDB repositories and [11 PRs](https://github.com/search?p=1&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2016-08-06..2016-08-12&ref=searchresults&type=Issues&utf8=%E2%9C%93) in the TiKV repositories.

## Notable changes to `TiDB`

+ Rewrite Lexer and improve the speed of parsing SQL texts by 40%.
+ Add a command line flag for log output file and rotate log files regularly.
+ Optimize the 2 phase commit process and adopt faster methods to clear locks.
+ Optimize the execution speed of the `Insert On Duplicate Update` statement.
+ Update the  [Documents](https://github.com/pingcap/docs) repository.
+ Fix several bugs.

## Notable changes to `TiKV`

+ Support the `Scan` and `Resolve` transaction lock. 
+ Support garbage collection(GC) stale peer.
+ Use a `Write` column family to store transaction commit logs. 
+ Remove the unnecessary `Seek` operation.
+ Fix random quorum test.

## Notable changes to `Placement Driver`

+ Support the `get PD leader` API.
