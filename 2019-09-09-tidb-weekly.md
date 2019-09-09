---
title: Weekly update (September 02 ~ September 08, 2019)
date: 2019-09-09
summary: Last week, we landed 55 PRs in the TiDB repository and 29 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog post

Our blog post [Lesson Learned from Queries over 1.3 Trillion Rows of Data Within Milliseconds of Response Time at Zhihu.com](https://pingcap.com/success-stories/lesson-learned-from-queries-over-1.3-trillion-rows-of-data-within-milliseconds-of-response-time-at-zhihu/) became the first spotlight on [Dzone](https://dzone.com/articles/lesson-learned-from-queries-over-13-trillion-rows-1).

## Community

### New contributors

tikv:

* [jadireddi](https://github.com/jadireddi)
* [aknuds1](https://github.com/aknuds1)

parser:

* [hey-kong](https://github.com/hey-kong)
* [yangwenmai](https://github.com/yangwenmai)
* [yufeiminds](https://github.com/yufeiminds)

rust-prometheus:

* [brndnmtthws](https://github.com/brndnmtthws)

## Call for participation

TiDB:

* [Vectorize all the built-in functions](https://github.com/pingcap/tidb/issues/12058)
* [Issues to solve](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)

TiKV:

* [Issues to solve](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

TiDB:

Last week, we landed [55 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-09-02..2019-09-08+) in the TiDB repository.

* Release [TiDB v3.0.3](https://pingcap.com/docs/v3.0/releases/3.0.3/)
* Add a test framework for the functions of vectorized expression evaluation
* Enable the vectorized expression evaluation by default
* Support dividing a Region into multiple Regions

TiSpark:

* Release TiSpark [v2.1.5](https://github.com/pingcap/tispark/releases/tag/v2.1.5) and [v2.2.0](https://github.com/pingcap/tispark/releases/tag/v2.2.0)

TiKV and PD:

Last week, we landed [29 PRs](https://github.com/search?p=3&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-09-02..2019-09-08&type=Issues) in the TiKV and PD repositories.

* Release TiKV and PD [v3.0.3](https://pingcap.com/docs/v3.0/releases/3.0.3/)
* Fix the issue that a wrong value might be returned when the number of keys is `0`
* Fix the issue that a Region does not merge to the sibling with smaller size
* Support updating the lock TTL through heartbeats when executing a large transaction
* Support checking configuration by running the `config-check` command-line option

### Critical PRs

TiDB:

* [Support the vectorized bitmap operations for `nulls` in `Column`](https://github.com/pingcap/tidb/pull/12034)
* [Fix the `modify column` operation on the `bit` column](https://github.com/pingcap/tidb/pull/12008)
* [Add a test framework for the functions of vectorized expression evaluation](https://github.com/pingcap/tidb/pull/11963)
* [Eliminate the redundant projection](https://github.com/pingcap/tidb/pull/11920)
* [Support dividing a Region into multiple Regions](https://github.com/pingcap/tidb/pull/11739)
* [Support `index_lookup_merge_join` in the physical plan](https://github.com/pingcap/tidb/pull/11338)
* [Support `IndexNestedLoopHashJoin`](https://github.com/pingcap/tidb/pull/8661)
* [Do not send TSO requests when `point get` uses `maxUint64` as its transaction timestamp](https://github.com/pingcap/tidb/pull/11981)
* [Enable the vectorized expression evaluation by default](https://github.com/pingcap/tidb/pull/11965)
* [Split `AVG` to `COUNT` and `SUM` for the `TableReader` Coprocessor task](https://github.com/pingcap/tidb/pull/11926)

TiKV and PD:

* [Use the new `approximate keys` function when the result is `0`](https://github.com/tikv/tikv/pull/5415)
* [Add the `txn_heart_beat` API](https://github.com/tikv/tikv/pull/5407)
* [Fix the issue that a Region does not merge to the sibling with smaller size](https://github.com/pingcap/pd/pull/1726)
* [Add the backup service](https://github.com/tikv/tikv/pull/5359)
* [Add the `config-check` flag for tikv-server](https://github.com/tikv/tikv/pull/5391)
* [Add the `config-check` flag for pd-server](https://github.com/pingcap/pd/pull/1725)
* [Continue to use OpenSSL](https://github.com/tikv/tikv/pull/5384)
* [Fix a thread-safe bug and improve code](https://github.com/pingcap/pd/pull/1719)
* [Fix the precision loss while unflattening `Duration` in `codec`](https://github.com/tikv/tikv/pull/5367)

### Proposal

TiDB:

* [Add Contributor Covenant Code of Conduct](https://github.com/pingcap/tidb/pull/12010)
* [Update the Github workflow](https://github.com/pingcap/tidb/pull/12000)

## Upcoming TiDB event

[Paper reading](https://calendar.google.com/calendar/embed?src=community%40pingcap.com&ctz=Asia%2FShanghai)
