---
title: Weekly update (July 22 ~ July 28, 2019)
date: 2019-07-29
summary: Last week, we landed 102 PRs in the TiDB repository, 4 PRs in the TiSpark repository, and 27 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [102 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-07-22..2019-07-28+) in the TiDB repository.

## Added

- [Support subqueries in the `SHOW` statement](https://github.com/pingcap/tidb/pull/10942)
- [Add support for the `octet_length` function](https://github.com/pingcap/tidb/pull/11451)
- [Introduce `Sel` to `Chunk` to indicate which rows are selected](https://github.com/pingcap/tidb/pull/11384)
- [Add the methods of vectorized data access to `Column`](https://github.com/pingcap/tidb/pull/11368)
- [Add `opt_rule_blacklist` in `mysql` tables](https://github.com/pingcap/tidb/pull/11096)

## Improved

- [Handle the partitioned table in some HTTP APIs](https://github.com/pingcap/tidb/pull/11463)
- [Improve compatibility with mysql when`datatime` is invalid](https://github.com/pingcap/tidb/pull/11445)
- [Show `CARTESIAN Join` explicitly in the results of `Explain`](https://github.com/pingcap/tidb/pull/11415)
- [Change the `toErr` logic in `executor/ddl.go`](https://github.com/pingcap/tidb/pull/11308)
- [Reduce the lock conflict between sending message and re-creating streaming clients](https://github.com/pingcap/tidb/pull/11301)
- [Support more `Analyze` options](https://github.com/pingcap/tidb/pull/11278)
- [Reduce the allocation and release of memory for `load data` and `batch insert`](https://github.com/pingcap/tidb/pull/11284)

## Fixed

- [Fix the overflow of the built-in `add_date`/`sub_date` functions](https://github.com/pingcap/tidb/pull/11472)
- [Fix the panic when dumping pseudo columns](https://github.com/pingcap/tidb/pull/11430)
- [Fix the issue that `current_timestamp`/`now` are not consistent in one stmt like in MySQL](https://github.com/pingcap/tidb/pull/11392)
- [Fix the issue that `floatStrToIntStr` fails in some cases](https://github.com/pingcap/tidb/pull/11376)
- [Disallow dropping indexes on the `auto_increment` column](https://github.com/pingcap/tidb/pull/11360)
- [Fix the bug of `uint64` overflow in `ConvertJSONToFloat`](https://github.com/pingcap/tidb/pull/11355)
- [Fix the generation of the field name](https://github.com/pingcap/tidb/pull/11324)
- [Reject the invalid conversion from `like` to `=`](https://github.com/pingcap/tidb/pull/11320)
- [Fix a bug in the column charset and `collate` when creating tables and modifying columns](https://github.com/pingcap/tidb/pull/11300)
- [Fix the bug of `REVOKE ROLE`](https://github.com/pingcap/tidb/pull/11273)
- [Fix bugs and make the rule of outer join elimination more effective](https://github.com/pingcap/tidb/pull/11160)
- [Fix the issue that `autoid` does not handle the float and double types](https://github.com/pingcap/tidb/pull/11110)
- [Fix the compatibility issue of the `auto_increment` column in the `INFORMATION_SCHEMA.TABLES` table](https://github.com/pingcap/tidb/pull/10207)

# Weekly update in TiSpark

Last week, we landed [4 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-07-22..2019-07-28+) in the TiSpark repository.

## Added

- [Add the Spark version to TiSpark `UDF ti_version()`](https://github.com/pingcap/tispark/pull/943)

# Weekly update in TiKV and PD

Last week, we landed [27 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-07-22..2019-07-28&type=Issues) in the TiKV and PD repositories.

## Improved

- [Add more details about the gRPC `ResourceExhausted` failure](https://github.com/tikv/tikv/pull/5126)
- [Separate the interfaces of Coprocessor statistics](https://github.com/tikv/tikv/pull/5121)
- [Rename `follower read`](https://github.com/tikv/tikv/pull/5118)
- [Make the RocksDB aware of `jemalloc`](https://github.com/tikv/tikv/pull/5117)
- [Change the outputs of errors, panics, and logs from `Debug` to `Display`](https://github.com/tikv/tikv/pull/5114)
- [Use `into` rather than explicitly using `RepeatedField`](https://github.com/tikv/tikv/pull/5112)
- [Use an individual package for `tso`](https://github.com/pingcap/pd/pull/1628)
- [Use an individual package for the ID allocator](https://github.com/pingcap/pd/pull/1623)
- [Return a Region error when TiKV is closing](https://github.com/tikv/tikv/pull/4820)
- [Improve `rust-rocksdb`](https://github.com/tikv/tikv/pull/5139)

## Added

- [Introduce the trait of Coprocessor `Storage`](https://github.com/tikv/tikv/pull/5129)
- [Add a retry mechanism for `join`](https://github.com/pingcap/pd/pull/1643)
- [Migrate implementation and test for the `DateFormatSig` RPN Function](https://github.com/tikv/tikv/pull/5097)
- [Add the `convert *` functions to the decimal](https://github.com/tikv/tikv/pull/5029)
- [Add the `convert *` functions to the float](https://github.com/tikv/tikv/pull/4998)

## Fixed

- [Fix the issue that the `merge region` API is added](https://github.com/pingcap/pd/pull/1653)
- [Fix the wrong constraint check when `txn` is overlapping](https://github.com/tikv/tikv/pull/5128)
- [Fix the scatter range](https://github.com/pingcap/pd/pull/1650)
- [Fix a compatibility issue for `protos`](https://github.com/tikv/tikv/pull/5125)
- [Fix `ScanRegions`](https://github.com/pingcap/pd/pull/1648)
- [Remove the remaining references of `tikv-importer`](https://github.com/tikv/tikv/pull/5123)
- [Copy `/health` and `/diagnose` to `/api/{version}` and deprecate the old ones](https://github.com/pingcap/pd/pull/1647)
- [Ease the transition to Prost](https://github.com/tikv/tikv/pull/5120)
- [Fix the compilation errors when running `make fail_release`](https://github.com/tikv/tikv/pull/5115)
- [Fix the scatter range](https://github.com/pingcap/pd/pull/1642)
- [Fix bugs in `pd-simulator`](https://github.com/pingcap/pd/pull/1635)

# New contributors (Thanks!)

tikv:

- [lucab](https://github.com/lucab)

tidb:

- [unknwon](https://github.com/unknwon)
- [wty4427300](https://github.com/wty4427300)

parser:

- [gleonid](https://github.com/gleonid)
