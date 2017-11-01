---
title: Weekly update (November 28 ~ December 04, 2016)
date: 2016-12-05
summary: Last week, we landed 48 PRs in the TiDB repositories and 6 PRs in the TiDB docs repositories.
tags: ['TiDB', 'TiKV']
---

# Weekly update (November 28 ~ December 04, 2016)

Last week, we landed [48 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-11-28..2016-12-04) in the TiDB repositories and [6 PRs](https://github.com/pingcap/docs/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-11-28..2016-12-04%20) in the TiDB docs repositories.

## Added

+ [Support the built-in function: str\_to\_date. ](https://github.com/pingcap/tidb/pull/2078) 

+ Refactor the time structure: [Introduce a `TimeInternal` interface to replace the go time representation.](https://github.com/pingcap/tidb/pull/2098)

+ [Add the raw Key-Value API ](https://github.com/pingcap/tidb/pull/2101) and make TiKV a raw Key-Value engine. 

+ [Add a bench tool for the raw Key-Value ](https://github.com/pingcap/tidb/pull/2109)[API](https://github.com/pingcap/tidb/pull/2101).

+ [Support the PARTITION keyword](https://github.com/pingcap/tidb/pull/2115): parsed but ignored.

+ [Support the `Alter User` statement to change user’s password.](https://github.com/pingcap/tidb/pull/2144)

+ [Support the `set password = pwd;` statement.](https://github.com/pingcap/tidb/pull/2155)

+ [Use circleci.](https://github.com/pingcap/tidb/pull/2154)

## Fixed

+ [Check duplicate column names when adding index.](https://github.com/pingcap/tidb/pull/2103)

+ [Check duplicate index columns when creating table.](https://github.com/pingcap/tidb/pull/2123)

+ [Fix a bug when `join` exists in subquery.](https://github.com/pingcap/tidb/pull/2106)

+ [Make the `schema out of date` error retry automatically within TiDB.](https://github.com/pingcap/tidb/pull/2110)

+ [Fix a typo in the `INFORMATION_SCHEMA.COLUMNS` table.](https://github.com/pingcap/tidb/pull/2126)

+ [Fix the `date_format` type infer bug.](https://github.com/pingcap/tidb/pull/2152)

+ [Do not prune the `set variable` expression in projection.](https://github.com/pingcap/tidb/pull/2160)

## Improved

+ [Update the template for new issue.](https://github.com/pingcap/tidb/pull/2131)

+ [Use the statement context to handle truncated error.](https://github.com/pingcap/tidb/pull/2147)

+ [Push the aggregate operator down under union all.](https://github.com/pingcap/tidb/pull/2150) 

## Document change

The following guides are updated:

* [TiDB Binary Deployment](https://github.com/pingcap/docs/blob/master/op-guide/binary-deployment.md)

* [TiDB Docker Deployment](https://github.com/pingcap/docs/blob/master/op-guide/docker-deployment.md)

* [Compatibility with MySQL](https://github.com/pingcap/docs/blob/master/op-guide/mysql-compatibility.md)

# Weekly update in TiKV

Last week, we landed [22 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2016-11-27..2016-12-03&type=Issues&ref=searchresults) in the TiKV repositories.

## Added

+ Support [consistency check](https://github.com/pingcap/tikv/pull/1344) to find if data is corrupted or not dynamically. 

+ Add configuration to control the [max running task count](https://github.com/pingcap/tikv/pull/1361). 

+ Add the raw [Key-Value API](https://github.com/pingcap/tikv/pull/1364).

## Fixed

+ [Check the Placement Driver list](https://github.com/pingcap/tikv/pull/1201) to fix [#1186](https://github.com/pingcap/tikv/issues/1186).

+ Check whether the term is stale for the Raft command to fix [#1317](https://github.com/pingcap/tikv/issues/1317).

+ Schedule [the log Garbage Collection by size](https://github.com/pingcap/tikv/pull/1362) to fix [#1337](https://github.com/pingcap/tikv/issues/1337).

## Improved

+ Replace the score type with [resource kind](https://github.com/pingcap/pd/pull/393) to calculate the scores more easily. 

+ Replace origin concept `balance` with [`schedule`](https://github.com/pingcap/tikv/pull/1344) and simplify configurations.  

+ [Use coordinator](https://github.com/pingcap/pd/pull/398) to control the speed of different schedulers.

