---
title: Weekly update (December 11 ~ December 17, 2017)
date: 2017-12-18
summary: Last week, we landed 46 PRs in the TiDB repositories, 10 PRs in the TiSpark repositories, and 14 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [46 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is:pr%20is:merged%20merged:2017-12-11..2017-12-17) in the TiDB repositories.

## Added

* [Support `SEPARATOR` in the `group_concat` aggregate function.](https://github.com/pingcap/tidb/pull/5420)
* [Support the `BinaryJSON` type.](https://github.com/pingcap/tidb/pull/5404)
* [Add a config for the SQL parser to enable parsing syntax for window function.](https://github.com/pingcap/tidb/pull/5365)
* [Support the http index MVCC interface.](https://github.com/pingcap/tidb/pull/5304)

## Fixed

* [Show the index column length if necessary in `show create table` statement.](https://github.com/pingcap/tidb/pull/5414)
* [Clear the delta info when rolling back a transaction.](https://github.com/pingcap/tidb/pull/5390)
* [Only set `defaultValues` in aggregation push down.](https://github.com/pingcap/tidb/pull/5383)
* [Fix a bug when applying meets index `join`.](https://github.com/pingcap/tidb/pull/5381)

## Improved

* [Support analyzing all indices statements.](https://github.com/pingcap/tidb/pull/5403)
* [Load timezone from TiKV when starting a new session.](https://github.com/pingcap/tidb/pull/5393)
* [Support `date_format` push down.](https://github.com/pingcap/tidb/pull/5386)
* [`NewIndexLookUpJoin` executor for `Chunk`.](https://github.com/pingcap/tidb/pull/5382)
* [Attach the `requiredProp` info to physical plans.](https://github.com/pingcap/tidb/pull/5378)
* [Support `tls` connection to pd and tikv.](https://github.com/pingcap/tidb/pull/5311)
* Support `Chunk` in executors: 
    - [`DDLExec`](https://github.com/pingcap/tidb/pull/5417)
    - [`CancelDDLJobsExec`](https://github.com/pingcap/tidb/pull/5416)
    - [`ShowDDLExec`](https://github.com/pingcap/tidb/pull/5415)
    - [`PrepareExec`](https://github.com/pingcap/tidb/pull/5408)
    - [`CheckTableExec`](https://github.com/pingcap/tidb/pull/5407)
    - [`SelectLockExec`](https://github.com/pingcap/tidb/pull/5399)
    - [`ExplainExec`](https://github.com/pingcap/tidb/pull/5398)
    - [`SetExecutor`](https://github.com/pingcap/tidb/pull/5397)
    - [`ExistsExec`](https://github.com/pingcap/tidb/pull/5396)
    - [`UpdateExec`](https://github.com/pingcap/tidb/pull/5372)
    - [`JoinResultGenerator`](https://github.com/pingcap/tidb/pull/5357)

# Weekly update in TiSpark

Last week, we landed [10 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2017-12-11..2017-12-17) in the TiSpark repositories.

## Fixed

* [Fix the PD cache invalidation not synced for the TiSpark side.](https://github.com/pingcap/tispark/pull/123)
* [Fix the Region Request failure not synced with the TiSpark driver.](https://github.com/pingcap/tikv-client-lib-java/pull/189)
* [Fix the inconsistent datatype mapping for `Datetime` type.](https://github.com/pingcap/tikv-client-lib-java/pull/190)
* [Fix inconsistent datatype mapping for `DOUBLE` type.](https://github.com/pingcap/tikv-client-lib-java/pull/191)
* [Fix not printing index name in plan.](https://github.com/pingcap/tikv-client-lib-java/pull/192)
* [Fix the schema change that causes a SQL failure.](https://github.com/pingcap/tikv-client-lib-java/pull/197)
* [Fix inconsistency of the timestamp unit.](https://github.com/pingcap/tispark/pull/135)

# Weekly update in TiKV and PD

Last week, we landed [14 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-12-11..2017-12-17) in the TiKV and PD repositories.

## Added

* [Coprocessor: support `date_format`.](https://github.com/pingcap/tikv/pull/2503)
* [Pd/Client: support `get_region_info`.](https://github.com/pingcap/tikv/pull/2534)
* [Worker: add pending capacity.](https://github.com/pingcap/tikv/pull/2560)
* [Storage: add more fail points.](https://github.com/pingcap/tikv/pull/2569)

## Fixed

* [Tests: use the same RocksDB configuration as production.](https://github.com/pingcap/tikv/pull/2572)
* [PD: fix the stale region info when overlapping.](https://github.com/pingcap/pd/pull/880)
* [PD: fix `tls` for `join`.](https://github.com/pingcap/pd/pull/888)
* [PD: fix the panic that the cluster status is nil.](https://github.com/pingcap/pd/pull/889)

## Improved

* [Update Prometheus.](https://github.com/pingcap/tikv/pull/2579)
* [Use the lower case of `logrus`.](https://github.com/pingcap/pd/pull/886)
* [Correct a typo.](https://github.com/pingcap/tikv/pull/2584)