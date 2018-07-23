---
title: Weekly update (July 16 ~ July 22, 2018)
date: 2018-07-23
summary: Last week, we landed 41 PRs in the TiDB repositories, 2 PRs in the TiSpark repositories, and 23 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [41 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-07-16..2018-07-22+) in the TiDB repositories.

## Added

- [Support `group_concat` in the new aggregation evaluation framework](https://github.com/pingcap/tidb/pull/7032)
- [Support the remained types (`String`/`Time`/`Duration`/`JSON`) for `Max`/`Min`](https://github.com/pingcap/tidb/pull/7056)
- [Support `FIRST_ROW` in the new aggregation evaluation framework](https://github.com/pingcap/tidb/pull/7057)
- [Support the `admin check table` statement for table partition](https://github.com/pingcap/tidb/pull/7087)
- [Add the proposal template](https://github.com/pingcap/tidb/pull/7090)
- [Add the new storage row format proposal](https://github.com/pingcap/tidb/pull/7095)
- [Add the design document about the new aggregate framework](https://github.com/pingcap/tidb/pull/7097)
- [Set the `PB` field type and the `ExtraHandle` column type](https://github.com/pingcap/tidb/pull/7118)

## Fixed

- [Fix the daylight saving time issue](https://github.com/pingcap/tidb/pull/6823)
- [Fix the panic of creating partition tables](https://github.com/pingcap/tidb/pull/7059)
- [Fix the bug in loading data](https://github.com/pingcap/tidb/pull/7074/files)
- [Fix the OOM issue in the batch operations](https://github.com/pingcap/tidb/pull/7086)
- [Add `keepalive`](https://github.com/pingcap/tidb/pull/7099)
- [Truncate the prefix index from runes when the charset is UTF-8](https://github.com/pingcap/tidb/pull/7109)
- [Check `b.err` located after `buildSort` and `buildLimit` in `builUnion`](https://github.com/pingcap/tidb/pull/7114)
- [Use reference count to keep only one domain instance](https://github.com/pingcap/tidb/pull/7094)

## Improved

- [Speed up executing the `replace into` statement](https://github.com/pingcap/tidb/pull/7027)
- [Handle the error of `mismatch cluster id`](https://github.com/pingcap/tidb/pull/7053)
- [Refactor the index for table partition](https://github.com/pingcap/tidb/pull/7062)
- [Check the partition count limit when creating and adding the partitioned table](https://github.com/pingcap/tidb/pull/7069)
- [Make decoding much faster](https://github.com/pingcap/tidb/pull/7071)

# Weekly update in TiSpark

Last week, we landed [2 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-07-16..2018-07-22) in the TiSpark repositories.

## Improved

- [Improve the error log of the PD connection issue](https://github.com/pingcap/tispark/pull/388)
- [Re-throw the exception when PD initialization fails](https://github.com/pingcap/tispark/pull/392) 

# Weekly update in TiKV and PD

Last week, we landed [23 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-07-16..2018-07-22) in the TiKV and PD repositories.

## Added

- [Create `MAINTAINERS.md`](https://github.com/pingcap/tikv/pull/3306)
- [Record the node version](https://github.com/pingcap/tikv/pull/3319)
- [Support `futures` for the `mpsc` channel](https://github.com/pingcap/tikv/pull/3297)
- [Support Region half-splitting without scan](https://github.com/pingcap/tikv/pull/3310)
- [Add the bottommost level compaction](https://github.com/pingcap/tikv/pull/3273)
- [Add the error code](https://github.com/pingcap/pd/pull/1137)
- [Support Region merging](https://github.com/pingcap/pd/pull/1153)
- [Support the Raft learner in the simulator](https://github.com/pingcap/pd/pull/1151)
- [Add the policy selection for splitting Regions](https://github.com/pingcap/pd/pull/1149)

## Fixed

- [Fix the template permissions](https://github.com/pingcap/tikv/pull/3328)
- [Fix the bug in `from_bytes`](https://github.com/pingcap/tikv/pull/3240)
- [Handle the non-integer input for bit related functions](https://github.com/pingcap/tikv/pull/3324)
- [Fix hot Write and Read cases](https://github.com/pingcap/pd/pull/1150)

## Improved

- [Enable `prevote` by default](https://github.com/pingcap/tikv/pull/3289)
- [Collapse continuous rollbacks](https://github.com/pingcap/tikv/pull/3290)
- [Check sensitive environment variables](https://github.com/pingcap/tikv/pull/3329)
- [Add a custom log formatter](https://github.com/pingcap/tikv/pull/3269)
- [Refactor `ClusterInfo`](https://github.com/pingcap/pd/pull/1147)
- [Improve the taint cache behavior](https://github.com/pingcap/pd/pull/1142)