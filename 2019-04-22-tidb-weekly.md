---
title: Weekly update (April 15 ~ April 21, 2019)
date: 2019-04-22
summary: Last week, we landed 28 PRs in the TiDB repository, 11 PRs in the TiSpark repository, and 27 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [28 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-04-15..2019-04-21+) in the TiDB repository.

## Added

- [Support `show global bind`](https://github.com/pingcap/tidb/pull/10200)
- [Support `drop global binding`](https://github.com/pingcap/tidb/pull/10193)
- [Support `create global binding`](https://github.com/pingcap/tidb/pull/9846)
- [Support `show open tables` with empty results](https://github.com/pingcap/tidb/pull/10166)
- [Add the role support for `SHOW GRANT`](https://github.com/pingcap/tidb/pull/10016)
- [Support `SET DEFAULT ROLE`](https://github.com/pingcap/tidb/pull/9949)
- [Support the `JSON_SEARCH` built-in function](https://github.com/pingcap/tidb/pull/8704)

## Improved

- [Speed up decoding the column ID](https://github.com/pingcap/tidb/pull/10188)
- [Adapt the `utf8mb4_0900_ai_ci` collation](https://github.com/pingcap/tidb/pull/10183)
- [Show more information about Coprocessor tasks in slow query logs](https://github.com/pingcap/tidb/pull/10165)
- [Show memory consumption in slow query logs](https://github.com/pingcap/tidb/pull/10162)
- [Add a memory table to store hot Region information](https://github.com/pingcap/tidb/pull/10106)
- [Show `StatsVersion` of the table in slow query logs](https://github.com/pingcap/tidb/pull/10082)
- [Support `ConstItem()` for expressions to test if it is a constant](https://github.com/pingcap/tidb/pull/10004)

## Fixed

- [Fix wrong results caused by splitting ranges inappropriately in some cases](https://github.com/pingcap/tidb/pull/10179)
- [Fix the stack overflow issue caused by folding constants in some cases](https://github.com/pingcap/tidb/pull/10174)
- [Fix the issue that the bad null error is ignored when disabling the strict SQL mode](https://github.com/pingcap/tidb/pull/10161)
- [Fix a race when recreating the batch-commands client when TiKV crashes](https://github.com/pingcap/tidb/pull/10143)
- [Fix wrong results caused by pruning unfoldable expressions in `order by`](https://github.com/pingcap/tidb/pull/10064)


# Weekly update in TiSpark

Last week, we landed [11 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-04-15..2019-04-21+) in the TiSpark repository.

## Added

- [Add a `tidb-adapter` plugin to use TiDB as a metastore](https://github.com/pingcap/tispark/pull/651)
- [Support `Spark 2.3.x` by reflection rather than profile](https://github.com/pingcap/tispark/pull/660)

## Fixed

- [Fix a partition parser bug when encountering `ZERO_DECIMAL`](https://github.com/pingcap/tispark/pull/651)
- [Fix a bug in unsupported partition expressions](https://github.com/pingcap/tispark/pull/667)
- [Fix the issue that the prefix length is larger than the value used in reality](https://github.com/pingcap/tispark/pull/668)

## Improved

- [Add the Spark version in TiSpark version description](https://github.com/pingcap/tispark/pull/650)

# Weekly update in TiKV and PD

Last week, we landed [27 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-04-15..2019-04-21&type=Issues) in the TiKV and PD repositories.

## Added

* [Add the batch aggregation framework](https://github.com/tikv/tikv/pull/4533)
* [Add `rocksdb.num-immutable-mem-table`](https://github.com/tikv/tikv/pull/4528)
* [Support scattering Regions and get the operator status](https://github.com/pingcap/pd/pull/1501)
* [Make properties index distance configurable](https://github.com/tikv/tikv/pull/4517)
* [Add `ret_field_type`](https://github.com/tikv/tikv/pull/4512)

## Improvement

* [Move `kvGet` to the `util` package](https://github.com/pingcap/pd/pull/1513)
* [Use `builder` to build the field type](https://github.com/tikv/tikv/pull/4546)
* [Add comments for several modules](https://github.com/tikv/tikv/pull/4545)
* [Clean up util and engine components](https://github.com/tikv/tikv/pull/4543)
* [Use `KeyBuilder` to reduce memory allocation and copy bound keys](https://github.com/tikv/tikv/pull/4537)
* [Use `bitflag` to replace bool](https://github.com/tikv/tikv/pull/4536)
* [Adapt the `BatchLimitExecutor` style to other batch executors](https://github.com/tikv/tikv/pull/4534)
* [Move `build` related functions to `DAGBuilder`](https://github.com/tikv/tikv/pull/4527)
* [Make executor summary collector work easier](https://github.com/tikv/tikv/pull/4498)
* [Move the logic of checking the availability of batch execution to the executor](https://github.com/tikv/tikv/pull/4483)

## Fixed

* [Make `tidy` check only module files](https://github.com/pingcap/pd/pull/1510)
* [Add the default HTTP prefix for the detaching mode](https://github.com/pingcap/pd/pull/1509)
* [Make `LoadRange` return both keys and values](https://github.com/pingcap/pd/pull/1508)
* [Retry updating the leader when initializing the PD client](https://github.com/pingcap/pd/pull/1507)
* [Update the copyright](https://github.com/tikv/tikv/pull/4531)
* [Remove repeated content](https://github.com/tikv/tikv/pull/4529)
* [Make `TestBalance` of the `hot-write-region` scheduler stable](https://github.com/pingcap/pd/pull/1503)
* [Accept multiple PK handles in the request](https://github.com/tikv/tikv/pull/4499)
* [Check the iterator status when the iterator is invalid](https://github.com/tikv/tikv/pull/4470)
* [Import data after all Regions are scattered](https://github.com/tikv/tikv/pull/4423)

# New contributors (Thanks!)

tikv:

- [b41sh](https://github.com/b41sh)

tidb-operator:

- [cofyc](https://github.com/cofyc)

parser:

- [Ryan-Git](https://github.com/Ryan-Git)
- [pingyu](https://github.com/pingyu)

docs:

- [philip](https://github.com/philip)