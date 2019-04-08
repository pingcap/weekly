---
title: Weekly update (April 01 ~ April 07, 2019)
date: 2019-04-08
summary: Last week, we landed 61 PRs in the TiDB repository, 9 PRs in the TiSpark repository, and 21 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [61 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-04-01..2019-04-07+) in the TiDB repository.

## Improved

- [Improve the unit test coverage of `util/set` from 0% to 100%](https://github.com/pingcap/tidb/pull/10057)
- [Support a fast `Analyze` session control variable](https://github.com/pingcap/tidb/pull/10039)
- [Improve the error message for connection closing](https://github.com/pingcap/tidb/pull/10034)
- [Remove the `errors.Trace` call in some high-level packages to improve the performance](https://github.com/pingcap/tidb/pull/10033)
- [Correct the estimated row count for the inner plan of `IndexJoin`](https://github.com/pingcap/tidb/pull/10015)
- [Replace lock operations in `MemTracker` with atomic operations to improve the performance](https://github.com/pingcap/tidb/pull/10005)
- [Improve the unit test coverage of `executor/aggfuncs` from 47.7% to 70%](https://github.com/pingcap/tidb/pull/10002)
- [Improve the unit test coverage of `global_vars_cache` from 0% to 100%](https://github.com/pingcap/tidb/pull/9919)
- [Raise a warning for unmatched Join hint in some cases](https://github.com/pingcap/tidb/pull/9914)
- [Improve the unit test coverage of `infoschema` from 65.20% to 85.2%](https://github.com/pingcap/tidb/pull/9898)
- [Push down constant filters over Join properly](https://github.com/pingcap/tidb/pull/9848)
- [Allow `kill tidb [session id]` to stop executors and release resources quickly](https://github.com/pingcap/tidb/pull/9844)
- [Improve the performance of computing `FieldType.Flen` of `int64`/`uint64`](https://github.com/pingcap/tidb/pull/9726)
- [Make `TableReader&IndexReader&IndexLookup` support the chunk size control](https://github.com/pingcap/tidb/pull/9452)

## Fixed

- [Fix the issue that `Desc table` is incompatible with MySQL in some cases](https://github.com/pingcap/tidb/pull/10022)
- [Fix the issue that `JSON_contains_path` is incompatible with MySQL](https://github.com/pingcap/tidb/pull/9992)
- [Fix the issue that the `dayname` function is incompatible with MySQL when doing arithmetic](https://github.com/pingcap/tidb/pull/9975)
- [Fix wrong results of `group_concat` in some cases](https://github.com/pingcap/tidb/pull/9967)
- [Fix the data race issue in `config.TreatOldVersionUTF8AsUTF8MB4`](https://github.com/pingcap/tidb/pull/9960)
- [Fix incorrect time fraction parsing method](https://github.com/pingcap/tidb/pull/9933)
- [Fix wrong results of `count(distinct)`/`sum(distinct)` of decimal columns in some cases](https://github.com/pingcap/tidb/pull/9913)
- [Make the `Alter` and `Rename` privileges the same with MySQL](https://github.com/pingcap/tidb/pull/9872)
- [Fix the `Alter` table charset bug and compatibility in some cases](https://github.com/pingcap/tidb/pull/9790)
- [Fix the read-only check for the `Prepare`/`Execute` statement](https://github.com/pingcap/tidb/pull/9723)
- [Fix improper using of the time zone in checking default column values](https://github.com/pingcap/tidb/pull/9578)

# Weekly update in TiSpark

Last week, we landed [9 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-04-01..2019-04-07+) in the TiSpark repository.

## Added

- [Support range partition pruning](https://github.com/pingcap/tispark/pull/599)

## Fixed

- [Fix the issue that `ManagedChannel` is not closed in the test](https://github.com/pingcap/tispark/pull/624)

# Weekly update in TiKV and PD

Last week, we landed [21 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-04-01..2019-04-07&type=Issues) in the TiKV and PD repositories.

## Added

* [Add the execution summary framework](https://github.com/tikv/tikv/pull/4433)
* [Introduce the vectorized evaluation framework](https://github.com/tikv/tikv/pull/4322)
* [Add one more configuration option for very fast builds](https://github.com/tikv/tikv/pull/4458)
* [Make `end-point-enable-batch-if-possible` configurable](https://github.com/tikv/tikv/pull/4472)
* [Use static metrics for `KV_COMMAND_COUNTER`](https://github.com/tikv/tikv/pull/4442)
* [Enlarge the `ingest` buffer](https://github.com/tikv/tikv/pull/4464)

## Fixed

* [Fix the performance bug](https://github.com/tikv/tikv/pull/4484)
* [Improve the Region heartbeat](https://github.com/pingcap/pd/pull/1489)
* [Fix the issue that the Region scatter might transfer the leader to a removed peer](https://github.com/pingcap/pd/pull/1482)

# New contributors (Thanks!)

tidb:

* [Debiancc](https://github.com/Debiancc)

tikv: 

* [myguyy](https://github.com/myguyy)
* [seansu4you87](https://github.com/seansu4you87)
* [yaalsn](https://github.com/yaalsn)

pd:

* [yaalsn](https://github.com/yaalsn)

parser:

* [wuudjac](https://github.com/wuudjac)