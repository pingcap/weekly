---
layout: post
title: Weekly Update
---
## Weekly update in TiDB

Last week, we landed [21 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-02-27..2017-03-05%20) in the TiDB repositories.

## Added

* [Add metrics for related region count for a transaction.](https://github.com/pingcap/tidb/pull/2701)

* [Record sql_mode in session context.](https://github.com/pingcap/tidb/pull/2739)

* [Support `Show Processlist`.](https://github.com/pingcap/tidb/pull/2744)

* [Add an empty `Triggers` table in information_schema database.](https://github.com/pingcap/tidb/pull/2749)

* [Support `ANSI_QUOTES` sql_mode in parser.](https://github.com/pingcap/tidb/pull/2754)

* [Support use wildcard as user hostname in grant statement.](https://github.com/pingcap/tidb/pull/2757)

* [Support the `MD5` builtin function.](https://github.com/pingcap/tidb/pull/2780)

* [Support the `SHA/SHA1` builtin function.](https://github.com/pingcap/tidb/pull/2781)


## Fixed

* [Use `PI` as identifier](https://github.com/pingcap/tidb/pull/2763)

* [Fix a panic in prepared statement.](https://github.com/pingcap/tidb/pull/2767)


## Improved

* [Use unique key to eliminate aggregation.](https://github.com/pingcap/tidb/pull/2702)

* [Tuning tikv client max timeout parameter.](https://github.com/pingcap/tidb/pull/2746)

* [Adjust log level in tikv client.](https://github.com/pingcap/tidb/pull/2765)


# Weekly update in TiKV

Last week, We landed [8 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-02-26..2017-03-04+&type=Issues&ref=searchresults) in the TiKV repositories.

## Added

* Use [ReadIndex](https://github.com/pingcap/tikv/pull/1642) to serve safe Raft read.

* Add [`tso`](https://github.com/pingcap/pd/pull/550) command for `pd-ctl`.

* Add [ServerIsBusy](https://github.com/pingcap/tikv/pull/1660) metric.

## Fixed

* Fix a [data race](https://github.com/pingcap/pd/pull/552) when update configuration.

## Improved

* [Notify PD](https://github.com/pingcap/tikv/pull/1658) immediately when leader changes.

* Make scheduler [TooBusy threshold](https://github.com/pingcap/tikv/pull/1666) configurable.
