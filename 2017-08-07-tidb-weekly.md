---
date: 2017-08-07T00:00:00Z
title: Weekly Update
url: /2017/08/07/tidb-weekly/
---

## Weekly update in TiDB

2017-08-07

Last week, we landed [54 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-07-31..2017-08-06%20) in the TiDB repositories.

## Added
* [Support natural join.](https://github.com/pingcap/tidb/pull/3861)
* [Add a switch for enabling cost-based optimizor.](https://github.com/pingcap/tidb/pull/3877)
* [Assign low priority for SQL with full table scan and high priority for SQL with point get.](https://github.com/pingcap/tidb/pull/3881)
* [Support `\N` which is the shotcut of null.](https://github.com/pingcap/tidb/pull/3943)
* [Support TIMESTAMP in the `get_format` function.](https://github.com/pingcap/tidb/pull/3976)
* [Add a flag to enable TCP keep-alive.](https://github.com/pingcap/tidb/pull/3995)
* [Support `DISTINCTROW`.](https://github.com/pingcap/tidb/pull/4017)

## Fixed
* [Truncate the trailing spaces for "CHAR[(M)]" types](https://github.com/pingcap/tidb/pull/3878)
* [Fix float point parsing with leading dot.](https://github.com/pingcap/tidb/pull/3964)


## Improved
* [Refactor the row structure:](https://github.com/pingcap/tidb/pull/3758) to reduce memory allocation.
* Refactor the following expression/builtin-function evaluation framework:
  - [trim](https://github.com/pingcap/tidb/pull/3936)
  - [rtrim](https://github.com/pingcap/tidb/pull/3939)
* [Check schema changing more precisely.](https://github.com/pingcap/tidb/pull/3999)
* [Adjust the cost of index join.](https://github.com/pingcap/tidb/pull/4014)

## Weekly update in TiKV

Last week, We landed [21 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-07-30..2017-08-05&type=Issues) in the TiKV repositories.

## Added

* Add [priority](https://github.com/pingcap/tikv/pull/2079) for coprocessor thread pool.
* Add [`ceil_real`](https://github.com/pingcap/tikv/pull/2105) function for coprocessor.
* Add [`remove`](https://github.com/pingcap/tikv/pull/2091) function for JSON.
* Dynamically [set label](https://github.com/pingcap/pd/pull/689) by PD API.
* Support [delete member](https://github.com/pingcap/pd/pull/695) by id.
* Add more util [functions](https://github.com/pingcap/tikv/pull/2100).

## Fixed

* Stop the [resolver thread](https://github.com/pingcap/tikv/pull/2104) explicitly.

## Improved

* Refactor the storage [configuration](https://github.com/pingcap/tikv/pull/2102) field.
* Deny the [`http` prefix](https://github.com/pingcap/tikv/pull/2101) for PD addresses.
* Refactor the [properties collector](https://github.com/pingcap/tikv/pull/2096).
* Improve the storage [test](https://github.com/pingcap/tikv/pull/2108).
* Use the [`MinOverlappingRatio`](https://github.com/pingcap/tikv/pull/2117) compaction priority by default.