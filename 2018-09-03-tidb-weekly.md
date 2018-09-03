---
title: Weekly update (August 27 ~ September 02, 2018)
date: 2018-09-03
summary: Last week, we landed 45 PRs in the TiDB repository, 2 PRs in the TiSpark repository, and 30 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [45 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-08-27..2018-09-02+) in the TiDB repository.

## Added

* [Enable the `Mutex` profiling in the TiDB server](https://github.com/pingcap/tidb/pull/7510)
* [Let `Analyze` use the `RC` level and the low priority](https://github.com/pingcap/tidb/pull/7496)
* [Support `Grow` of the chunk capacity](https://github.com/pingcap/tidb/pull/7473)
* [Add job action and schema version information to metrics](https://github.com/pingcap/tidb/pull/7472)
* [Forbid users to drop an important system table](https://github.com/pingcap/tidb/pull/7471)
* [Support `rollback` when adding an index in a partitioned table](https://github.com/pingcap/tidb/pull/7437)
* [Add a `KeyOnly` option for the `Seek` operation](https://github.com/pingcap/tidb/pull/7419)
* [Maintain `HistColl` in `StatsInfo` of `DataSource`](https://github.com/pingcap/tidb/pull/7385)
* [Add a TiDB tracing prototype](https://github.com/pingcap/tidb/pull/7016)

## Improved

* [Remove `goroutine_pool`](https://github.com/pingcap/tidb/pull/7564)
* [Remove the test coverage task from `travis`](https://github.com/pingcap/tidb/pull/7533)
* [Rebase the auto increment ID when needed](https://github.com/pingcap/tidb/pull/7515)
* [Fix the lint tool](https://github.com/pingcap/tidb/pull/7503)
* [Make the duplicate error output in the `Update` statement more clearly](https://github.com/pingcap/tidb/pull/7495)
* [Bump Go version to 1.11](https://github.com/pingcap/tidb/pull/7491)
* [Make `TestTableSplit` stable in the `ddl` package](https://github.com/pingcap/tidb/pull/7487)
* [Improve compatibility for converting a string to an integer](https://github.com/pingcap/tidb/pull/7483)
* [Use the `shallow` copy for `Join`](https://github.com/pingcap/tidb/pull/7433)
* [Improve the `propagate` constant and propagate more filters](https://github.com/pingcap/tidb/pull/7276)

## Fixed

* [Fix the Hash Join executor and break the `innerTable` fetcher if an error happens during fetching the outer table](https://github.com/pingcap/tidb/pull/7554)
* [Fix the `AutoAnalyze` trigger condition](https://github.com/pingcap/tidb/pull/7550)
* [Fix data race in `ddl.TestStat()`](https://github.com/pingcap/tidb/pull/7548)
* [Add an unsigned flag to the Year type](https://github.com/pingcap/tidb/pull/7542)
* [Fix the `last_insert_id` in `INSERT... ON DUPLICATE KEY UPDATE`](https://github.com/pingcap/tidb/pull/7534)
* [Fix the update error of zero column size in the `statistics` package](https://github.com/pingcap/tidb/pull/7530)
* [Fix the issue that the Year type string format has too many leading zeros in the `Prepare` and `Execute` statements](https://github.com/pingcap/tidb/pull/7525)
* [Fix the `insert zero timestamp` bug in the `Prepare` statement](https://github.com/pingcap/tidb/pull/7506) 
* [Fix the `out of range` error for `intdiv`](https://github.com/pingcap/tidb/pull/7492)
* [Fix `ComStmtSendLongData` when the data length is `0`](https://github.com/pingcap/tidb/pull/7485)
* [Fix the `INSERT... ON DUPLICATE KEY UPDATE` plan](https://github.com/pingcap/tidb/pull/7406)
* [Fix a bug for bit default value](https://github.com/pingcap/tidb/pull/7249)
* [Fix the `admin check table` error when a column of the index is virtually generated](https://github.com/pingcap/tidb/pull/6817)

# Weekly update in TiSpark

Last week, we landed [2 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-08-27..2018-09-02+) in the TiSpark repository.

## Fixed

- [Fix the issue that `table not exists` might occur when loading the table](https://github.com/pingcap/tispark/pull/430)

## Improved

- [Add details in the `explain` result](https://github.com/pingcap/tispark/pull/428)

# Weekly update in TiKV and PD

Last week, we landed [30 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-08-27..2018-09-02&type=Issues) in the TiKV and PD repositories.

## Added

- Add new built-in functions:

    - [`builtin-is_ipv6`](https://github.com/tikv/tikv/pull/3479)
    - [`builtin-sign`](https://github.com/tikv/tikv/pull/3518)
    - [`builtin-atan_1_arg` and `builtin-atan_2_args`](https://github.com/tikv/tikv/pull/3520)

- Add new documents:
    
    - [`overview`, `op-guide`, and `client`](https://github.com/tikv/tikv/pull/3494)
    - [TiKV Control User Guide](https://github.com/tikv/tikv/pull/3502)
    - [RocksDB Option Configuration](https://github.com/tikv/tikv/pull/3526)
    - [TiKV Coprocessor Configuration](https://github.com/tikv/tikv/pull/3535)
    - [Reference to CNCF](https://github.com/tikv/tikv/pull/3541)

- [Add a method to get `approximate_split_keys()`](https://github.com/tikv/tikv/pull/3506)
- [Add `keepalive` configurations](https://github.com/tikv/tikv/pull/3533/files)
- [Add statistics for the PD simulator](https://github.com/pingcap/pd/pull/1218)
- [Add the `GetAllStores` function to the PD Client interface](https://github.com/pingcap/pd/pull/1228)

## Fixed

- [Fix the false stale peer alert](https://github.com/tikv/tikv/pull/3483) 

## Improved

- [Use the `approximate` way to split large Regions](https://github.com/tikv/tikv/pull/3511)
- [Reduce `clone` in the transaction process](https://github.com/tikv/tikv/pull/3530)
- [Print the help message when starting tikv-ctl without arguments](https://github.com/tikv/tikv/pull/3531)
- [Remove some unnecessary conversions in PD](https://github.com/pingcap/pd/pull/1229)

# New contributors (Thanks!)

tidb-operator:

- [fengzixu](https://github.com/fengzixu)

tidb:

- [shafreeck](https://github.com/shafreeck)

tikv:

- [Observer42](https://github.com/Observer42)
- [caniszczyk](https://github.com/caniszczyk)