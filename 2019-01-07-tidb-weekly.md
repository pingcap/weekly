---
title: Weekly update (December 31 ~ January 06, 2019)
date: 2019-01-07
summary: Last week, we landed 38 PRs in the TiDB repository, 2 PRs in the TiSpark repository, and 10 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [38 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-12-31..2019-01-06+) in the TiDB repository.

## Added

- [Add support for `Views` in `Infoschema`](https://github.com/pingcap/tidb/pull/8892)
- [Add support for `Drop View`](https://github.com/pingcap/tidb/pull/8791)
- [Support the `Window` function in the planner](https://github.com/pingcap/tidb/pull/8630)
- [Add support for the `default` function](https://github.com/pingcap/tidb/pull/8540)
- [Implement the parallel partition phase for Radix Hash Join](https://github.com/pingcap/tidb/pull/7911)

## Improved

- [Support the `show create database if not exists` syntax](https://github.com/pingcap/tidb/pull/8926)
- [Forbid committing the transaction if `StmtCommit` fails](https://github.com/pingcap/tidb/pull/8918)
- [Report an error when updating the generated column inside a transaction](https://github.com/pingcap/tidb/pull/8909)
- [Improve the compatibility when using an empty database](https://github.com/pingcap/tidb/pull/8908)
- [Run `FLUSH PRIVILEGES` synchronously on `GRANT`](https://github.com/pingcap/tidb/pull/8886)
- [Support `show columns from` for `Views`](https://github.com/pingcap/tidb/pull/8863)
- [Refine the code about DDL job canceling or rollback](https://github.com/pingcap/tidb/pull/8858)
- [Check the user privilege on `SET GLOBAL`](https://github.com/pingcap/tidb/pull/8837)
- [Add the post-process stage after physical optimization](https://github.com/pingcap/tidb/pull/8828)
- [Propagate the constraint for `>` and monotonous increasing functions](https://github.com/pingcap/tidb/pull/8640)

## Fixed

- [Handle the empty input and improve the compatibility for `format`](https://github.com/pingcap/tidb/pull/8797)
- [Fix the panic when writing a table with a column in the write only state](https://github.com/pingcap/tidb/pull/8792)
- [Fix the insert failure when dropping a column](https://github.com/pingcap/tidb/pull/8791)
- [Fix the hang issue of canceling `Add Index`](https://github.com/pingcap/tidb/pull/8621)

# Weekly update in TiSpark

Last week, we landed [2 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-12-31..2019-01-06+) in the TiSpark repository.

## Improved

- [Add retry for `getRegion` requests when `regionId` returns `0`](https://github.com/pingcap/tispark/pull/542)

## Fixed

- [Allow checking the TiSpark version when a database is not selected](https://github.com/pingcap/tispark/issues/545)

# Weekly update in TiKV and PD

Last week, we landed [10 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-12-31..2019-01-06&type=Issues) in the TiKV and PD repositories.

## Added

- [Add the `add_duration_and_duration` built-in function](https://github.com/tikv/tikv/pull/3984)

## Improved

- [Upgrade `rust-rocksdb` to upgrade RocksDB to Titan smoothly](https://github.com/tikv/tikv/pull/4002)
- [Rearrange loggers](https://github.com/tikv/tikv/pull/3987)
- [Retry validating the endpoints when creating a RPC client](https://github.com/tikv/tikv/pull/3851)

# New contributors (Thanks!)

tidb:

- [Westicles1980](https://github.com/Westicles1980)
- [acmerfight](https://github.com/acmerfight)

parser:

- [924060929](https://github.com/924060929)
- buzzers
- [lnhote](https://github.com/lnhote)
- [shinytang6](https://github.com/shinytang6)

docs-cn:

- [zzh1985](https://github.com/zzh1985)

docs:

- [b41sh](https://github.com/b41sh)