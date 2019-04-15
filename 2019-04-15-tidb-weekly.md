---
title: Weekly update (April 08 ~ April 14, 2019)
date: 2019-04-15
summary: Last week, we landed 52 PRs in the TiDB repository, 9 PRs in the TiSpark repository, and 32 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [52 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-04-08..2019-04-14+) in the TiDB repository.

## Added

- [Add the `tidb_skip_isolation_level_check` variable to skip the isolation check](https://github.com/pingcap/tidb/pull/10065)
- [Support fast `Analyze` in the planner and executor's builder](https://github.com/pingcap/tidb/pull/10040)
- [Support `EXPLAIN` on `ConnectionID`](https://github.com/pingcap/tidb/pull/10030)
- [Add the `RevokeRole` support](https://github.com/pingcap/tidb/pull/9771)

## Improved

- [Validate the value when setting the `read_only` variable](https://github.com/pingcap/tidb/pull/10072)
- [Refine some code in `http_handler.go`](https://github.com/pingcap/tidb/pull/10071)
- [Improve the UT coverage of the `metrics` package to 100%](https://github.com/pingcap/tidb/pull/10066)
- [Remove the useless `memoryAllocator` struct](https://github.com/pingcap/tidb/pull/10061)
- [Make `convertToIndexScan` and `convertToTableScan` return results more quickly](https://github.com/pingcap/tidb/pull/10058)
- [Improve the UT coverage of the `meta` package from 76% to 85%](https://github.com/pingcap/tidb/pull/10054)
- [Solve the bootstrap write conflict when starting multiple `tidb-server`s in a new cluster](https://github.com/pingcap/tidb/pull/10029)
- [Update the `db-table/{table_partition_id}` HTTP API](https://github.com/pingcap/tidb/pull/10026)
- [Improve the UT coverage of the `util/kvencoder` package to 85%](https://github.com/pingcap/tidb/pull/10008)
- [Trace and control the memory usage in DistSQL layer](https://github.com/pingcap/tidb/pull/10003)
- [Improve the UT coverage of `types/json` package to 85%](https://github.com/pingcap/tidb/pull/9977)
- [Stop server startup if an unrecognized option is found in a configuration file](https://github.com/pingcap/tidb/pull/9855)
- [Ignore `Fulltext` keys in the `CREATE TABLE` and `ALTER TABLE` statements](https://github.com/pingcap/tidb/pull/9821)
- [Check the `KEY` option for the generated column when creating a table](https://github.com/pingcap/tidb/pull/9529)

## Fixed

- [Fix the issue that `EXTRACT MONTH` does not support 0](https://github.com/pingcap/tidb/pull/10116)
- [Fix the issue that `MONTHNAME` is incompatible with MySQL](https://github.com/pingcap/tidb/pull/10109)
- [Fix the issue that `JSON_KEY` is incompatible with MySQL](https://github.com/pingcap/tidb/pull/10090)
- [Fix the issue that `MAKETIME` is incompatible with MySQL](https://github.com/pingcap/tidb/pull/10074)
- [Fix the leak test failure issue of `RecordSet`](https://github.com/pingcap/tidb/pull/10063)
- [Fix the issue that `EXPLAIN ANALYZE` does not include the `execution info` column](https://github.com/pingcap/tidb/pull/10035)
- [Fix the issue that `Charset`/`Collation` shown in `SHOW FULL COLUMNS` is incompatible with MySQL](https://github.com/pingcap/tidb/pull/10007)
- [Fix the wrongly altering `SHARD_ROW_ID_BITS` issue in some cases](https://github.com/pingcap/tidb/pull/9868)

# Weekly update in TiSpark

Last week, we landed [9 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-04-08..2019-04-14+) in the TiSpark repository.

## Added

- [Support the `CreateTableLike` command](https://github.com/pingcap/tispark/pull/641)

## Fixed

- [Remove the `Spark` dependency in `tikv-client`](https://github.com/pingcap/tispark/pull/634)
- [Fix the `desc table` command failure issue for hive tables](https://github.com/pingcap/tispark/pull/643)
- [Fix incorrect `next()` implementation for `Key`](https://github.com/pingcap/tispark/pull/648)

## Improved

- [Clean up the `JSONType` code](https://github.com/pingcap/tispark/pull/633)

# Weekly update in TiKV and PD

Last week, we landed [32 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-04-08..2019-04-14&type=Issues) in the TiKV and PD repositories.

## Added

* [Add metrics for TSO handling time in PD](https://github.com/pingcap/pd/pull/1504)

## Improvement

* [Move `tikv_util` as a component](https://github.com/tikv/tikv/pull/4504)
* [Use `tokio-threadpool` and thread local metrics for `readpool`](https://github.com/tikv/tikv/pull/4486)
* [Add the `max_columns` check when building a vectorized expression](https://github.com/tikv/tikv/pull/4481)
* [Add the `tcmalloc` support to the `tikv_alloc` crate](https://github.com/tikv/tikv/pull/4370)

## Fixed

* [Fix the prefix extractor panic when deleting a range](https://github.com/tikv/tikv/pull/4503)
* [Remove `strict_sql_mode` covered by `sql_mode`](https://github.com/tikv/tikv/pull/4494)
* [Avoid a panic in `RotatingFileLogger` of TiKV](https://github.com/tikv/tikv/pull/4492)
* [Enlarge the stall buffer ingested by TiKV](https://github.com/tikv/tikv/pull/4475)

# New contributors (Thanks!)

tikv:

- [ZhangHanDong](https://github.com/ZhangHanDong)

tidb-operator:

- [qiffang](https://github.com/qiffang)

parser:

- [hhxcc](https://github.com/hhxcc)

docs-cn:

- [reAsOn2010](https://github.com/reAsOn2010)
