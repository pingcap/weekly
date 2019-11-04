---
title: Weekly update (October 28 ~ November 03, 2019)
date: 2019-11-04
summary: Last week, we landed 100 PRs in the TiDB repository, 6 PRs in the TiSpark repository, 47 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog post

Summoned by TiDB Hackathon 2019, a bunch of passionate hackers and geeks gathered in three PingCAP offices in Beijing, Shanghai, and Guangzhou on October 26 and 27. They contributed their brilliant ideas to "Improve" TiDB.

Last week, we published a post that introduces the top 3 winners at TiDB Hackathon 2019 and the cozy and friendly environment of this meeting.

The full article is here:

[INSERT INTO tidb.hackathon_2019 VALUES ("Hack", "Fun", "TiDB Ecosystem")](https://pingcap.com/blog/insert-into-tidb-hackathon-2019-values-hack-fun-tidb-ecosystem/)

## Community

### New contributors

tidb:

* [TommyCpp](https://github.com/TommyCpp)
* [icditwang](https://github.com/icditwang)
* [yjh126yjh](https://github.com/yjh126yjh)
* [edytagarbarz](https://github.com/edytagarbarz)
* [cosmic-jc](https://github.com/cosmic-jc)

docs-cn:

* [shonge](https://github.com/shonge)

## Call for participation

* [Vectorized Expression Working Group](https://github.com/pingcap/community/blob/master/working-groups/wg-vec-expr.md)
    * [`Date` or `Time` built-in functions (16/65)](https://github.com/pingcap/tidb/issues/12101)
    * [`Decimal` built-in functions (15/31)](https://github.com/pingcap/tidb/issues/12102)
    * [`Int` built-in functions (112/187)](https://github.com/pingcap/tidb/issues/12103)
    * [`JSON` built-in functions (15/27)](https://github.com/pingcap/tidb/issues/12104)
    * [`Real` built-in functions (41/49)](https://github.com/pingcap/tidb/issues/12105)
    * [`String` built-in functions (56/133)](https://github.com/pingcap/tidb/issues/12106)
    * [`Duration` built-in functions (13/45)](https://github.com/pingcap/tidb/issues/12176)
    * Last week, [36 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+sort%3Aupdated-desc+merged%3A2019-10-28..2019-11-03+label%3Acomponent%2Fexpression+) are landed in the expression component.

* Coprocessor SIG:
    * [Improve the performance of Chunk Encoder](https://github.com/tikv/tikv/issues/5729)
    * [Implement more UDFs](https://github.com/tikv/tikv/issues/5727)
    * [Implement the new row format](https://github.com/tikv/tikv/issues/5726)
    * [Port `BinaryJSON`](https://github.com/tikv/tikv/issues/5715)
    * [Tracing](https://github.com/tikv/tikv/issues/5714)
    * [The maximum execution time of Per-request](https://github.com/tikv/tikv/issues/5712)

* [More issues to solve for TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)
* [More issues to solve for TiKV](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

Last week, we landed [100 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-10-28..2019-11-03+) in the TiDB repository, [6 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-10-28..2019-11-03+) in the TiSpark repository, and [47 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-10-28..2019-11-03&type=Issues) in the TiKV and PD repositories.

### Critical PRs

TiDB:

* [Fix the potential goroutine leak when killing the connection](https://github.com/pingcap/tidb/pull/13051)
* [Add more fields in the `slow_query` table](https://github.com/pingcap/tidb/pull/13007)
* [Add the isolation read with the storage engine type](https://github.com/pingcap/tidb/pull/12997)
* [Add the `push selection below projection` transformation rule in the cascades planner](https://github.com/pingcap/tidb/pull/12992)
* [Support querying the CPU, memory, mutex, block, allocs, or goroutines flamegraphs by SQL statements](https://github.com/pingcap/tidb/pull/12986)
* [Stop updating the pessimistic transaction lock's TTL when the session is killed](https://github.com/pingcap/tidb/pull/12959)
* [Support scanning the TiFlash table in the cost-based optimizer](https://github.com/pingcap/tidb/pull/12868)
* [Add `enable-timestamp` and `enable-error-stack` for the log configuration](https://github.com/pingcap/tidb/pull/12853)
* [Support creating the TiFlash replica of a table in DDL operations](https://github.com/pingcap/tidb/pull/12453)

TiSpark:

* [Fix the parse failure on the JSON value of view tables](https://github.com/pingcap/tispark/pull/1174)

TiKV and PD:

* [Remove `namespace`](https://github.com/pingcap/pd/pull/1804)
* [Change the configuration names from `disable-*` to `enable-*`](https://github.com/pingcap/pd/pull/1816)
* [Improve the performance of the Coprocessor table lookup](https://github.com/tikv/tikv/pull/5682)
* [Reject commit requests with `commit_ts < primary_lock.min_commit_ts`](https://github.com/tikv/tikv/pull/5691)
* [Add the `GetRegionCount` interface](https://github.com/pingcap/pd/pull/1850)
* [Keep the pessimistic lock's TTL if it's greater than the prewrite request's TTL](https://github.com/tikv/tikv/pull/5737)
* [Add `@winkyao` to `MAINTAINERS.md`](https://github.com/tikv/tikv/pull/5785)

## Upcoming TiDB events

[TiDB Experience Sharing Meeting (Guangzhou)](https://pingcap.com/meetup/) (Chinese page)

* Time: November 7th, 2019
* Location: PingCAP office in Guangzhou, Guangdong Province

[TiDB Experience Sharing Meeting (Shenzhen)](https://pingcap.com/meetup/) (Chinese page)

* Time: November 9th, 2019
* Location: Beike Building, Nanshan District, Guangdong Province
