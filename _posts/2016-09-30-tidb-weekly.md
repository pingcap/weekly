---
layout: post
title: TiDB Weekly
---

Last week, we landed [17 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-09-26..2016-09-30%20) in the TiDB repositories.

## Notable changes to `TiDB`

+ [Make the GC alive time configurable](https://github.com/pingcap/tidb/pull/1754) so that users can keep the deleted data as long as they want.
+ [Add the metrics for all kinds of statements](https://github.com/pingcap/tidb/pull/1755) to provide more information for insights.
+ [Improve the kv package test coverage.](https://github.com/pingcap/tidb/pull/1758)
+ [Record the processed row count during DDL](https://github.com/pingcap/tidb/pull/1759) so that users can track the progress of DDL.
+ [Consider the limit clause in the cost based optimizer (CBO) framework.](https://github.com/pingcap/tidb/pull/1760)
+ [Add metrics for kv errors.](https://github.com/pingcap/tidb/pull/1765)
+ [Make truncate statement a DDL.](https://github.com/pingcap/tidb/pull/1766) Convert the truncate operation into a `drop table` process followed by a `create table` process. Then TiDB can delete the truncated data with a background worker.

