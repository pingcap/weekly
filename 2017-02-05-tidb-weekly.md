---
date: 2017-02-05T00:00:00Z
title: Weekly Update
---

## Weekly update in TiDB

Last two weeks, we landed [43 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-01-23..2017-02-05%20) in the TiDB repositories.

## Added

* [Support information_schema.table_constraints.](https://github.com/pingcap/tidb/pull/2586)

* [Support the `UTC_TIMESTAMP` builtin function](https://github.com/pingcap/tidb/pull/2592)

* [Increase transaction entry count limit.](https://github.com/pingcap/tidb/pull/2537)

* Add logs for expensive query and big transaction: [2536](https://github.com/pingcap/tidb/pull/2536), [2545](https://github.com/pingcap/tidb/pull/2545), [2546](https://github.com/pingcap/tidb/pull/2546)

## Fixed

* [Fix GC lifetime metrics.](https://github.com/pingcap/tidb/pull/2587)

* [Fix primary key name parsing.](https://github.com/pingcap/tidb/pull/2582)

* [Fix a bug of left outer semi join.](https://github.com/pingcap/tidb/pull/2573)

* [Fix a bug of exists sub query.](https://github.com/pingcap/tidb/pull/2549)

* [Fix a bug abaout prefix index.](https://github.com/pingcap/tidb/pull/2445)

## Improved

* [Only plans that have apply will add cache.](https://github.com/pingcap/tidb/pull/2564)

* [Use a short-cut way to way And/Or/Xor expresson.](https://github.com/pingcap/tidb/pull/2561)

* [Refine the range calculating.](https://github.com/pingcap/tidb/pull/2534)

# Weekly update in TiKV

Last two weeks, we landed [20 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-01-22..2017-02-04&type=Issues&ref=searchresults) in the TiKV repositories.

## Added

+ Add [`start_ts`](https://github.com/pingcap/tikv/pull/1511) for scan in `tikv-ctl`.

+ Support [HTTP scheme](https://github.com/pingcap/tikv/pull/1543) parsing.

## Fixed

+ Fix [too long](https://github.com/pingcap/tikv/pull/1566) scan slow log.

## Improved

+ Use [`reverse_seek_le`](https://github.com/pingcap/tikv/pull/1498) for the reverse seek write.

+ [Ignore overwriting data](https://github.com/pingcap/tikv/pull/1500) in `prewrite`.

+ [Update raft in raftstore](https://github.com/pingcap/tikv/pull/1540) after handling ConfChange.

+ Make [coprocessor task](https://github.com/pingcap/tikv/pull/1551) run more concurrently.

+ [Ignore deleting the value](https://github.com/pingcap/tikv/pull/1553) when roll back `lock`.

+ [Update leader lease](https://github.com/pingcap/tikv/pull/1560) before applying raft log.
