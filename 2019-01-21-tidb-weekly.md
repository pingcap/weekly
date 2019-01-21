---
title: Weekly update (January 14 ~ January 20, 2019)
date: 2019-01-21
summary: Last week, we landed 57 PRs in the TiDB repository, 1 PR in the TiSpark repository, and 19 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [57 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-01-14..2019-01-20+) in the TiDB repository.

## Added

- [Add the `ALLOW_INVALID_DATES` SQL mode support](https://github.com/pingcap/tidb/pull/9027)
- [Support the `PARTITION` syntax for selecting partition tables](https://github.com/pingcap/tidb/pull/8990)
- [Support the aggregate window function without the frame in the executor](https://github.com/pingcap/tidb/pull/8899)
- [Support `SHOW CREATE TABLE` for `View`](https://github.com/pingcap/tidb/pull/8865)
- [Support the `OR REPLACE` syntax for `CREATE VIEW`](https://github.com/pingcap/tidb/pull/8856)
- [Support restoring deleted tables](https://github.com/pingcap/tidb/pull/7937)

## Improved

- [Improve error messages for MySQL compatibility](https://github.com/pingcap/tidb/pull/9112)
- [Cut the scan range by Region before sending requests to TiKV](https://github.com/pingcap/tidb/pull/9070)
- [Handle the optimizer hint properly for Cartesian Join](https://github.com/pingcap/tidb/pull/9037)
- [Enable the plugin framework in TiDB](https://github.com/pingcap/tidb/pull/9006)
- [Support the Window function with the frame in the planner](https://github.com/pingcap/tidb/pull/9004)
- [Send gRPC messages to TiKV in batch](https://github.com/pingcap/tidb/pull/8986)
- [Disallow `ALTER TABLE` on `View`](https://github.com/pingcap/tidb/pull/8890)
- [Use constraint propagation in partition pruning](https://github.com/pingcap/tidb/pull/8885)
- [Print the column character set in `SHOW CREATE TABLE`](https://github.com/pingcap/tidb/pull/8866)
- [Return an error when `INSERT`/`UPDATE`/`ANALYZE`/`DELETE` a `View`](https://github.com/pingcap/tidb/pull/8848)
- [Modify the max length limit of the `VARCHAR` type](https://github.com/pingcap/tidb/pull/8818)
- [Support the reverse raw scan on TiKV](https://github.com/pingcap/tidb/pull/8352)
- [Build a new histogram using range information](https://github.com/pingcap/tidb/pull/7921)

## Fixed

- [Fix a false negative result of `ADMIN CHECK TABLE`](https://github.com/pingcap/tidb/pull/9108)
- [Make the statistics worker recover from the panic correctly](https://github.com/pingcap/tidb/pull/9072)
- [Fix a wrong result of `MergeJoin`](https://github.com/pingcap/tidb/pull/9046)
- [Fix a panic caused by parsing the CSV input](https://github.com/pingcap/tidb/pull/9005)
- [Fix an incorrect behavior under the `NO_ZERO_DATE` SQL mode](https://github.com/pingcap/tidb/pull/8765)

# Weekly update in TiSpark

Last week, we landed [1 PR](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-01-14..2019-01-20+) in the TiSpark repository.

## Fixed

- [Fix the possible null version in `pom`](https://github.com/pingcap/tispark/pull/555)

# Weekly update in TiKV and PD

Last week, we landed [19 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-01-14..2019-01-20&type=Issues) in the TiKV and PD repositories.

## Added

- [Add the `add_time_duration_null` Coprocessor pushdown function](https://github.com/tikv/tikv/pull/4063)
- [Verify the TiDB range in Coprocessor Endpoint](https://github.com/tikv/tikv/pull/4013)
- [Add multi-thread RaftStore](https://github.com/tikv/tikv/pull/4066)

## Improved

- [Pass `db` options to `ldb` in tikv-ctl](https://github.com/tikv/tikv/pull/4068)

## Fixed

- [Fix the potential nil panic in the `AdjacentRegion` scheduler after PD leader is changed](https://github.com/pingcap/pd/pull/1403)
- [Fix the `month_name` Coprocessor pushdown function](https://github.com/tikv/tikv/pull/4063)
- [Fix the `epollex` error on MacOS](https://github.com/tikv/tikv/pull/4084)

# New contributors (Thanks!)

tidb:

- [ariesdevil](https://github.com/ariesdevil)
- [kamijin-fanta](https://github.com/kamijin-fanta)

tikv:

- [JaySon-Huang](https://github.com/JaySon-Huang)
- [ariesdevil](https://github.com/ariesdevil)

tispark:

- [ariesdevil](https://github.com/ariesdevil)

parser:

- [GunaYX](https://github.com/GunaYX)
- [cgcgbcbc](https://github.com/cgcgbcbc)