---
title: Weekly update (June 24 ~ June 30, 2019)
date: 2019-07-01
summary: Last week, we landed 52 PRs in the TiDB repository, 9 PRs in the TiSpark repository, and 38 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [52 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-06-24..2019-06-30+) in the TiDB repository.

## Added

- [Add support for `MAX_EXECUTION_TIME`](https://github.com/pingcap/tidb/pull/10541)
- [Add a check for the GC life time that is too short](https://github.com/pingcap/tidb/pull/10936)
- [Add an HTTP API to get some information of the sub-optimal query](https://github.com/pingcap/tidb/pull/10717)
- [Add support for mysqldump from MySQL 8.0](https://github.com/pingcap/tidb/pull/10829)

## Improved

- [Relax the restrictions of `trace format='row'`](https://github.com/pingcap/tidb/pull/10979)
- [Make auto-increment ID adjustable](https://github.com/pingcap/tidb/pull/10978)
- [Lock the key in the Point Get executor for pessimistic transactions](https://github.com/pingcap/tidb/pull/10972)
- [Set up connection information in the session when the audit plugin is enabled](https://github.com/pingcap/tidb/pull/10923)
- [Do not change the DDL lease during the bootstrap process](https://github.com/pingcap/tidb/pull/10908)
- [Support `IF EXISTS`/`IF NOT EXISTS` for some DDL operations](https://github.com/pingcap/tidb/pull/10723)
- [Fix the `MAX_EXECUTION_TIME` SQL hint and a global variable](https://github.com/pingcap/tidb/pull/10963)

## Fixed

- [Fix the `show create table` output for generated columns](https://github.com/pingcap/tidb/pull/9608)
- [Fix the bug of saving the GC safe point in PD before doing distributed GC](https://github.com/pingcap/tidb/pull/10927)
- [Let `baseFuncDesc.typeInfer` return an error instead of triggering a panic](https://github.com/pingcap/tidb/pull/10910)

# Weekly update in TiSpark

Last week, we landed [9 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-06-24..2019-06-30+) in the TiSpark repository.

## Fixed

- [Fix the column size estimation issue](https://github.com/pingcap/tispark/pull/858)
- [Fix the incorrect timestamp of `tidbMapDatabase`](https://github.com/pingcap/tispark/pull/862)
- [Fix the issue that the Region and Store information do not come from the same `RegionTask`](https://github.com/pingcap/tispark/pull/869)

# Weekly update in TiKV and PD

Last week, we landed [38 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-06-24..2019-06-30&type=Issues) in the TiKV and PD repositories.

## Improved

- [Only debug log outputs when batch execution cannot be utilized](https://github.com/tikv/tikv/pull/4985)
- [Print the pd-ctl success response message](https://github.com/pingcap/pd/pull/1600)
- [Tolerate a backslash in the label name](https://github.com/pingcap/pd/pull/1595)
- [Move duplicated code into the existing macro](https://github.com/tikv/tikv/pull/4955)
- [Refine the deadlock](https://github.com/tikv/tikv/pull/4932)
- [Output most keys in the hex format](https://github.com/tikv/tikv/pull/4921)

## Added

- [Add an option about the gRPC gateway](https://github.com/pingcap/pd/pull/1596)
- [Add some metrics to Coprocessor](https://github.com/tikv/tikv/pull/4959)

## Fixed

- [Fix some bugs in date time processing](https://github.com/tikv/tikv/pull/4918)
- [Fix multiple double panics in the drop path with the added `safe_panic` macro](https://github.com/tikv/tikv/pull/4552)
- [Fix the upgrade problem caused by `TwoWayMerge`](https://github.com/pingcap/pd/pull/1602)
- [Fix a pd-ctl subcommand option](https://github.com/pingcap/pd/pull/1582)

# New contributor (Thanks!)

tikv: [uvd](https://github.com/uvd)