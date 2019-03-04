---
title: Weekly update (February 25 ~ March 03, 2019)
date: 2019-03-04
summary: Last week, we landed 63 PRs in the TiDB repository, 2 PRs in the TiSpark repository, and 36 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [63 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-02-25..2019-03-03) in the TiDB repository.

## Added

- [Support the `RANK` and `DENSE_RANK` window functions](https://github.com/pingcap/tidb/pull/9500)
- [Add the `CREATE ROLE` support](https://github.com/pingcap/tidb/pull/9461)
- [Support range framed window functions](https://github.com/pingcap/tidb/pull/9450)
- [Compute and store the column order correlation with a handle](https://github.com/pingcap/tidb/pull/9315)

## Improved

- [Improve the performance of parsing date formatted values](https://github.com/pingcap/tidb/pull/9516)
- [Improve the compatibility of modifying the column charset with MySQL](https://github.com/pingcap/tidb/pull/9480)
- [Restrict the adjusting factor for the index feedback](https://github.com/pingcap/tidb/pull/9445)
- [Control the chunk size for the selection and projection operators](https://github.com/pingcap/tidb/pull/9398)
- [Handle default values for generated columns when adding an index](https://github.com/pingcap/tidb/pull/9371)
- [Only cast aggregation's argument types when necessary](https://github.com/pingcap/tidb/pull/9340)
- [Add the error count limit for DDL jobs](https://github.com/pingcap/tidb/pull/9295)
- [Disallow generated columns to refer to columns with the `AUTO_INCREMENT` flag](https://github.com/pingcap/tidb/pull/9234)
- [Reduce lock contention of the statistics collector](https://github.com/pingcap/tidb/pull/9233)
- [Write the binlog record when the DDL job state is `done`](https://github.com/pingcap/tidb/pull/9207)
- [Check the column field length when adding a column](https://github.com/pingcap/tidb/pull/9143)

## Fixed

- [Fix the rollback logic for the `LOAD DATA` statement](https://github.com/pingcap/tidb/pull/9444)
- [Fix the wrong default value for time columns](https://github.com/pingcap/tidb/pull/9488)
- [Only show valid columns in `SHOW stats_histograms`](https://github.com/pingcap/tidb/pull/9487)
- [Fix a timezone misusage bug when converting the timestamp constant expression to the protobuf](https://github.com/pingcap/tidb/pull/9473)
- [Fix the infinite retry issue when the sleep time is larger than `max-txn-time`](https://github.com/pingcap/tidb/pull/9454)
- [Remove correlated columns from the items of the `ORDER BY` clause](https://github.com/pingcap/tidb/pull/9435)
- [Only read the transaction buffer for dirty rows in `UnionScan`](https://github.com/pingcap/tidb/pull/9428)
- [Fix a bug of modifying the column flag from `null` to `not null`](https://github.com/pingcap/tidb/pull/9427)
- [Refine `Compare` methods of Merge Join to avoid incorrect results](https://github.com/pingcap/tidb/pull/9390)
- [Fix wrong behaviors of `PREPARE` and `EXECUTE`](https://github.com/pingcap/tidb/pull/9204)
- [Make Semi Join null- and empty-aware](https://github.com/pingcap/tidb/pull/9051)
- [Fix a wrong result of `UnionScan` on partitioned tables](https://github.com/pingcap/tidb/pull/8871)

# Weekly update in TiSpark

Last week, we landed [2 PRs](https://github.com/pingcap/tispark/pulls?utf8=✓&q=is%3Apr+is%3Amerged+merged%3A2019-02-25..2019-03-03+) in the TiSpark repository.

## Improved

- [Skip `LockResolverTest` when the PD client is not present](https://github.com/pingcap/tispark/pull/579)

# Weekly update in TiKV and PD

Last week, we landed [36 PRs](https://github.com/search?p=1&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-02-25..2019-03-03&type=Issues) in the TiKV and PD repositories.

## Added

* [Add thread context switch metrics](https://github.com/tikv/tikv/pull/4282)
* [Add a command line parameter to specify the metrics push address](https://github.com/tikv/tikv/pull/4279)
* [Add the encryption support for Importer](https://github.com/tikv/tikv/pull/4278)
* [Add `make audit`](https://github.com/tikv/tikv/pull/4265)
* [Add metrics for the key exceeding bound](https://github.com/tikv/tikv/pull/4255)
* [Add the batch executor interface](https://github.com/tikv/tikv/pull/4241)

## Improved

* [Use the `dyn` keyword for traits objects](https://github.com/tikv/tikv/pull/4217)
* [Direct the local reader for raw read](https://github.com/tikv/tikv/pull/4222)
* [Remove the Tokio runtime](https://github.com/tikv/tikv/pull/4256)
* [Implement encoding functions for `VectorValue` and `LazyBatchColumn(Vec)`](https://github.com/tikv/tikv/pull/4215)

## Fixed

* [Fix the encrypted file generated issue](https://github.com/tikv/tikv/pull/4296)
* [Fix the scatter range NPE when getting `storeInfo` of a non-existing store](https://github.com/pingcap/pd/pull/1439)
* [Fix the issue of getting tombstone stores](https://github.com/tikv/tikv/pull/4223)
* [Fix the merge panic when receiving multiple snapshots](https://github.com/tikv/tikv/pull/4198)
* [Fix range properties](https://github.com/tikv/tikv/pull/4174)

# New contributors (Thanks!)

tidb:

- [guilhermehubner](https://github.com/guilhermehubner)

tikv:

- [crlf0710](https://github.com/crlf0710)
