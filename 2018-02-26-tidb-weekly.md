---
title: Weekly update (February 12 ~ February 25, 2018)
date: 2018-02-26
summary: Last two weeks, we landed 27 PRs in the TiDB repositories and 13 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last two weeks, we landed [27 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is:pr+is:merged+merged:2018-02-12..2018-02-25) in the TiDB repositories.

## Added

* [Support the `select 1 order by 1` syntax](https://github.com/pingcap/tidb/pull/5881)

## Fixed

* [Fix the bug in `insert` statements when dropping columns](https://github.com/pingcap/tidb/pull/5883)
* [Fix the bug when updating the stats table](https://github.com/pingcap/tidb/pull/5880)

## Improved

* [Allow `golint` to check `context.Context` in `make check`](https://github.com/pingcap/tidb/pull/5898/files)
* [Do not import `golang.org/x/net/context` as `goctx` alias](https://github.com/pingcap/tidb/pull/5895)
* [Move the package context to `sessionctx`](https://github.com/pingcap/tidb/pull/5890)
* [Add the recover mechanism for join workers](https://github.com/pingcap/tidb/pull/5894)
* [Add `StatementsPerTransaction` and `TransactionDuration` metrics](https://github.com/pingcap/tidb/pull/5859)
* [Add `keep alive` metrics to figure out whether TiDB instance is down](https://github.com/pingcap/tidb/pull/5847)

# Weekly update in TiKV and PD

Last two weeks, we landed [13 PRs](https://github.com/search?q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-02-12..2018-02-25) in the TiKV and PD repositories.

## Added

* [Add peer label level statistics](https://github.com/pingcap/pd/pull/951)
* [Support stream aggregation](https://github.com/pingcap/tikv/pull/2714)
* [Support multiple Regions in `tombstone`](https://github.com/pingcap/tikv/pull/2711)
* [Add a handler which is invoked after the client reconnects to PD](https://github.com/pingcap/tikv/pull/2757)

## Fixed

* [Fix the misspelled word to improve GoReport Card Result](https://github.com/pingcap/pd/pull/956)
* [Fix the panic caused by `region not found`](https://github.com/pingcap/pd/pull/957)
* [Fix the bug of the hot region scheduler adding peers to down stores](https://github.com/pingcap/pd/pull/958)

## Improved

* [Add the timestamp field for the Region heartbeat](https://github.com/pingcap/tikv/pull/2728)
* [Increase the priority of replica checker's operator](https://github.com/pingcap/pd/pull/954)
* [Increase the default value of the replica scheduler limit](https://github.com/pingcap/pd/pull/960)
