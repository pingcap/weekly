---
date: 2017-10-23T00:00:00Z
title: Weekly Update
---

# Weekly update in TiDB

2017-10-23

In the last two weeks, we landed [83 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is:pr%20is:merged%20merged:2017-10-09..2017-10-22) in the TiDB repositories.

## Added
* [Support writing slow query log into separate files.](https://github.com/pingcap/tidb/pull/4804)
* [Dummy implementation for the `SHOW PROFILES` statement.](https://github.com/pingcap/tidb/pull/4795)
* [Add metrics for automatic analyzing.](https://github.com/pingcap/tidb/pull/4793)
* [Support the operation of `cancel DDL jobs`.](https://github.com/pingcap/tidb/pull/4753)
* [Add a new http status API to get meta regions.](https://github.com/pingcap/tidb/pull/4597)

## Removed
* [Remove the `self` field in `baseBuiltinFunc` completely.](https://github.com/pingcap/tidb/pull/4766)
* [Remove `foldable` from `baseBuiltinFunc`.](https://github.com/pingcap/tidb/pull/4759)

## Fixed
* [Fix a bug occurred in `select sum(float col)*0.1`](https://github.com/pingcap/tidb/pull/4854)
* [Cast types for the expression of assignments of `updateList`.](https://github.com/pingcap/tidb/pull/4850)
* [Fix a `PhysicalReader` range bug when data is `MaxInt64`.](https://github.com/pingcap/tidb/pull/4835)
* [Add `unsigned` and `zerofill` flags to field type year.](https://github.com/pingcap/tidb/issues/4830)
* [Fix a `select distinct` bug.](https://github.com/pingcap/tidb/pull/4828)
* [Fix a bug when `auto_increment` meets `unsigned`.](https://github.com/pingcap/tidb/pull/4824)
* [Change the DNV of default null column to `0`.](https://github.com/pingcap/tidb/pull/4825)
* [Correct the signature building of Values.](https://github.com/pingcap/tidb/pull/4814)
* [Add schema state check when executing the `show create table` or `analyze statistic` statement.](https://github.com/pingcap/tidb/pull/4801)
* [Set missing result field `Org_table` and `Database` to `Navicat` for MySQL compatibility.](https://github.com/pingcap/tidb/pull/4770)
* [Fix a bug in the copy function.](https://github.com/pingcap/tidb/pull/4765)
* [Fix a bug when converting time to scalar.](https://github.com/pingcap/tidb/pull/4760)
* [Fix a bug when building histograms for columns.](https://github.com/pingcap/tidb/pull/4757)
* [Fix a bug when merging sample collectors.](https://github.com/pingcap/tidb/pull/4752)
* [Fix ineffectual assignments.](https://github.com/pingcap/tidb/pull/4746)
* [Fix the issue that the `show grants` statement displays empty entries.](https://github.com/pingcap/tidb/pull/4734)
* [Set proper parent for newly projection-eliminated child.](https://github.com/pingcap/tidb/pull/4730)
* [Put RPC handler in response instead of returning it.](https://github.com/pingcap/tidb/pull/4723)
* [Quit the builtin function SLEEP when it is killed.](https://github.com/pingcap/tidb/issues/4378)
* [Fix the issue that the unsigned integer column length is not consistent with MySQL.](https://github.com/pingcap/tidb/pull/4693)
* [Add the `ParseErrorWith` function to make the parse error compatible with MySQL.](https://github.com/pingcap/tidb/pull/4238)


## Improved
* [Rename the DDL job state variable.](https://github.com/pingcap/tidb/pull/4818)
* [Rename the package `inspectkv` to `admin`.](https://github.com/pingcap/tidb/pull/4815)
* [Change reorg wait time from 1ms to 50ms.](https://github.com/pingcap/tidb/pull/4808)
* [Support int1, int2, int3, int4, int8 type syntax.](https://github.com/pingcap/tidb/pull/4803)
* [Estimate NDV more precisely.](https://github.com/pingcap/tidb/pull/4797)
* [Return MySQL error code for Unsafe SafePoint.](https://github.com/pingcap/tidb/pull/4786)
* [Estimate NDV as pseudo when its value is zero.](https://github.com/pingcap/tidb/pull/4769)
* [Make some builtin functions foldable.](https://github.com/pingcap/tidb/pull/4756)
* [Return `NULL` when error is not nil.](https://github.com/pingcap/tidb/pull/4749)
* [Improvement for multi-delete.](https://github.com/pingcap/tidb/pull/4742)
* [Split the detach process from `BuildRange`.](https://github.com/pingcap/tidb/pull/4741)
* [Use single method to set parent and children.](https://github.com/pingcap/tidb/pull/4738)
* [Use pattern match to check `dbRecord` in `mysql.db`.](https://github.com/pingcap/tidb/pull/4733)
* [Check `sc.IgnoreZeroInDate` when parsing the string or number type to date/datetime/timestamp.](https://github.com/pingcap/tidb/pull/4732)
* [Enforce errcheck in Makefile.](https://github.com/pingcap/tidb/pull/4724)
* [Open auto analyze by default.](https://github.com/pingcap/tidb/pull/4722)
* [Improve the fold constant.](https://github.com/pingcap/tidb/pull/4721)
* [Avoid type assertion for `ast.ExprNode`.](https://github.com/pingcap/tidb/pull/4710)
* [Avoid come assertion for `StmtNode`.](https://github.com/pingcap/tidb/pull/4705)
* [Use `ParseTimeFormNum` instead of `ParseTime`.](https://github.com/pingcap/tidb/pull/4706)
* [Support plan cache for the `SELECT` statement.](https://github.com/pingcap/tidb/pull/4644)

# Weekly update in TiSpark

## Added
* Add [support for explain](https://github.com/pingcap/tispark/pull/52)

## Fixed
* Fix [tispark-sql table alias problem](https://github.com/pingcap/tispark/pull/54)


# Weekly update in TiKV

In the last two weeks, We landed [46 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-10-09..2017-10-22&type=Issues) in the TiKV repositories.

## Added

* [Register classifiers by name](https://github.com/pingcap/pd/pull/799) when using namespace.
* Add the [operator priority](https://github.com/pingcap/pd/pull/804) mechanism.
* Support [setting a region to tombstone](https://github.com/pingcap/tikv/pull/2394) status.
* Add [MVCC scan](https://github.com/pingcap/tikv/pull/2335) support to debug API.
* Support [fail point](https://github.com/pingcap/tikv/pull/2354).
* Support [removing table_id/store_id](https://github.com/pingcap/pd/pull/776) from namespace.
* [Persist scheduler](https://github.com/pingcap/pd/pull/785) list to etcd.
* Support [namespace](https://github.com/pingcap/pd/pull/788)(experimental).
* Support [health check](https://github.com/pingcap/pd/pull/792) in pd-ctl.
* Store [case-insensitive labels](https://github.com/pingcap/pd/pull/794).
* Support [adding/removing region peer](https://github.com/pingcap/pd/pull/795) in pd-ctl.

## Fixed

* [Fixes typos](https://github.com/pingcap/tikv/pull/2390) in raft.
* Fix [table namespace classifier](https://github.com/pingcap/pd/pull/808).
* Fix [split check tests](https://github.com/pingcap/tikv/pull/2381).

## Improved

* [Refactor `clusterInfo`](https://github.com/pingcap/pd/pull/782).
* [Refactor the debug API](https://github.com/pingcap/tikv/pull/2377) for tikv-ctl.
* Adjust [scheduler interface](https://github.com/pingcap/pd/pull/798).
* [Reduce allocation](https://github.com/pingcap/tikv/pull/2391) in Raft.
* Report [read statistics to pd-worker](https://github.com/pingcap/tikv/pull/2337) directly.
* [Move out the PD work](https://github.com/pingcap/tikv/pull/2361) from `raftstore`.
* Use [`try`](https://github.com/pingcap/tikv/pull/2362) shorthand.
* [Move significant](https://github.com/pingcap/tikv/pull/2363) send to Raft router.
* Adjust [label checks](https://github.com/pingcap/tikv/pull/2372).
* Optimize approximate [region size](https://github.com/pingcap/tikv/pull/2375) for region heartbeat.
* Flow control based on [current writing KV count](https://github.com/pingcap/tikv/pull/2376).

