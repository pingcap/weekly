---
date: 2016-10-31T00:00:00Z
title: Weekly Update
url: /2016/10/31/tidb-weekly/
---

Last week, we landed [24 PRs](https://github.com/pingcap/tidb/pulls?utf8=✓&q=is%3Apr%20is%3Amerged%20merged%3A2016-10-25..2016-10-31%20) in the TiDB repositories and [28 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2016-10-24..2016-10-30&type=Issues&ref=searchresults) in the TiKV repositories.

## Notable changes to `TiDB`

+ [Support coalesce/case when pushing down on local storage](https://github.com/pingcap/tidb/pull/1856)。

+ [Support showing indexes in the table syntax.](https://github.com/pingcap/tidb/pull/1873)

+ [Split eval.go into some smaller files](https://github.com/pingcap/tidb/pull/1865) to make code cleaner.

+ [Fix a bug about truncating data.](https://github.com/pingcap/tidb/pull/1877)

+ [Fix the mysql version number format.](https://github.com/pingcap/tidb/pull/1879)

+ [Fix a bug about dropping the nonexist foreign key.](https://github.com/pingcap/tidb/pull/1874)

+ [Fix a bug in the parser where hexadecimal was parsed as string.](https://github.com/pingcap/tidb/pull/1871)

+ [Add comments for executor package](https://github.com/pingcap/tidb/pull/1876) to improve code readability.

+ [Add a command line flag to print binary version.](https://github.com/pingcap/tidb/pull/1896)

+ [Add a command line flag to prevent cartesian product.](https://github.com/pingcap/tidb/pull/1894)

## Notable changes to `TiKV`

+ [Compact region](https://github.com/pingcap/tikv/pull/1204) automatically after deleting lots of keys. 
+ Remove the [`rocksdb` DSN](https://github.com/pingcap/tikv/pull/1209) for the `tikv-server` command flag.
+ Use an [atomic value](https://github.com/pingcap/tikv/pull/1210) to control the snapshot progress. 
+ Add [timer](https://github.com/pingcap/tikv/pull/1211) for latch waiting. 
+ [Check the region range](https://github.com/pingcap/tikv/pull/1219) before replicating a peer.
+ Make sure the [callback](https://github.com/pingcap/tikv/pull/1224) command is called. 
+ Coprocessor supports the [`multiply` operator](https://github.com/pingcap/tikv/pull/1216).
+ Coprocessor supports the [`case when`operator](https://github.com/pingcap/tikv/pull/1227).  
+ [Record the last compacted index](https://github.com/pingcap/tikv/pull/1230) to speed up compacting the Raft log.

## Notable changes to `Placement Driver`

+ Refactor store/region cache to make code clearer, including PR [353](https://github.com/pingcap/pd/pull/353), [365](https://github.com/pingcap/pd/pull/365), [366](https://github.com/pingcap/pd/pull/366).
+ Support the [`GetPDMembers`](https://github.com/pingcap/pd/pull/357) API.

## New contributors

+ [Librazy](https://github.com/Librazy)
