---
date: 2017-04-10T00:00:00Z
title: Weekly Update
url: /2017/04/10/tidb-weekly/
---

## Weekly update in TiDB

Last two weeks, we landed [74 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-03-27..2017-04-09%20) in the TiDB repositories.

## Added

* Support Index Nest Lookup Join operator.[#2834](https://github.com/pingcap/tidb/pull/2834), [#2945](https://github.com/pingcap/tidb/pull/2945)

* Add many builtin functions: [`quote`](https://github.com/pingcap/tidb/pull/2845), [`is_ipv4`](https://github.com/pingcap/tidb/pull/2864), [`compress`](https://github.com/pingcap/tidb/pull/2879), [`inet_aton`](https://github.com/pingcap/tidb/pull/2882), [`format`](https://github.com/pingcap/tidb/pull/2883), [`bin`](https://github.com/pingcap/tidb/pull/2924 ), [`random-bytes`](https://github.com/pingcap/tidb/pull/2927), [`sin`](https://github.com/pingcap/tidb/pull/2885), [`inet_ntoa`](https://github.com/pingcap/tidb/pull/2887), [`cos, from_base64, tan, cot`](https://github.com/pingcap/tidb/pull/2977), [`to_days`](https://github.com/pingcap/tidb/pull/2983), [`timestampadd`](https://github.com/pingcap/tidb/pull/2992)

* [Check privileges for `show databases/tables` statement.](https://github.com/pingcap/tidb/pull/2934)

* Calculate distinct information in statistic module.[#2947](https://github.com/pingcap/tidb/pull/2947), [#2966](https://github.com/pingcap/tidb/pull/2966)

* [Add a switcher to split large inset transaction into multiple small transactions automatically.](https://github.com/pingcap/tidb/pull/2958)

* [Add memory table `INFORMATION_SCHEMA.USER_PRIVILEGES`.](https://github.com/pingcap/tidb/pull/2963)

* [Add memory table `INFORMATION_SCHEMA.ENGINES`.](https://github.com/pingcap/tidb/pull/2988)

* [Support `Super_priv`.](https://github.com/pingcap/tidb/pull/2990)

* [Support Top-N operator push down in optimizer.](https://github.com/pingcap/tidb/pull/2997)


## Fixed

* [Fix case-when expression and coalesce expression type inference.](https://github.com/pingcap/tidb/pull/2918)

* [Fix a goroutine leak in tikv client.](https://github.com/pingcap/tidb/pull/2925)

* [Fix a bug in the `date_format` builtin function.](https://github.com/pingcap/tidb/pull/2908)

* [Fix goroutine leak in tikv client.](https://github.com/pingcap/tidb/pull/2921)

* [Reset affected rows counter when retrying SQL statement.](https://github.com/pingcap/tidb/pull/2949)

* [Recognize number literal as decimal when meet int64 overflow error.](https://github.com/pingcap/tidb/pull/2954)


## Improved

* Refactor optimizer: [Introduce TaskProfile to represent a group of physical plans.](https://github.com/pingcap/tidb/pull/2902) [Add base phyiscal plans.](https://github.com/pingcap/tidb/pull/2975)

* Refactor statistic module.[#2913](https://github.com/pingcap/tidb/pull/2913), [#2952](https://github.com/pingcap/tidb/pull/2952), [#2956](https://github.com/pingcap/tidb/pull/2956), [#2993](https://github.com/pingcap/tidb/pull/2993)

* Refactor coprocessor architecture: [table scan and index scan operator](https://github.com/pingcap/tidb/pull/2930), [aggregation operator](https://github.com/pingcap/tidb/pull/2970), [limit operator](https://github.com/pingcap/tidb/pull/3004), [top-n operator](https://github.com/pingcap/tidb/pull/3008)

* [Add sorted information for SortMergeJoin operator.](https://github.com/pingcap/tidb/pull/2931)

* [Refactor distsql package.](https://github.com/pingcap/tidb/pull/2942)

* [Reduce memory usage in HashJoin operator.](https://github.com/pingcap/tidb/pull/2957)


## New Contributors

**Thank you guys!**

* [Blame cosmos](https://github.com/kiroInn)

* [Zhao Yi Jun](https://github.com/ariesdevil)

* [Bin Liu](https://github.com/liubin)

* [Michael Belenchenko](https://github.com/Tratar)

* [Van](https://github.com/bom-d-van)

* [jinhelin](https://github.com/JinheLin)


# Weekly update in TiKV

# 2017-04-10

Last two weeks, We landed [46 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-03-26..2017-04-08&type=Issues) in the TiKV repositories.

## Added

* Add [rate limiter](https://github.com/pingcap/tikv/pull/1379) for RocksDB compaction.

* Add gRPC support for PD, see [493](https://github.com/pingcap/pd/pull/493), [590](https://github.com/pingcap/pd/pull/590), [1591](https://github.com/pingcap/tikv/pull/1591), [1712](https://github.com/pingcap/tikv/pull/1712), [1725](https://github.com/pingcap/tikv/pull/1725).

* Add RocksDB [SST](https://github.com/pingcap/tikv/pull/1618) format for snapshot.

* Show [replication configuration](https://github.com/pingcap/pd/pull/573) in `pd-ctl`. 

* Make [RocksDB info log path](https://github.com/pingcap/tikv/pull/1700) configurable. 

* Slow down balance [interval increasing speed](https://github.com/pingcap/pd/pull/585). 

* Report [disk space usage](https://github.com/pingcap/tikv/pull/1706) to PD.

* Report [region write-flow rate](https://github.com/pingcap/tikv/pull/1707) to PD.

* Show more [information for region](https://github.com/pingcap/pd/pull/589) in HTTP API.

* Output [statistics regularly](https://github.com/pingcap/pd/pull/597) for `pd-tso-bench`.

* Avoid selecting on the [same context](https://github.com/pingcap/pd/pull/604) in different Goroutines.

## Fixed

* Avoid [removing the leader peer](https://github.com/pingcap/pd/pull/580) directly. 

* Avoid open RocksDB [many times](https://github.com/pingcap/tikv/pull/1698). 

* Parse [`ALREADY_BOOTSTRAPPED`](#) error correctly, see [593](https://github.com/pingcap/pd/pull/593), [1720](https://github.com/pingcap/tikv/pull/1720).

* Use [pool](https://github.com/pingcap/pd/pull/608)￼ to store TSO request to reduce memory allocation and GC pressure.

## Improved

* [Abort `Prewrite` command](https://github.com/pingcap/tikv/pull/1652) if the transaction is rolled back before. 

* Make PD scheduler more [reliable](https://github.com/pingcap/pd/pull/560). 

* Make Raft ReadIndex more [stable](https://github.com/pingcap/tikv/pull/1703).

* Add many unit tests to improve the system stability.