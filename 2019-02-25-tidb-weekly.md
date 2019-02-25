---
title: Weekly update (February 18 ~ February 24, 2019)
date: 2019-02-25
summary: Last week, we landed 75 PRs in the TiDB repository, 3 PRs in the TiSpark repository, and 21 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [75 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-02-18..2019-02-24+) in the TiDB repository.

## Added

- [Add system tables for the upcoming `RBAC` feature](https://github.com/pingcap/tidb/pull/9377)
- [Add the `log_bin` system variable](https://github.com/pingcap/tidb/pull/9343)
- [Implement the skyline pruning optimization](https://github.com/pingcap/tidb/pull/9337)
- [Add the `FlushTiDBPlugin` support](https://github.com/pingcap/tidb/pull/9320)
- [Add the `ShowCreateView` support](https://github.com/pingcap/tidb/pull/9309)
- [Support the `NAME_CONST` built-in function](https://github.com/pingcap/tidb/pull/9261)
- [Add the `SHOW CREATE USER` support](https://github.com/pingcap/tidb/pull/9240)
- [Support the `ROW_NUMBER()` window function](https://github.com/pingcap/tidb/pull/9098)
- [Add an HTTP API to control whether the check is enabled when the inserted column data is 4-byte UTF-8 characters](https://github.com/pingcap/tidb/pull/9024)
- [Support `ALTER TABLE ALGORITHM = INPLACE/INSTANT`](https://github.com/pingcap/tidb/pull/8811)

## Improved

- [Add the table ID into statistics of columns](https://github.com/pingcap/tidb/pull/9394)
- [Improve the compatibility of `RAND` with MySQL](https://github.com/pingcap/tidb/pull/9387)
- [Improve the compatibility of DDL errors with MySQL](https://github.com/pingcap/tidb/pull/9367)
- [Control the number of rows returned by `TopN/Sort` in one chunk](https://github.com/pingcap/tidb/pull/9364)
- [Support row framed window functions](https://github.com/pingcap/tidb/pull/9358)
- [Control the number of rows returned by `Limit` in one chunk](https://github.com/pingcap/tidb/pull/9354)
- [Change the cost formula for join reordering](https://github.com/pingcap/tidb/pull/9303)
- [Handle `Cancel` properly for DDL jobs](https://github.com/pingcap/tidb/pull/9226)
- [Push down the check condition to TiKV for the `Prewrite` request](https://github.com/pingcap/tidb/pull/9127)
- [Refactor constant folding for `IF`/`IFNULL`](https://github.com/pingcap/tidb/pull/9094)
- [Handle `PARTITION BY RANGE COLUMNS` for a single column](https://github.com/pingcap/tidb/pull/9082)
- [Collect the Coprocessor runtime statistics for `EXPLAIN ANALYZE`](https://github.com/pingcap/tidb/pull/9057)

## Fixed

- [Get the correct `SHOW CREATE TABLE` result when adding an index](https://github.com/pingcap/tidb/pull/9388)
- [Merge the statement buffer in `BatchGetValues`](https://github.com/pingcap/tidb/pull/9374)
- [Show the correct port used by the TiDB server](https://github.com/pingcap/tidb/pull/9365)
- [Fix the unique key constraint check for `CREATE TABLE`](https://github.com/pingcap/tidb/pull/9345)
- [Make the value of `tidb_force_priority` consistent with the configuration value](https://github.com/pingcap/tidb/pull/9342)
- [Fix a panic caused by the `ORDER BY` clause](https://github.com/pingcap/tidb/pull/9333)
- [Fix a panic caused by the timestamp in range partition](https://github.com/pingcap/tidb/pull/9324)
- [Check the unique key constraint for `ALTER TABLE ADD INDEX` on partitioned tables](https://github.com/pingcap/tidb/pull/9323)
- [Fix a wrong default value for the timestamp in multiple time zones](https://github.com/pingcap/tidb/pull/9115)

# Weekly update in TiSpark

Last week, we landed [3 PRs](https://github.com/pingcap/tispark/pulls?utf8=✓&q=is%3Apr+is%3Amerged+merged%3A2019-02-18..2019-02-24+) in the TiSpark repository.

## Added

- [Change the default `spark.version` to 2.3.3](https://github.com/pingcap/tispark/pull/571)

## Fixed

- [Fix the issue of building key ranges with the `XOR` expression](https://github.com/pingcap/tispark/pull/576)

# Weekly update in TiKV and PD

Last week, we landed [21 PRs](https://github.com/search?p=2&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-02-18..2019-02-24&type=Issues) in the TiKV and PD repositories.

## Added

* [Prewrite only when keys do not exist](https://github.com/tikv/tikv/pull/4085)
* [Support encryption for the data stored in the disk](https://github.com/tikv/tikv/pull/3936)

## Improved

* [Bind the port lazily when it is configured](https://github.com/tikv/tikv/pull/4228)
* [Make the batch strategy fairer](https://github.com/tikv/tikv/pull/4200)

# New contributors (Thanks!)

tidb:

- [aliiohs](https://github.com/aliiohs)
- [ltg001](https://github.com/ltg001)

tikv:

- [JoeWrightss](https://github.com/JoeWrightss)

docs-cn:

- [ZhaoQi99](https://github.com/ZhaoQi99)
- [pcqz](https://github.com/pcqz)