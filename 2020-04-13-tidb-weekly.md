---
title: Weekly update (April 06 ~ April 12, 2020)
date: 2020-04-13
summary: Last week, we landed 100 PRs in the TiDB repository and 32 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog posts

April 8th, 2020 is the 5th anniversary of PingCAP. Last week, we published an article written by our CTO Ed Huang to look back and to share his thoughts about the future of databases. The full article is here:

[A Peek into the Future of Database: A Unified Infrastructure to Adapt Intelligently](https://pingcap.com/blog/future-of-database-unified-infrastructure-to-adapt-intelligently/)

Last week, we also published a post that walks you through TiDB 4.0's highlights across its deployment, use, operations and maintenance, ecosystem, and cloud services. You're welcome to join us in [TiDB Community Slack](https://join.slack.com/t/tidbcommunity/shared_invite/enQtNzc0MzI4ODExMDc4LWYwYmIzMjZkYzJiNDUxMmZlN2FiMGJkZjAyMzQ5NGU0NGY0NzI3NTYwMjAyNGQ1N2I2ZjAxNzc1OGUwYWM0NzE) to give us advice or feedback on your user experience. The full article is here:

[TiDB 4.0 Preview: An Easier-to-Use, Production-Ready HTAP Database](https://pingcap.com/blog/tidb-4.0-preview-easier-to-use-production-ready-htap-database/)

## Community

### New contributors

tidb:

* [time-and-fate](https://github.com/time-and-fate)

docs:

* [mmyj](https://github.com/mmyj)

docs-cn:

* [wyuchen007](https://github.com/wyuchen007)
* [piperck](https://github.com/piperck)

parser:

* [cncal](https://github.com/cncal)

## Call for participation

### TiDB

* [All help-wanted issues in TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aopen+is%3Aissue+label%3Ahelp-wanted)

### TiKV

* [To support removing bad Regions by one command](https://github.com/tikv/tikv/issues/6976)
* [To combine the store balance rate and the store limit](https://github.com/pingcap/pd/issues/2245)
* [All help-wanted issues in TiKV](https://github.com/tikv/tikv/issues?q=is%3Aopen+is%3Aissue+label%3Astatus%2Fhelp-wanted)
* [All help-wanted issues in PD](https://github.com/pingcap/pd/issues?q=is%3Aissue+is%3Aopen+label%3Astatus%2Fhelp-wanted)

## Updates of the week

### Progress

Last week, we landed [100 PRs](https://github.com/pingcap/tidb/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-04-06..2020-04-12) in the TiDB repository and [32 PRs](https://github.com/tikv/tikv/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-04-06..2020-04-12+) in the TiKV and PD repositories.

#### TiDB

* [Enable the inline projection for `MergeJoin`](https://github.com/pingcap/tidb/pull/15463)
* [Support adding multiple columns](https://github.com/pingcap/tidb/pull/15540)

#### TiDB Dashboard

* [Remove some dependencies](https://github.com/pingcap-incubator/tidb-dashboard/pull/328)

#### TiUP

* The `mirrors` component is released, which is used to build a local mirror of TiUP and make TiUP available in offline scenarios.

#### TiKV

* [Improve TiKV metrics performance for `tidb_query` and `engine_rocks`](https://github.com/tikv/tikv/pull/7267)
* [Make `ChangeCmd` a significant message](https://github.com/tikv/tikv/pull/7377)
* [Set the term in the read index response](https://github.com/tikv/tikv/pull/7372)
* [Remove the scan cache and add the `ObserveID`](https://github.com/tikv/tikv/pull/7278)

#### PD

* [Support the rate control for removing peers](https://github.com/pingcap/pd/pull/2226)
* [Implement the recovery progress](https://github.com/pingcap/pd/pull/2322)
* [Update the state change process](https://github.com/pingcap/pd/pull/2332)

## On-going TiDB event

[TiDB Usability Challenge Program](https://pingcap.com/community/tidb-usability-challenge/)
