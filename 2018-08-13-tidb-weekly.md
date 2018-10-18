---
title: Weekly update (August 06 ~ August 12, 2018)
date: 2018-08-13
summary: Last week, we landed 46 PRs in the TiDB repositories and 27 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [46 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-08-06..2018-08-12+) in the TiDB repositories.

## Added

- [Support the `Update` operation for table partition](https://github.com/pingcap/tidb/pull/7166)
- [Support the prefix index in `admin check table`](https://github.com/pingcap/tidb/pull/7241)

## Fixed

- [Fix behaviors of builtin `LTrim`, `RTrim` and `Trim`](https://github.com/pingcap/tidb/pull/7291)
- [Fix `group_concat(a)` when `a` is null](https://github.com/pingcap/tidb/pull/7287)
- [Make `USE INDEX(PRIMARY)` work on the integer primary key](https://github.com/pingcap/tidb/pull/7298)
- [Fix `admin check table` false alarm when the index contains the `pkIsHandle` column](https://github.com/pingcap/tidb/pull/7317)
- [Fix inconsistent row count estimation](https://github.com/pingcap/tidb/pull/7233)
- [Fix a bug when applying the `RenameTable` diff](https://github.com/pingcap/tidb/pull/7336)

## Improved

- [Perform the batch check for the constrains when adding a unique index](https://github.com/pingcap/tidb/pull/7132)
- [Remove `Exists` in `plan` and `executor`](https://github.com/pingcap/tidb/pull/7207)
- [Disable the Read Committed isolation level](https://github.com/pingcap/tidb/pull/7280)
- [Refactor `joinResultGenerator` to handle the unmatched outer records](https://github.com/pingcap/tidb/pull/7288)
- [Adjust the way of checking all the schema versions](https://github.com/pingcap/tidb/pull/7319)
- [Update the import path from `coreos/gofail` to `etcd-io/gofail` to fix CI](https://github.com/pingcap/tidb/pull/7329)

# Weekly update in TiKV and PD

Last week, we landed [27 PRs](https://github.com/search?p=1&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-08-06..2018-08-13&type=Issues) in the TiKV and PD repositories.

## Added

- Support more functions in Coprocessor: 
    
    - [`upper/lower`](https://github.com/tikv/tikv/pull/3433)
    - [`bin`](https://github.com/tikv/tikv/pull/3397)
    - [`PI`](https://github.com/tikv/tikv/pull/3382)
    - [`interval`](https://github.com/tikv/tikv/pull/3330)

- [Support splitting Regions by the number of keys](https://github.com/tikv/tikv/pull/3317)
- [Make PD support allocating timestamp after recovering from incorrect system time](https://github.com/pingcap/pd/pull/1173)

## Fixed

- [Fix the TiKV panic when the decimal overflows](https://github.com/tikv/tikv/pull/3343)
- [Prevent `dynamic-level-size` from being turned on for existing TiKV clusters](https://github.com/tikv/tikv/pull/3348/files)

## Improved

- [Output unit `B` in tikv-ctl](https://github.com/tikv/tikv/pull/3421)
- [Improve TiKV Read flow statistics accuracy](https://github.com/tikv/tikv/pull/3402)
- Improve the TiKV performance: 
    
    - [PR1](https://github.com/tikv/tikv/pull/3429)
    - [PR2](https://github.com/tikv/tikv/pull/3419)
    - [PR3](https://github.com/tikv/tikv/pull/2639)

- [Improve the PD performance](https://github.com/pingcap/pd/pull/1180) 
- [Improve the TiKV log output](https://github.com/tikv/tikv/pull/3416) 
- [Add a test for time fallback in PD](https://github.com/pingcap/pd/pull/1186)
- [Improve the PD error code](https://github.com/pingcap/pd/pull/1167)

# New contributors (Thanks!)

docs-cn:

- [Lunatictwo](https://github.com/Lunatictwo)

TiKV:

- [smallyard](https://github.com/smallyard)
- [sweetIan](https://github.com/sweetIan)
