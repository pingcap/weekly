---
title: Weekly update (January 28 ~ February 10, 2019)
date: 2019-02-11
summary: Last two weeks, we landed 25 PRs in the TiDB repository, 2 PRs in the TiSpark repository, and 23 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last two weeks, we landed [25 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-01-28..2019-02-10+) in the TiDB repository.

## Added

- [Add the `tidb_indexes` table in `infoschema`](https://github.com/pingcap/tidb/pull/9183)

## Improved

- [Enable the `any_value` function in aggregation if `ONLY_FULL_GROUP_BY` is set](https://github.com/pingcap/tidb/pull/9255)
- [Improve the compatibility of the `format` function with MySQL](https://github.com/pingcap/tidb/pull/9182)
- [Support the JSON type for the `COALESCE` built-in function](https://github.com/pingcap/tidb/pull/9087)
- [Rewrite the exact `like` expression to the equal condition](https://github.com/pingcap/tidb/pull/9071)
- [Derive the `col is not null` condition from `col op col`](https://github.com/pingcap/tidb/pull/8603)

## Fixed

- [Create a new slice when cloning arguments of `baseFuncDesc`](https://github.com/pingcap/tidb/pull/9254)
- [Handle `Float32` for the `values` built-in function](https://github.com/pingcap/tidb/pull/9215)
- [Fix precision when casting a float to a string](https://github.com/pingcap/tidb/pull/9137)

# Weekly update in TiSpark

Last two weeks, we landed [2 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-01-28..2019-02-10+) in the TiSpark repository.

## Added

- [Support using TiDB as a meta store](https://github.com/pingcap/tispark/pull/544)

## Fixed

- [Fix the timestamp consistency issue](https://github.com/pingcap/tispark/pull/550)

# Weekly update in TiKV and PD

Last two weeks, we landed [23 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-01-28..2019-02-10&type=Issues) in the TiKV and PD repositories.

## Improved

- [Configure criterion from TiKV command line arguments](https://github.com/tikv/tikv/pull/4169)
- [Enlarge `max-manifest-file-size` to 128MB](https://github.com/tikv/tikv/pull/4140)
- [Make PD `Region` commands support `jq`](https://github.com/pingcap/pd/pull/1420)

## Fixed

- [Revert updating to the latest version of etcd](https://github.com/pingcap/pd/pull/1425)
- [Do not return a retriable error when TiKV is closing](https://github.com/tikv/tikv/pull/4146)
- [Upgrade to Rust 2018](https://github.com/tikv/tikv/pull/4138)
- [Disable `procinfo` on the non-Linux platform](https://github.com/tikv/tikv/pull/4133)

# New contributors (Thanks!)

tidb:

- [caohe](https://github.com/caohe)
- [tender-boluo](https://github.com/tender-boluo)

pd:

- [fredchenbj](https://github.com/fredchenbj)