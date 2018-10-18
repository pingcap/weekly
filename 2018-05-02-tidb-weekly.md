---
title: Weekly update (April 23 ~ April 29, 2018)
date: 2018-05-02
summary: Last week, we landed 49 PRs in the TiDB repositories, 18 PRs in the TiSpark repositories, and 21 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [49 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-04-23..2018-04-29) in the TiDB repositories.

## Added

- [Add the `CHANGELOG.md` file to the TiDB repository](https://github.com/pingcap/tidb/pull/6402)
- [Support more `ODBC` syntaxes](https://github.com/pingcap/tidb/pull/6399)
- [Support `PARTITION BY RANGE COLUMNS` in `SHOW CREATE TABLE`](https://github.com/pingcap/tidb/pull/6332)
- [Support the `ALTER CONVERT TO` syntax](https://github.com/pingcap/tidb/pull/6416)
- [Support the `ALTER TABLE AUTO_INCREMENT` syntax](https://github.com/pingcap/tidb/pull/6417)
- [Support the `SET NAMES COLLATE DEFAULT` syntax](https://github.com/pingcap/tidb/pull/6404)

## Fixed

- [Fix `Dump`/`Load` statistics information](https://github.com/pingcap/tidb/pull/6285)
- [Fix data race on the `LockKeys()` function](https://github.com/pingcap/tidb/pull/6340)
- [Fix range calculating in the `TableHandlesToKVRanges()` function](https://github.com/pingcap/tidb/pull/6364)
- [Fix the compatibility problem of the `UNION` statement](https://github.com/pingcap/tidb/pull/6370)
- [Fix the wrong behavior of the `tryToGetMemTask()` function](https://github.com/pingcap/tidb/pull/6390)
- [Refine the optimization rule of "TopN Push Down"](https://github.com/pingcap/tidb/pull/6407)

## Improved

- [Add more log information about slow queries](https://github.com/pingcap/tidb/pull/6343)
- [Log the slow Coprocessor task in detail](https://github.com/pingcap/tidb/pull/6344)
- [Enhance the validation of column names when creating a table](https://github.com/pingcap/tidb/pull/6349)

# Weekly update in TiSpark

Last week, we released TiSpark 1.0 GA and landed [18 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-04-23..2018-04-29) in the TiSpark repositories.

## Fixed

- [Fix the leaky session](https://github.com/pingcap/tispark/pull/334)
- [Fix the unsigned index](https://github.com/pingcap/tispark/pull/332)
- [Fix the logic of handling the stale epoch error](https://github.com/pingcap/tispark/pull/325)
- [Fix the logic of handling zero store ID](https://github.com/pingcap/tispark/pull/324)
- [Fix the `map single table` method](https://github.com/pingcap/tispark/pull/319)

## Improved

- [Allow forcing the metadata to refresh](https://github.com/pingcap/tispark/pull/330)
- [Adjust the retry policy factor and cache invalidation](https://github.com/pingcap/tispark/pull/326)

# Weekly update in TiKV and PD

Last week, we landed [21 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-04-23..2018-04-29) in the TiKV and PD repositories.

## Added

- [Add the change log for TiKV](https://github.com/pingcap/tikv/pull/2952)
- [Add the change log for 2.0 GA](https://github.com/pingcap/pd/pull/1038)
- [Add metrics for hotspot cache](https://github.com/pingcap/pd/pull/1027)
- [Do fuzz test](https://github.com/pingcap/tikv/pull/2942)

## Fixed

- [Improve the Key Scan feature and fix a bug for MVCC](https://github.com/pingcap/tikv/pull/2964)

## Improved

- [Refine the installation instructions](https://github.com/pingcap/pd/pull/1041)
- [Collect Raft's log](https://github.com/pingcap/tikv/pull/2996)
- [Adjust `clean_stale_peer_delay`](https://github.com/pingcap/tikv/pull/2990)
- [Merge `(RAW)KV_COMMAND_COUNTER` into `COMMAND_COUNTER`](https://github.com/pingcap/tikv/pull/2973)
- [Release the log cache eagerly using GC ](https://github.com/pingcap/tikv/pull/2962)