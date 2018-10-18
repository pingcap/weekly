---
title: Weekly update (September 10 ~ September 16, 2018)
date: 2018-09-17
summary: Last week, we landed 35 PRs in the TiDB repository, 1 PR in the TiSpark repository, and 28 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [35 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-09-10..2018-09-16+) in the TiDB repository.

## Added

* [Add a design document for TiDB cluster's system timezone](https://github.com/pingcap/tidb/pull/7656)
* [Support resigning the DDL owner and use the `ddl`/`owner`/`resign` HTTP method](https://github.com/pingcap/tidb/pull/7649)
* [Write system timezone into the `MYSQL.TIDB` table in the bootstrap stage](https://github.com/pingcap/tidb/pull/7638)
* [Add two built-in functions `decode` and `encode`](https://github.com/pingcap/tidb/pull/7622)
* [Add a proposal document for a `Volcano/Cascades` model based SQL planner](https://github.com/pingcap/tidb/pull/7543)

## Improved

* [Make the decimal default precision visible in `SHOW CREATE TABLE`](https://github.com/pingcap/tidb/pull/7667)
* [Use the `pumps` client to write binlog files](https://github.com/pingcap/tidb/pull/7659)
* [Improve the error message of GC life time](https://github.com/pingcap/tidb/pull/7658)
* [Fill the data length fields for `INFORMATION_SCHEMA.TABLES`](https://github.com/pingcap/tidb/pull/7657)
* [Support more built-in JSON functions](https://github.com/pingcap/tidb/pull/7651)
* [Refactor the `INFORMATION_SCHEMA.CHARSETS` and `INFORMATION_SCHEMA.COLLATIONS` tables](https://github.com/pingcap/tidb/pull/7647)
* [Register the metrics when TiDB starts up](https://github.com/pingcap/tidb/pull/7642)
* [Store topN slow queries in the `domain` package](https://github.com/pingcap/tidb/pull/7646)
* [Split `property` related code into a single package](https://github.com/pingcap/tidb/pull/7630)
* [Reduce the interval for checking `create table/schema`](https://github.com/pingcap/tidb/pull/7608)
* [Merge multiple `EQ` or `In` expressions if possible when calculating the range](https://github.com/pingcap/tidb/pull/7577)
* [Use `UnsafeDestroyRange` instead of `DeleteRange` in GC](https://github.com/pingcap/tidb/pull/7560)
* [Make `updateRecord` easier to understand](https://github.com/pingcap/tidb/pull/7557)
* [Update the way of using the index feedback](https://github.com/pingcap/tidb/pull/7488)
* [Move the error library from `juju/errors` to `pkg/errors`](https://github.com/pingcap/tidb/pull/7151)

## Fixed

* [Fix a bug in `INSERT ... ON DUPLICATE KEY UPDATE`](https://github.com/pingcap/tidb/pull/7675)
* [Consider the timezone when calculating the default value for `datetime`](https://github.com/pingcap/tidb/pull/7655)
* [Fix parsing `datetime` from `string`](https://github.com/pingcap/tidb/pull/7654)
* [Use the inferred type as the column type in the schema](https://github.com/pingcap/tidb/pull/7624)
* [Fix the default `NUMBER_SCALE` value of the float type in `INFORMATION_SCHEMA.COLUMNS`](https://github.com/pingcap/tidb/pull/7602)

# Weekly update in TiSpark

Last week, we landed [1 PR](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-09-10..2018-09-16+) in the TiSpark repository.

## Fixed

- [Resolve the conflicting `jackson` version introduced by `typesafe.play`](https://github.com/pingcap/tispark/pull/449)

# Weekly update in TiKV and PD

Last week, we landed [28 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-09-10..2018-09-16+) in the TiKV and PD repositories.

## Added

- [Add new built-in functions `builtin-log2` and `builtin-log10`](https://github.com/tikv/tikv/pull/3379)
- [Scale a TiKV cluster](https://github.com/tikv/tikv/pull/3585)
- [Implement `DestroyRange`](https://github.com/tikv/tikv/pull/3560)
- [Add a thread pool `scheduler`](https://github.com/tikv/tikv/pull/3582)

## Fixed

- [Fix the panic issue about the `hot store` command](https://github.com/pingcap/pd/pull/1244)
- [Suppress the growth of `EntryCache` when a TiKV peer is down](https://github.com/tikv/tikv/pull/3529)
- [Update the follower size and keys after a commit is merged](https://github.com/tikv/tikv/pull/3573)
- [Broadcast the commit for urgent requests](https://github.com/tikv/tikv/pull/3592) 
- [Flush logs before exiting](https://github.com/tikv/tikv/pull/3594)
- [Remove `ReadDelegate` lazily when a peer is destroyed asynchronously](https://github.com/tikv/tikv/pull/3596)
- [Fix a check about messages from the merged Region](https://github.com/tikv/tikv/pull/3604)

## Improved

- [Make the TSO time decoding in `pd-ctl` more accurate](https://github.com/pingcap/pd/pull/1242)
- [Reduce the scheduler messages](https://github.com/tikv/tikv/pull/3583)
- [Use asynchronous snapshots in scheduler](https://github.com/tikv/tikv/pull/3551)
- [Split the `txn` process module](https://github.com/tikv/tikv/pull/3609)
- [Remove `Generic` from `DAGContext`](https://github.com/tikv/tikv/pull/3598)
- [Introduce `Deadline` and a new `ReqContext`](https://github.com/tikv/tikv/pull/3599)

# New contributors (Thanks!)

- tidb: [kuafou](https://github.com/kuafou)
- tikv: [sllt](https://github.com/sllt)
- docs-cn: [ethercflow](https://github.com/ethercflow)
