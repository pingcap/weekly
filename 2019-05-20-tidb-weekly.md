---
title: Weekly update (May 13 ~ May 19, 2019)
date: 2019-05-20
summary: Last week, we landed 37 PRs in the TiDB repository, 19 PRs in the TiSpark repository, and 24 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [37 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-05-13..2019-05-19+) in the TiDB repository.

## Added

- [Implement `ALTER DATABASE` to alter the charset/collation](https://github.com/pingcap/tidb/pull/10393)
- [Support the `incremental` and `repeats` importer comments](https://github.com/pingcap/tidb/pull/10434)

## Improved

- [Disable the new `@@wait_timeout` feature](https://github.com/pingcap/tidb/pull/10441)
- [Improve the package test code coverage to above 85% in `util/codec`](https://github.com/pingcap/tidb/pull/10351)
- [Make the `resolveLock` phase of GC concurrent to improve its speed](https://github.com/pingcap/tidb/pull/10379)
- [Always set `isPessimisticLock` in the request for pessimistic transactions](https://github.com/pingcap/tidb/pull/10451)
- [Use multiple indexes to scan a table if possible](https://github.com/pingcap/tidb/pull/10121)
- [Refine transaction retry error messages](https://github.com/pingcap/tidb/pull/10466)
- [Reduce the wait backoff time when the lock has expired](https://github.com/pingcap/tidb/pull/10006)

## Fixed

- [Fix a time format error in `ParseSlowLog`](https://github.com/pingcap/tidb/pull/10526)
- [Fix the issue that the `RANGE` frame has no `ORDER BY` clause in the `Window` function](https://github.com/pingcap/tidb/pull/10496)
- [Fix the inconsistency problem by prohibiting modifying decimal precision](https://github.com/pingcap/tidb/pull/10433)
- [Fix a bug when an unsigned histogram meets signed ranges in the feedback](https://github.com/pingcap/tidb/pull/10415)
- [Fix the issue that `period_diff` is not compatible with MySQL 8.0](https://github.com/pingcap/tidb/pull/10383)
- [Fix the wrong range calculation for the `CHAR` column](https://github.com/pingcap/tidb/pull/10124)
- [Fix the issue that the type of the `add_date` result is not compatible with MySQL](https://github.com/pingcap/tidb/pull/9830)
- [Fix the float overflow issue when converting a decimal to a float and then converting a float to an uint](https://github.com/pingcap/tidb/pull/10405)

# Weekly update in TiSpark

Last week, we landed [19 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-05-13..2019-05-19+) in the TiSpark repository.

## Fixed

- [Fix the concurrent `dagRequest` issue](https://github.com/pingcap/tispark/pull/714)
- [Fix the behavior of downgrading to a table scan when performing an index scan](https://github.com/pingcap/tispark/pull/725)

# Weekly update in TiKV and PD

Last week, we landed [24 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-05-13..2019-05-19&type=Issues) in the TiKV and PD repositories.

## Added

* [Add the `explain analyze` support for the aggregation executor](https://github.com/tikv/tikv/pull/4715)
* [Add the summary support for the Top-N executor](https://github.com/tikv/tikv/pull/4710)
* [Set timeout for `MoveLeader`](https://github.com/pingcap/pd/pull/1538)
* [Support the execution summary for the selection executor](https://github.com/tikv/tikv/pull/4699)
* [Add the `ScanRegions` gRPC protocol in PD](https://github.com/pingcap/pd/pull/1535)

## Fixed

* [Do not collect requests that read indexes during transferring the leader](https://github.com/tikv/tikv/pull/4688)
* [Reject transferring the leader when the Region's configuration is recently changed](https://github.com/tikv/tikv/pull/4684)

## Improved

* [Handle system commands in the high priority pool](https://github.com/tikv/tikv/pull/4679)
* [Make most ticks lazy in TiKV](https://github.com/tikv/tikv/pull/4655)
* [Use `tokio_threadpool` for the transaction scheduler](https://github.com/tikv/tikv/pull/4628)
* [Speed up Docker building and remove unused files](https://github.com/tikv/tikv/pull/4590)

# New contributors (Thanks!)

tikv:

- [andrisak](https://github.com/andrisak)

tidb:

- [hailanwhu](https://github.com/hailanwhu)
- [jzdxeb](https://github.com/jzdxeb)

docs-cn:

- [spongedu](https://github.com/spongedu)
