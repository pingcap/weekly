---
date: 2016-10-17T00:00:00Z
title: Weekly Update
---

Last week, we landed [27 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-10-01..2016-10-16) in the TiDB repositories and [32 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2016-10-02..2016-10-16&type=Issues&ref=searchresults) in the TiKV repositories.

## Notable changes to `TiDB`

+ Support [projection elimination](https://github.com/pingcap/tidb/pull/1740) so that the executor can run faster when it is not necessary to have a projection layer.

+ [Write DDL binlog](https://github.com/pingcap/tidb/pull/1752) to file.

+ [Convert sort and limit to top-n in the query planning phrase.](https://github.com/pingcap/tidb/pull/1769)

+ [Support reading history data even if the schema changes. ](https://github.com/pingcap/tidb/pull/1790)

+ Add comments for the [server package](https://github.com/pingcap/tidb/pull/1798) and the [plan package](https://github.com/pingcap/tidb/pull/1804).

+ [Add metrics for GC configuration.](https://github.com/pingcap/tidb/pull/1814)

+ [Verify the data for utf-8 columns.](https://github.com/pingcap/tidb/pull/1818)

+ Fix bugs.

## Notable changes to `TiKV`

+ [Compact the `lock` column family](https://github.com/pingcap/tikv/pull/1125) periodically. 
+ Add [random latency filter](https://github.com/pingcap/tikv/pull/1120) to simulate the transport test. 
+ Improve the [datum test](https://github.com/pingcap/tikv/pull/1152) coverage.
+ [Cache the Raft log term](https://github.com/pingcap/tikv/pull/1154) to avoid calling `rocksdb::get` every time. 
+ [Check the store ID](https://github.com/pingcap/tikv/pull/1155) before sending to raftstore and [refresh expired store address](https://github.com/pingcap/tikv/pull/1156) for the resolve process to fix [issue 1153](https://github.com/pingcap/tikv/issues/1153).
+ [Add new regions' meta in StaleEpoch error](https://github.com/pingcap/tikv/pull/1160) to fix [issue 974](https://github.com/pingcap/tikv/issues/974).
+ Coprocessor supports [timezone](https://github.com/pingcap/tikv/pull/1166) for timestamp comparison.

## Notable changes to `Placement Driver`

+ Ignore balancing the [peer with on-going operation](https://github.com/pingcap/pd/pull/331) to fix [TiKV issue 1084](https://github.com/pingcap/tikv/issues/1084).
