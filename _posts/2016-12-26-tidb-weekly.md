# New Release

[TiDB RC1](https://github.com/pingcap/tidb/releases/tag/rc1) is released! 

## Weekly update in TiDB

Last week, we landed [34 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-12-19..2016-12-25%20) in the TiDB repositories.

## Added

* [Support the `RPAD` built-in function.](https://github.com/pingcap/tidb/pull/2270).

* [Support the `show keys from table from database` statement.](https://github.com/pingcap/tidb/pull/2308) 

## Fixed

* [Retry infinite times if the commit primary key times out.](https://github.com/pingcap/tidb/pull/2276)

* [Do not push aggregation down to the memory tables.](https://github.com/pingcap/tidb/pull/2296)

* [Fix a bug about the `alter table` statement](https://github.com/pingcap/tidb/pull/2297).

## Improved

* Refactor the time type related code: [#2259](https://github.com/pingcap/tidb/pull/2259), [#2280](https://github.com/pingcap/tidb/pull/2280), [#2284](https://github.com/pingcap/tidb/pull/2284), #2289, [#2292](https://github.com/pingcap/tidb/pull/2292)

* Refactor optimizer: [extract initialization related code into physical Initialization.](https://github.com/pingcap/tidb/pull/2263)

* [Speed up the DDL statement.](https://github.com/pingcap/tidb/pull/2268)

* [Avoid generating `parser.go` every time.](https://github.com/pingcap/tidb/pull/2281)

* [Skip the constraint check ](https://github.com/pingcap/tidb/pull/2288)for prewrite to improve the loading data speed. 

* [Speed up the `add index` statement.](https://github.com/pingcap/tidb/pull/2309)

## New contributor

* [silentred](https://github.com/silentred)

# Weekly update in TiKV

Last week, We landed [14 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2016-12-18..2016-12-25&type=Issues&ref=searchresults) in the TiKV repositories.

## Added

* Add configuration to control the [replica scheduling speed](https://github.com/pingcap/pd/pull/426). 

* [Skip constraint check](https://github.com/pingcap/tikv/pull/1411) for prewrite to improve the loading data speed. 

* Add [region and store commands](https://github.com/pingcap/pd/pull/439) to pd-ctl.

* Add [configuration](https://github.com/pingcap/tikv/pull/1422) to cache index and filter blocks in the block cache.

## Fixed

* [Report snapshot](https://github.com/pingcap/tikv/pull/1394) sending status reliably to fix [#1377](https://github.com/pingcap/tikv/issues/1377).

* Store [short value](https://github.com/pingcap/tikv/pull/1407) in write cf directly to save space and improve performance.

## Improved

* Remove unnecessary [admin operators](https://github.com/pingcap/pd/pull/427). 

* Handle Raft ready [append log](https://github.com/pingcap/tikv/pull/1420)[ in one WriteBatch](https://github.com/pingcap/tikv/pull/1420) to reduce the CPU usage and improve performance. 

* [Remove the down peer first](https://github.com/pingcap/pd/pull/446) when scheduling replicas.

