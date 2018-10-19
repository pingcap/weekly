---
title: Weekly update (May 21 ~ May 27, 2018)
date: 2018-05-28
summary: Last week, we landed 44 PRs in the TiDB repositories, 2 PRs in the TiSpark repositories, and 20 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [44 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-05-21..2018-05-27) in the TiDB repositories.

## Added

- [Make `tidb_max_chunk_size` a global variable](https://github.com/pingcap/tidb/pull/6585)
- [Add a timeout for writing binlogs](https://github.com/pingcap/tidb/pull/6587)
- [Support `high_priority` for `DELETE`/`UPDATE`/`REPLACE INTO` statements](https://github.com/pingcap/tidb/pull/6592)
- [Support changing the log level online](https://github.com/pingcap/tidb/pull/6604)
- [Support `ComChangeUser`](https://github.com/pingcap/tidb/pull/6623)
- [Support `JOIN` hint for `UPDATE`/`DELETE` statements](https://github.com/pingcap/tidb/pull/6626)

## Fixed

- [Fix the compatibility problem of `ON UPDATE CURRENT_TIMESTAMP`](https://github.com/pingcap/tidb/pull/6567)
- [Fix a bug of `ON DUPLICATE KEY UPDATE`](https://github.com/pingcap/tidb/pull/6589)
- [Fix the decimal fraction of `DIV`](https://github.com/pingcap/tidb/pull/6590)
- [Fix count estimation of `betweenRowCount`](https://github.com/pingcap/tidb/pull/6596)
- [Fix the wrong result of `CEIL(DECIMAL)`](https://github.com/pingcap/tidb/pull/6598)
- [Fix the wrong result of `CEIL(INT)` integer](https://github.com/pingcap/tidb/pull/6606)
- [Fix the cost estimation of `Index Scan` and `Table Scan`](https://github.com/pingcap/tidb/pull/6608)
- [Fix a bug of deleting an index in `YEAR` type](https://github.com/pingcap/tidb/pull/6611)
- [Fix the wrong result of `FLOOR`](https://github.com/pingcap/tidb/pull/6620)
- [Fix the false alarm of `ADMIN CHECK TABLE`](https://github.com/pingcap/tidb/pull/6625)
- [Fix a panic of `MAX`/`MIN`](https://github.com/pingcap/tidb/pull/6632)
- [Fix a bug in `rebuildRange` when the plan cache for the `PREPARE` statement is enabled](https://github.com/pingcap/tidb/pull/6637)

## Improved

- [Create a new `backoff` for each Region](https://github.com/pingcap/tidb/pull/6438/files)
- [Do not log the Write error during handshake](https://github.com/pingcap/tidb/pull/6605)
- [Refine the log level of `stats`](https://github.com/pingcap/tidb/pull/6627)
- [Set the rollback log to the `debug` level](https://github.com/pingcap/tidb/pull/6653)
- [Refine the comparison between the timestamp column and the string constant](https://github.com/pingcap/tidb/pull/6621)
- [Push `CEIL` down to TiKV](https://github.com/pingcap/tidb/pull/6607)

# Weekly update in TiSpark

Last week, we landed [2 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-05-21..2018-05-27) in the TiSpark repositories.

## Fixed

- [Fix incorrect histogram `totalRowCount`](https://github.com/pingcap/tispark/pull/353)

## Improved

- [Improve the `tidbMapTable` logic](https://github.com/pingcap/tispark/pull/350)

# Weekly update in TiKV and PD

Last week, we landed [20 PRs](https://github.com/search?p=1&q=repo:pingcap/tikv+repo:pingcap/pd+is:pr+is:merged+merged:2018-05-21..2018-05-27&type=Issues&utf8=%E2%9C%93) in the TiKV and PD repositories.

## Added

- [Encode and decode for arrow chunk](https://github.com/pingcap/tikv/pull/3001)

## Fixed

- [Implement GC on the stale learner automatically](https://github.com/pingcap/tikv/pull/3091)
- [Allow Snapshot to remove only the temporary files created by itself](https://github.com/pingcap/tikv/pull/3094)
- [Fix the panic issue when collecting hot-cache metrics](https://github.com/pingcap/pd/pull/1091)

## Improved

- [Remove the Read trait from the decoding function of bytes](https://github.com/pingcap/tikv/pull/3062)
- [Remove the Read trait from the decoding function of decimals](https://github.com/pingcap/tikv/pull/3071)
- [Remove the Read trait from the decoding function of JSON](https://github.com/pingcap/tikv/pull/3081)

# New contributors (Thanks!)

PD: 

- [goerzh](https://github.com/goerzh)
- [shilicqupt](https://github.com/shilicqupt)