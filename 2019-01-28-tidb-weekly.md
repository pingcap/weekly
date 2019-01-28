---
title: Weekly update (January 21 ~ January 27, 2019)
date: 2019-01-28
summary: Last week, we landed 22 PRs in the TiDB repository, 1 PR in the TiSpark repository, and 20 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [22 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-01-21..2019-01-27+) in the TiDB repository.

## Added

- [Add a variable to control whether to check MB4 characters in the UTF-8 charset](https://github.com/pingcap/tidb/pull/9175)

## Improved

- [Log failure reasons for `AutoAnalyze`](https://github.com/pingcap/tidb/pull/9178)
- [Log the reason why `AutoAnalyze` is triggered](https://github.com/pingcap/tidb/pull/9176)
- [Improve the message compatibility with MySQL when setting up connections with the server](https://github.com/pingcap/tidb/pull/9140)
- [Improve the syntax error code and message compatibility with MySQL](https://github.com/pingcap/tidb/pull/9103)

## Fixed

- [Use a separate `backoffer` structure for asynchronous commits](https://github.com/pingcap/tidb/pull/9119)
- [Prohibit altering tables from the binary charset to `utf8mb4`](https://github.com/pingcap/tidb/pull/9107)
- [Fix wrong results of queries that contain `any`/`all`](https://github.com/pingcap/tidb/pull/9106)
- [Resolve the charset of table columns correctly](https://github.com/pingcap/tidb/pull/9105)

# Weekly update in TiSpark

Last week, we landed [1 PR](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-01-21..2019-01-27+) in the TiSpark repository.

## Fixed

- [Fix case sensitive configurations](https://github.com/pingcap/tispark/pull/557)

# Weekly update in TiKV and PD

Last week, we landed [20 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-01-21..2019-01-27&type=Issues) in the TiKV and PD repositories.

## Improved

- [Update etcd in PD](https://github.com/pingcap/pd/pull/1414)
- [Make the hot Region scheduler configurable](https://github.com/pingcap/pd/pull/1412)

## Fixed

- [Fix the event listener issue by checking the `CompactionJobInfos` status](https://github.com/tikv/tikv/pull/4126)
- [Fix the `is_point` usage issue in `IndexScanExecutor`](https://github.com/tikv/tikv/pull/4119)
- [Fix the GC state of invalid logs](https://github.com/tikv/tikv/pull/4090)

# New contributors (Thanks!)

tidb:

- [hueypark](https://github.com/hueypark)

tikv:

- [fredchenbj](https://github.com/fredchenbj)

parser:

- [arnkore](https://github.com/arnkore)

docs-cn:

- [tender-boluo](https://github.com/tender-boluo)