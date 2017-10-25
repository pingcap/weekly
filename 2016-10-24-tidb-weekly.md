---
date: 2016-10-24T00:00:00Z
title: Weekly Update
url: /2016/10/24/tidb-weekly/
---

Last week, we landed [30 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-10-17..2016-10-24%20) in the TiDB repositories and [26 PRs](https://github.com/search?p=1&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2016-10-17..2016-10-23&ref=searchresults&type=Issues&utf8=%E2%9C%93) in the TiKV repositories.

## Notable changes to `TiDB`

+ [Set the concurrency for the SQL executor using the Set statement](https://github.com/pingcap/tidb/pull/1795)

+ [Convert the `Limit+Sort` operator to the `TopN` operator on local storage](https://github.com/pingcap/tidb/pull/1819)

+ [Fix the gotouinue leak problem](https://github.com/pingcap/tidb/pull/1834)

+ [Support the logic/bitwise operator on local storage](https://github.com/pingcap/tidb/pull/1838)

+ [Support creating user without password](https://github.com/pingcap/tidb/pull/1841)

+ [Eliminate common aggregation function](https://github.com/pingcap/tidb/pull/1843)

+ [Support the Drop User statement](https://github.com/pingcap/tidb/pull/1854)

+ Fix bugs

## Notable changes to `TiKV`

+ Provide a tool [`tikv-ctl`](https://github.com/pingcap/tikv/pull/1163) to browse the internal data in RocksDB. 
+ Make [the Raft column family](https://github.com/pingcap/tikv/pull/1171) configurable. 
+ Avoid [deleting other regions' data](https://github.com/pingcap/tikv/pull/1174) accidentally.
+ Coprocessor supports [`minus`, `intdiv` and `mod`](https://github.com/pingcap/tikv/pull/1180) operations. 
+ Support canceling a [applying snapshot job](https://github.com/pingcap/tikv/pull/1182) which is in queue directly.
+ Use [`get_region_by_id`](https://github.com/pingcap/tikv/pull/1184) to check the stale region.
+ [Skip fetching unnecessary values](https://github.com/pingcap/tikv/pull/1192)  to speed up the scan performance. 
+ Add [flow control](https://github.com/pingcap/tikv/pull/1195) to fix [issue 1190](https://github.com/pingcap/tikv/issues/1190)
+ [Clean up temporary snapshot](https://github.com/pingcap/tikv/pull/1197) file when startup.
+ [Shrink the send buffer](https://github.com/pingcap/tikv/pull/1205) after sending a big query to avoid occupying too much memory.

## Notable changes to `Placement Driver`

+ Add [`uptime`](https://github.com/pingcap/pd/pull/341) to show the online time for a store. 
+ [Embed `metapb.Store`](https://github.com/pingcap/pd/pull/352) into `storeInfo` to make the code cleaner.
