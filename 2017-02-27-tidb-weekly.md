---
title: Weekly update (February 19 ~ February 26, 2016)
date: 2017-02-27
summary: Last week, we landed 39 PRs in the TiDB repositories and 25 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV']
---

# Weekly update in TiDB

Last week, we landed [39 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-02-19..2017-02-26%20) in the TiDB repositories.

## Added

* [Support Revoke statement.](https://github.com/pingcap/tidb/pull/2661)

* Add rules in parser and empty implementation for unsupported builtin functions: [#2667](https://github.com/pingcap/tidb/pull/2667), [#2677](https://github.com/pingcap/tidb/pull/2677), [#2679](https://github.com/pingcap/tidb/pull/2667)

* [Support wildcard chars in username or host in Grant statement.](https://github.com/pingcap/tidb/pull/2688)

* [Add a context arggument for distsql/kv interface:](https://github.com/pingcap/tidb/pull/2699) We will use the context to cancel running jobs.

* [Support `Create Table ... Like` statement.](https://github.com/pingcap/tidb/pull/2707)

* [Support `ON UPDATE CURRENT_TIMESTAMP` with precision](https://github.com/pingcap/tidb/pull/2714)

* [Support `Show Warnings` statement.](https://github.com/pingcap/tidb/pull/2724)

## Fixed

* [Fix memory leak when IndexScanExecutor meet error.](https://github.com/pingcap/tidb/pull/2678)

* [Add missing field length information for `show databases;`](https://github.com/pingcap/tidb/pull/2681)

* [Add missing field length information for Show statement.](https://github.com/pingcap/tidb/pull/2698)

* [Fix compatibility problme about string truncate error.](https://github.com/pingcap/tidb/pull/2685)

* [Ignore malformated data in MySQL packet.](https://github.com/pingcap/tidb/pull/2692)

* [Fix a bug about topn operator pushdown.](https://github.com/pingcap/tidb/pull/2693)

* [Fix a bug about add column with default value and not null flag.](https://github.com/pingcap/tidb/pull/2703)

## Improved

* [Prune correlated columns in groupby item list.](https://github.com/pingcap/tidb/pull/2568) 

* [Imporve the performance of point get query using primary key or unique key by 3%.](https://github.com/pingcap/tidb/pull/2631)

* [Decorrelated for aggregation.](https://github.com/pingcap/tidb/pull/2682)

# Weekly update in TiKV

Last week, We landed [25 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-02-19..2017-02-25+&type=Issues&ref=searchresults) in the TiKV repositories.

## Added

* [Detect system CPU/memory](https://github.com/pingcap/tikv/pull/1605) to adjust config automatically. 

* Add [RocksDB statistics](https://github.com/pingcap/tikv/pull/1606).

* Balance store according to [region count](https://github.com/pingcap/pd/pull/506).

* Add [`label`](https://github.com/pingcap/pd/pull/530), [`ping`](https://github.com/pingcap/pd/pull/534) , [`admin`](https://github.com/pingcap/pd/pull/536), [`scheduler`](https://github.com/pingcap/pd/pull/537), [`operator`](https://github.com/pingcap/pd/pull/539) commands for `pd-ctl`.

* Add [shuffle region](https://github.com/pingcap/pd/pull/538) scheduler.

## Fixed

* [Verify PD address](https://github.com/pingcap/pd/pull/528) when start `pd-ctl`.

* [Reject read index](https://github.com/pingcap/tikv/pull/1634) when new leader hasn’t committed the empty entry.

* [Accelerate campaign](https://github.com/pingcap/tikv/pull/1640) faster after split happens. 

* [Use default value](https://github.com/pingcap/tikv/pull/1644) in column info.

## Improved

* Save one TS get for [single point get](https://github.com/pingcap/tikv/pull/1608) by unique or primary key. 

* Prettfiy [command label](https://github.com/pingcap/pd/pull/520) name in metrics.  

* Make Raft [apply atomically](https://github.com/pingcap/tikv/pull/1648).

* Add [region ID](https://github.com/pingcap/tikv/pull/1654) for scheduler slow log.
