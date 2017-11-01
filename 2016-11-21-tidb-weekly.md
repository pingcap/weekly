---
title: Weekly update (November 14 ~ November 20, 2016)
date: 2016-11-21
summary: Last week, we landed 30 PRs in the TiDB repositories, 3 PRs in the TiDB docs repositories, and 19 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV']
---

# Weekly update in TiDB

Last week, we landed [30 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-11-14..2016-11-20) in the TiDB repositories, [3 PRs](https://github.com/pingcap/docs/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-11-14..2016-11-20%20) in the TiDB docs repositories.

## Added

+ Add [a session variable to skip unique constraint check](https://github.com/pingcap/tidb/pull/2031): This could be used when migrating data.

+ [More metrics for statement counter](https://github.com/pingcap/tidb/pull/1967).

## Fixed

+ [Use reserved keywords as the table/column name](https://github.com/pingcap/tidb/pull/2039).

+ [Add missing comments in the `show table status` result](https://github.com/pingcap/tidb/pull/2032).

+ [Fix a bug that gets duplicate `auto_inc` ID after truncating table.](https://github.com/pingcap/tidb/pull/2000).

## Improved

+ [Make the Explain result more explicit](https://github.com/pingcap/tidb/pull/2022).

+ [Tune the package size](https://github.com/pingcap/tidb/pull/2021) to be friendly for rocksdb.

+ [Use a better way to reload schema](https://github.com/pingcap/tidb/pull/2006) and reduce memory usage.

+ [Fetch schemas in a parallel way](https://github.com/pingcap/tidb/pull/1996) to make it faster when there are a huge number of schemas and tables.

## Document change

Add the following new guides:

* [Compatibility with MySQL](https://github.com/pingcap/docs/blob/master/op-guide/mysql-compatibility.md).

* [Reading data from history versions](https://github.com/pingcap/docs/blob/master/op-guide/history-read.md).

# Weekly update in TiKV

Last week, we landed [19 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2016-11-13..2016-11-19&type=Issues&ref=searchresults) in the TiKV repositories.

## Fixed

+ Check whether the [message is discarded](https://github.com/pingcap/tikv/pull/1316) after proposing.

## Improved

+ Still refactor cache to make it more easily to use, with PR [360](https://github.com/pingcap/pd/pull/360), [382](https://github.com/pingcap/pd/pull/382).

+ Add [lock Time To Live (TTL)](https://github.com/pingcap/tikv/pull/1302) for large transactions.

+ Try [updating the soft limit](https://github.com/pingcap/tikv/pull/1308) when requirement check fails.

+ Support configuring [fill cache](https://github.com/pingcap/tikv/pull/1309).

+ [Limit the WriteBatch size](https://github.com/pingcap/tikv/pull/1312) for the ResolveLock and Garbage Collection commands. 

+ Clean up unnecessary [filter args](https://github.com/pingcap/pd/pull/387).

+ [Abstract a Selector](https://github.com/pingcap/pd/pull/388) to handle different strategies to select stores. 

+ Enlarge the [latches size]([https://github.com/pingcap/tikv/pull/1321](https://github.com/pingcap/tikv/pull/1321)) of the scheduler to reduce lock conflicts.
