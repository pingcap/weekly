---
layout: post
title: Weekly Update
---
## Weekly update in TiDB

Last week, we landed [40 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-03-20..2017-03-26%20) in the TiDB repositories.

## Added

* [Support Sort Merge Join operator.](https://github.com/pingcap/tidb/pull/2850)

* Add many builtin functions: [`degree`](https://github.com/pingcap/tidb/pull/2844), [`insert`](https://github.com/pingcap/tidb/pull/2855), [`instr`](https://github.com/pingcap/tidb/pull/2857), [`any_value`](https://github.com/pingcap/tidb/pull/2866), [`elt`](https://github.com/pingcap/tidb/pull/2870), [`uuid`](https://github.com/pingcap/tidb/pull/2875), [`ord`](https://github.com/pingcap/tidb/pull/2881), [`sin`](https://github.com/pingcap/tidb/pull/2885), [`inet_ntoa`](https://github.com/pingcap/tidb/pull/2887), [`maketime`](https://github.com/pingcap/tidb/pull/2889), [`sha2`](https://github.com/pingcap/tidb/pull/2914), [`quarter`](https://github.com/pingcap/tidb/pull/2919),

* [Add a command line flag to start TiDB without authentication function.](https://github.com/pingcap/tidb/pull/2897)

* [Support use special comment `/*+ */` for optimizer hint.](https://github.com/pingcap/tidb/pull/2904)

* [Make index serial scan concurrency configurable with system variable.](https://github.com/pingcap/tidb/pull/2928)

## Fixed

* [Replace standard `context` package with `golang.org/x/net/context`.](https://github.com/pingcap/tidb/pull/2890)

* [Fix a bug in the `floor` builtin function.](https://github.com/pingcap/tidb/pull/2898)

* [Fix a bug in the `date_format` builtin function.](https://github.com/pingcap/tidb/pull/2908)

* [Fix goroutine leak in tikv client.](https://github.com/pingcap/tidb/pull/2921)


## Improved

* [Build statistics with multiple goroutines.](https://github.com/pingcap/tidb/pull/2713)

* Refactor coprocessor architecture: [Add DAG physical plan protobuf](https://github.com/pingcap/tidb/pull/2896) make code cleaner.

* [Refactor TiDB specific system variable](https://github.com/pingcap/tidb/pull/2915): Make code cleaner.

## New Contributors

**Thank you guys!**

* [Ma Xiaoyu](https://github.com/ilovesoup)

* [Zhang Yuning](https://github.com/codeworm96)

* [zs634134578](https://github.com/zs634134578)

* [Arthur Yang](https://github.com/arthuryangcs)

* [qhsong](https://github.com/qhsong)

* [Sheng Tang](https://github.com/ts25504)

* [hiwjd](https://github.com/hiwjd)


# Weekly update in TiKV

# 2017-03-27

Last week, We landed [18 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-03-19..2017-03-25&type=Issues) in the TiKV repositories.

## Added

* Add RocksDB [WAL options](https://github.com/pingcap/tikv/pull/1679) to support in memory storage.

## Fixed

* Fix fetching [stale TSO](https://github.com/pingcap/pd/pull/572) when leader switch back to the previous node.

* Make sure that [commit TS is always after the start TS](https://github.com/pingcap/tikv/pull/1690).

* [Speed up](https://github.com/pingcap/tikv/pull/1696) transferring leader process.

## Improved

* Make [Lock CF](https://github.com/pingcap/tikv/pull/1685) configurable. 

* Make [schedule and replication options](https://github.com/pingcap/pd/pull/574) persistent. 

* [Optimize balance speed](https://github.com/pingcap/pd/pull/575) with calculating leader/region count from cache.

* Prepare for introducing mio 0.6, see [1691](https://github.com/pingcap/tikv/pull/1691) [1692](https://github.com/pingcap/tikv/pull/1692) [1695](https://github.com/pingcap/tikv/pull/1695).

## New Contributor (Thanks!)

* [aya](https://github.com/aya)