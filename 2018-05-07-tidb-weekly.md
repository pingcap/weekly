---
title: Weekly update (April 30 ~ May 06, 2018)
date: 2018-05-07
summary: Last week, we landed 24 PRs in the TiDB repositories, 1 PR in the TiSpark repositories, and 15 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [24 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-04-30..2018-05-06+) in the TiDB repositories.

## Added

- [Add `DB_NAME` and `TABLE_NAME` in the result of `ADMIN SHOW DDL JOBS`](https://github.com/pingcap/tidb/pull/6276)
- [Add an HTTP API to scatter Regions of a table](https://github.com/pingcap/tidb/pull/6378)
- [Add the `tidb_retry_limit` session variable to control the transaction retry limit](https://github.com/pingcap/tidb/pull/6369)
- [Add the `auto_analyze_ratio` session variable to control the automatic analysis ratio](https://github.com/pingcap/tidb/pull/6455)
- [Support the `ALTER TABLE FORCE` syntax](https://github.com/pingcap/tidb/pull/6476)

## Fixed

- [Restrict the column type in range partition](https://github.com/pingcap/tidb/pull/6339)
- [Check the privilege for `SHOW CREATE TABLE` and `information_schema.tables`](https://github.com/pingcap/tidb/pull/6426)
- [Check `nil` for Coprocessor stream response](https://github.com/pingcap/tidb/pull/6467)
- [Set the index name of `ADMIN CHECK INDEX` to be case insensitive](https://github.com/pingcap/tidb/pull/6477)

## Improved

- [Reduce the memory usage for duplicated key update](https://github.com/pingcap/tidb/pull/6337)
- [Add the reorganization log to make trouble shooting easier](https://github.com/pingcap/tidb/pull/6428)
- [Add failure metrics for `checkLeader` and `prepare`](https://github.com/pingcap/tidb/pull/6452)

# Weekly update in TiSpark

Last week, we landed [1 PR](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-04-30..2018-05-06) in the TiSpark repositories.

## Fixed

- [Fix the TopN validation issue](https://github.com/pingcap/tispark/pull/343)

# Weekly update in TiKV and PD

Last week, we landed [15 PRs](https://github.com/search?p=2&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-04-30..2018-05-06&type=Issues&utf8=%E2%9C%93) in the TiKV and PD repositories.

## Added

- [Support compacting the whole cluster](https://github.com/pingcap/tikv/pull/2945)
- [Scatter the leader distribution in a specified range](https://github.com/pingcap/pd/pull/1037)

## Fixed

- [Resign the PD leader when it is not the same as the etcd leader](https://github.com/pingcap/pd/pull/1039)
- [Fix the parse error of `config.toml`](https://github.com/pingcap/pd/pull/1043)
- [Fix the bug of deleting the valid scheduler when starting the coordinator](https://github.com/pingcap/pd/pull/1045)

## Improved

- [Attach an interval to Region heartbeats](https://github.com/pingcap/tikv/pull/2965)
- [Open the `nightly` feature gate for crossbeam-channel](https://github.com/pingcap/tikv/pull/2995)
- [Upgrade etcd to v3.3.4](https://github.com/pingcap/pd/pull/1046)
