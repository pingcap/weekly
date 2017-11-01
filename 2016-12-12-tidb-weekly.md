---
title: Weekly update (December 05 ~ December 11, 2016)
date: 2016-12-12
summary: Last week, we landed 41 PRs in the TiDB repositories and 34 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV']
---

# Weekly update in TiDB

Last week, we landed [41 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-12-05..2016-12-11%20) in the TiDB repositories.

## Added

+ [Support the built-in function: `str_to_date`. ](https://github.com/pingcap/tidb/pull/2078) 

+ [Support built-in function schema().](https://github.com/pingcap/tidb/pull/2173)

+ [Support pushing the `case-when` expression to TiKV.](https://github.com/pingcap/tidb/pull/2171)

+ [Support changing the type and name of a column.](https://github.com/pingcap/tidb/pull/2174)

+ [Add the `](https://github.com/pingcap/tidb/pull/2194)[session_variables` and `plugins` of memory table to infoschema.](https://github.com/pingcap/tidb/pull/2194)

+ [Make the `union all` operator run parallelly.](https://github.com/pingcap/tidb/pull/2195)

+ [Support explaining the `union` statement.](https://github.com/pingcap/tidb/pull/2216)

## Fixed

+ [A bug that causes infinite loop.](https://github.com/pingcap/tidb/pull/2163)

+ [A bug in the `on duplicate…` statement when updating the primary key (PK)](https://github.com/pingcap/tidb/pull/2179)

+ [Make the charset name case-insensitive.](https://github.com/pingcap/tidb/pull/2184)

+ [Forbid dropping columns with the `auto_inc` and `PK` attribute.](https://github.com/pingcap/tidb/pull/2203)

+ [Fix bugs in the parser.](https://github.com/pingcap/tidb/pull/2210)

## Improved

+ [Pass the filter to TiKV when scanning indexes.](https://github.com/pingcap/tidb/pull/2166)

+ [Allocate column/index IDs in the table space](https://github.com/pingcap/tidb/pull/2205) to make the IDs shorter.

# Weekly update in TiKV

Last week, we landed [34 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2016-12-04..2016-12-10&type=Issues&ref=searchresults) in the TiKV repositories.

## Added

+ Support [online backup](https://github.com/pingcap/tikv/pull/1355) of the RocksDB data for `tikv-ctl` debugging. 

+ Add [replication constraints](https://github.com/pingcap/pd/pull/402) to schedule replicas. 

+ Support [`GrantLeaderScheduler`](https://github.com/pingcap/pd/pull/406) to transfer all leaders to one store. 

+ Support [`ShuffleLeaderScheduler`](https://github.com/pingcap/pd/pull/409) to shuffle leaders in different stores. 

+ Support Circle CI for [TiKV](https://github.com/pingcap/tikv/pull/1384) and [Placement Driver (PD)](https://github.com/pingcap/pd/pull/412).

+ Add the [state filter argument](https://github.com/pingcap/pd/pull/425) to get the stores API.

## Fixed

+ [Use `channel`](https://github.com/pingcap/tikv/pull/1375) to fix the possible stale snapshot state, issue [#1373](https://github.com/pingcap/tikv/issues/1373).

+ Report [`ServerIsBusy`](https://github.com/pingcap/tikv/pull/1390) and let [PD ignore the busy store](https://github.com/pingcap/pd/issues/420) when scheduling to fix [#414](https://github.com/pingcap/pd/issues/414).

## Improved

+ [Speed up the shutdown duration](https://github.com/pingcap/tikv/pull/1385) to reduce the close waiting time. 

+ [Add retry](https://github.com/pingcap/pd/pull/417) when initializing the cluster ID.

+ Support [safe ConfChange](https://github.com/pingcap/tikv/pull/1398) to fix [#1366](https://github.com/pingcap/tikv/issues/1366). 

+ [Report pending peers](https://github.com/pingcap/tikv/pull/1395) to PD to improve its scheduler. 

+ [Bind ports lazily](https://github.com/pingcap/tikv/pull/1400) to avoid the message channel full error when starting up.

