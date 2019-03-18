---
title: Weekly update (March 11 ~ March 17, 2019)
date: 2019-03-18
summary: Last week, we landed 63 PRs in the TiDB repository, 6 PRs in the TiSpark repository, and 28 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [63 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-03-11..2019-03-17+) in the TiDB repository.

## Added

- [Support the `NTILE` window function](https://github.com/pingcap/tidb/pull/9682)
- [Support the `LEAD` and `LAG` window functions](https://github.com/pingcap/tidb/pull/9672)
- [Support the `PERCENT_RANK` window functions](https://github.com/pingcap/tidb/pull/9671)
- [Support the `CUME_DIST` window function](https://github.com/pingcap/tidb/pull/9619)
- [Support the `NTH_VALUE` window function](https://github.com/pingcap/tidb/pull/9596)
- [Support the `log_bin` variable](https://github.com/pingcap/tidb/pull/9634)
- [Support the `JSON_ARRAY_APPEND` built-in JSON function](https://github.com/pingcap/tidb/pull/9609)

## Improved

- [Set the correlation when loading the needed column histogram](https://github.com/pingcap/tidb/pull/9701)
- [Stabilize the sort order when computing the correlation](https://github.com/pingcap/tidb/pull/9696)
- [Set the new child after injecting the Project operator](https://github.com/pingcap/tidb/pull/9684)
- [Generate `digest` and log it in slow logs](https://github.com/pingcap/tidb/pull/9662)
- [Skip loading the privilege when `skip-grant-table` is enabled](https://github.com/pingcap/tidb/pull/9654)
- [Replace some maps with the switch table to save memory](https://github.com/pingcap/tidb/pull/9650/files?file-filters%5B%5D=.go)
- [Unify the log format in the `planner` package](https://github.com/pingcap/tidb/pull/9630)
- [Update the `SELECT` denied message for the compatibility with MySQL](https://github.com/pingcap/tidb/pull/9627)
- [Update the binlog enabling configuration and add the `tidb_log_bin` system variable](https://github.com/pingcap/tidb/pull/9625)
- [Support `DROP ROLE`](https://github.com/pingcap/tidb/pull/9616)
- [Support `ROLL BACK` for renaming the table, modifying the table charset, and truncating the table partition](https://github.com/pingcap/tidb/pull/9602)
- [Only consider prefix columns in indexes for choosing Index Join](https://github.com/pingcap/tidb/pull/9601)
- [Unify the log format in the `executor` package](https://github.com/pingcap/tidb/pull/9521)
- [Unify the log format in the `expression` package](https://github.com/pingcap/tidb/pull/9507)
- [Refactor the slow log format for the compatibility with the MySQL slow log](https://github.com/pingcap/tidb/pull/9290)
- [Create a SQL bind table during bootstrap](https://github.com/pingcap/tidb/pull/9008)

## Fixed

- [Fix the issue that `last_day` is not compatible with MySQL](https://github.com/pingcap/tidb/pull/9746)
- [Fix the issue that Point Get might miss the unique key if the primary key is also in the condition](https://github.com/pingcap/tidb/pull/9737)
- [Fix the panic when wrapping the cast for the window function](https://github.com/pingcap/tidb/pull/9719)
- [Fix the issue that `str_to_date` is not compatible with MySQL](https://github.com/pingcap/tidb/pull/9693)
- [Fix the issue that `default_week_format` does not work](https://github.com/pingcap/tidb/pull/9685)
- [Fix the `Create Table ... Like` bug when the `refer` table has non-public column or index](https://github.com/pingcap/tidb/pull/9580)
- [Fix an unexpected error caused by `Over`](https://github.com/pingcap/tidb/pull/9567)
- [Correct `ExpectedCnt` for children plans of Join](https://github.com/pingcap/tidb/pull/9497)

# Weekly update in TiSpark

Last week, we landed [6 PRs](https://github.com/pingcap/tispark/pulls?utf8=✓&q=is%3Apr+is%3Amerged+merged%3A2019-03-11..2019-03-17+) in the TiSpark repository.

## Fixed

- [Fix the incorrect default value of the `Timestamp` type due to TiDB upgrade](https://github.com/pingcap/tispark/pull/596)
- [Fix possible `IndexOutOfBoundException` in `KeyUtils`](https://github.com/pingcap/tispark/pull/597)

# Weekly update in TiKV and PD

Last week, we landed [28 PRs](https://github.com/search?p=1&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-03-11..2019-03-17&type=Issues) in the TiKV and PD repositories.

## Added

* [Add an option to decide whether to panic or not when the key exceeds the bound or in the MVCC corruption](https://github.com/tikv/tikv/pull/4362)
* [Implement `replace`](https://github.com/tikv/tikv/pull/4360)
* [Implement `builtin_string` and `instr_binary`](https://github.com/tikv/tikv/pull/4340)
* `BatchExecutor`
    
    - [Add the context for `AsMySQLBool` and remove `BatchExecutorContext`](https://github.com/tikv/tikv/pull/4346)
    - [Implement `AsMySQLBool`](https://github.com/tikv/tikv/pull/4321)

## Improved

* [Remove the unnecessary Copy trait of `Tz` and `EvalConfig`](https://github.com/tikv/tikv/pull/4380)
* [Avoid some copies in the MVCC reader](https://github.com/tikv/tikv/pull/4373)
* [Refactor `ScannerBuilder`](https://github.com/tikv/tikv/pull/4292)
* [Export `jemalloc` statistics to Prometheus](https://github.com/tikv/tikv/pull/4332)
* [Use the address instead of the store ID for metrics](https://github.com/pingcap/pd/pull/1429)
* [Make the heartbeat more reasonable in the simulator](https://github.com/pingcap/pd/pull/1418)
* Importer
    
    - [Wait after `split` before `scatter`](https://github.com/tikv/tikv/pull/4352)
    - [Restrict the memory usage by RocksDB](https://github.com/tikv/tikv/pull/4352)
	- [Do not read the entire SST file into memory](https://github.com/tikv/tikv/pull/4349)
    - [Store the intermediate SST files on the disk instead of memory](https://github.com/tikv/tikv/pull/4348)
    - [Increase the default `region-split-size` to 512 MB](https://github.com/tikv/tikv/pull/4347)

## Fixed

* [Fix the issue about `instr_binary`](https://github.com/tikv/tikv/pull/4353)
* [Allow restart with a `StoreIdent` when the cluster is not bootstrapped](https://github.com/tikv/tikv/pull/4334)

# New contributors (Thanks!)

tidb:

- [jarvys](https://github.com/jarvys)
- [liufuyang](https://github.com/liufuyang)
- [wjhuang2016](https://github.com/wjhuang2016)
- [zyycj](https://github.com/zyycj)

tikv:

- [iosmanthus](https://github.com/iosmanthus)