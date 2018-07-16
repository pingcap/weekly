---
title: Weekly update (July 09 ~ July 15, 2018)
date: 2018-07-16
summary: Last week, we landed 30 PRs in the TiDB repositories and 19 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [30 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-07-09..2018-07-15) in the TiDB repositories.

## Added

- [Support `BIT_AND`/`BIT_XOR` in the new aggregation framework](https://github.com/pingcap/tidb/pull/7004)
- [Support `COUNT` in the new aggregation framework](https://github.com/pingcap/tidb/pull/7009)
- [Support `AVG(DISTINCT)` in the new aggregation framework](https://github.com/pingcap/tidb/pull/7015)
- [Add the `GENERATION_EXPRESSION` column in `information_schema.columns`](https://github.com/pingcap/tidb/pull/7017)
- [Support more syntactic rules regarding the `SET` syntax](https://github.com/pingcap/tidb/pull/7020)
- [Support `ADMIN SHOW DDL JOBS <NUMBER>` to specify the lines of the results](https://github.com/pingcap/tidb/pull/7020)
- [Support showing `AUTO_INCREMENT` in `information_schema.tables`](https://github.com/pingcap/tidb/pull/7037)

## Fixed

- [Fix a bug in `INSERT SELECT FROM ON DUPLICATE KEY UPDATE`](https://github.com/pingcap/tidb/pull/6593)
- [Fix the numeric type overflow in the binary protocol](https://github.com/pingcap/tidb/pull/6922)
- [Fix the results of decimal `Minus`/`Round`/`Mul`](https://github.com/pingcap/tidb/pull/7001)

## Improved

- [Check the schema when the DDL fails](https://github.com/pingcap/tidb/pull/6797)
- [Refine the `explain` result format](https://github.com/pingcap/tidb/pull/7011)
- [Speed up `autoAnalyze` when data is unchanged](https://github.com/pingcap/tidb/pull/7022)

# Weekly update in TiKV and PD

Last week, we landed [19 PRs](https://github.com/search?q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-07-09..2018-07-15&type=Issues) in the TiKV and PD repositories.

## Added

- [Add new builtin UDFs `regexp` and `regexp_binary`](https://github.com/pingcap/tikv/pull/3196)
- [Introduce the `loose` channel](https://github.com/pingcap/tikv/pull/3286)
- [Add options to disable replica-checker features](https://github.com/pingcap/pd/pull/1140)
- [Support filtering JSON output by calling the external `jq`](https://github.com/pingcap/pd/pull/1126)

## Fixed

- [Fix the unexpected behavior of tikv-ctl `unsafe-recover` command](https://github.com/pingcap/tikv/pull/3125)

## Improved

- [Report `approximate_keys` instead of `approximate_rows`](https://github.com/pingcap/tikv/pull/3295)
- [Add TiKV adopters and Roadmap](https://github.com/pingcap/tikv/pull/3301)
- [Update `rustc` and `clippy`](https://github.com/pingcap/tikv/pull/3302)

# New contributor (Thanks!)

docs: [brunoban](https://github.com/brunoban)