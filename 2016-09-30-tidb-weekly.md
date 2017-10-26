---
date: 2016-09-30T00:00:00Z
title: Weekly Update
---

Last week, we landed [17 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-09-26..2016-09-30%20) in the TiDB repositories and [13 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2016-09-26..2016-09-30&type=Issues&ref=searchresults) in the TiKV repositories.

## Notable changes to `TiDB`

+ [Make the GC alive time configurable](https://github.com/pingcap/tidb/pull/1754) so that users can keep the deleted data as long as they want.
+ [Add the metrics for all kinds of statements](https://github.com/pingcap/tidb/pull/1755) to provide more information for insights.
+ [Improve the kv package test coverage.](https://github.com/pingcap/tidb/pull/1758)
+ [Record the processed row count during DDL](https://github.com/pingcap/tidb/pull/1759) so that users can track the progress of DDL.
+ [Consider the limit clause in the cost based optimizer (CBO) framework.](https://github.com/pingcap/tidb/pull/1760)
+ [Add metrics for kv errors.](https://github.com/pingcap/tidb/pull/1765)
+ [Make truncate statement a DDL](https://github.com/pingcap/tidb/pull/1766) to convert the truncate operation into a `drop table` process followed by a `create table` process. Then TiDB can delete the truncated data with a background worker.

## Notable changes to `TiKV`

+ Add a metric for [Raft vote](https://github.com/pingcap/tikv/pull/1111) to monitor server's stability. 
+ Improve the test coverage for [scheduler](https://github.com/pingcap/tikv/pull/1113), [Raft](https://github.com/pingcap/tikv/pull/1117).
+ Check the [stale snapshot](https://github.com/pingcap/tikv/pull/1115) to fix [1084](https://github.com/pingcap/tikv/issues/1084).
+ [Reuse iterator](https://github.com/pingcap/tikv/pull/1116) to speed up `scan`.
+ [Remove `delete_file_in_range`](https://github.com/pingcap/tikv/pull/1124) to fix [1121](https://github.com/pingcap/tikv/issues/1121).

## Notable changes to `Placement Driver (PD)`

+ Add [more metrics](https://github.com/pingcap/pd/pull/330) to monitor the server.

