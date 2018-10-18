---
title: Weekly update (June 18 ~ June 24, 2018)
date: 2018-06-25
summary: Last week, we landed 18 PRs in the TiDB repositories, 5 PRs in the TiSpark repositories, and 19 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD', 'TiSpark']
---

# Weekly update in TiDB

Last week, we landed [18 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is:pr+is:merged+merged:2018-06-18..2018-06-24) in the TiDB repositories.

## Added

- [Support the binary fetch command](https://github.com/pingcap/tidb/pull/6648)
- [Add a variable to disable auto-retry of the transaction block](https://github.com/pingcap/tidb/pull/6872)

## Fixed

- [Allow comments to end up with multiple asterisks as MySQL does](https://github.com/pingcap/tidb/pull/6847)

## Improved

- [Allow using `IndexJoin` in more scenarios](https://github.com/pingcap/tidb/pull/6664)
- [Improve the performance of the `insert ignore on duplicate key update` statement](https://github.com/pingcap/tidb/pull/6760)
- [Optimize the accuracy of index row count estimation](https://github.com/pingcap/tidb/pull/6869)

# Weekly update in TiSpark

Last week, we landed [5 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-06-18..2018-06-24) in the TiSpark repositories.

## Added

- [Add deployment tools and information in `pom`](https://github.com/pingcap/tispark/pull/369)
- [Add the code coverage report tool](https://github.com/pingcap/tispark/pull/368)

# Weekly update in TiKV and PD

Last week, we landed [19 PRs](https://github.com/search?p=2&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-06-18..2018-06-24&type=Issues&utf8=%E2%9C%93) in the TiKV and PD repositories.

## Added

- [Count each index prefix when executing the Analyze operation](https://github.com/pingcap/tikv/pull/3206)
- [Allow configuring the timespan of log rotation](https://github.com/pingcap/tikv/pull/3219)
- [Provide more RocksDB metrics](https://github.com/pingcap/tikv/pull/3209)

## Fixed

- [Fix TiKV panic when multiplying specific decimals](https://github.com/pingcap/tikv/pull/3222)

## Improved

- [Change the maximum size of the bucket for snapshot from 2G to 1T](https://github.com/pingcap/tikv/pull/3221)
- Improve TiKV metrics performance [PR1](https://github.com/pingcap/tikv/pull/3227) [PR2](https://github.com/pingcap/tikv/pull/3225)
- [Preserve logs instead of dropping logs when logs overflow](https://github.com/pingcap/tikv/pull/3191)

# New contributors (Thanks!)

TiDB:

- [mz1999](https://github.com/mz1999)
- [liuzhengyang](https://github.com/liuzhengyang)