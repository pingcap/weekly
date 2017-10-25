---
date: 2017-06-05T00:00:00Z
title: Weekly Update
url: /2017/06/05/tidb-weekly/
---

## Weekly update in TiDB

Last two weeks, we landed [53 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-05-22..2017-06-04%20) in the TiDB repositories.

## Added

* [Support using `After` and `First` to specify column position in the `Alter Table` Statement.](https://github.com/pingcap/tidb/pull/3215)

* [Support the `password` builtin function.](https://github.com/pingcap/tidb/pull/3275)

* [Support the `inet6_ntoa` builtin function.](https://github.com/pingcap/tidb/pull/3333)

* [Support the `Extract` and `Unquote` function for Json.](https://github.com/pingcap/tidb/pull/3353)

* [Support  `json_{set/insert/replace}` and `json_merge` for Json.](https://github.com/pingcap/tidb/pull/3374)

* [Support batched `Index Lookup Join`.](https://github.com/pingcap/tidb/pull/3306)


## Fixed

* [Fix a goroutine leak problem.](https://github.com/pingcap/tidb/pull/3291)

* [Fix a bug in double read executor.](https://github.com/pingcap/tidb/pull/3316)

* [Fix a bug for type inferrer of Bit literal value.](https://github.com/pingcap/tidb/pull/3317)

* [Fix a bug about context cancellation.](https://github.com/pingcap/tidb/pull/3330)

## Improved

* Refactor expression evaluation:
  - [Refactor the `cast` function.](https://github.com/pingcap/tidb/pull/3266)
  - [Add the `GetTypeClass()` interface in Expression.](https://github.com/pingcap/tidb/pull/3321)

* [Update stored password in `mysql.user` table ](https://github.com/pingcap/tidb/pull/3292) to make it consistent with MySQL.

* Speed up the DDL process: 
    - [Use etcd to synchronise schema version instead of waiting two leases.](https://github.com/pingcap/tidb/pull/3322)
    - [Enable DDL speed up.](https://github.com/pingcap/tidb/pull/3367)

* [Add the `references_priv` column in `mysql.user`.](https://github.com/pingcap/tidb/pull/3343)

* [Close DDL worker gracefully when shutting down the TiDB server.](https://github.com/pingcap/tidb/pull/3349)


## Weekly update in TiKV

Last two weeks, We landed [33 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-05-21..2017-06-03&type=Issues) in the TiKV repositories.

## Added

* Introduce gRPC, see [1850](https://github.com/pingcap/tikv/pull/1850), [1865](https://github.com/pingcap/tikv/pull/1865), [1868](https://github.com/pingcap/tikv/pull/1868), [1879](https://github.com/pingcap/tikv/pull/1879).
* Report the [written keys](https://github.com/pingcap/tikv/pull/1820) to PD for better scheduler. 
* Balance the [hot regions](https://github.com/pingcap/pd/pull/638) by peer and leader together. 
* Record the cluster [bootstrap time](https://github.com/pingcap/pd/pull/645).
* Add the [state](https://github.com/pingcap/pd/pull/647) for operators. 
* Add the [metrics](https://github.com/pingcap/pd/pull/648) for balance.
* Add the [disaster recovery](https://github.com/pingcap/pd/pull/650) tool for PD.
* Output the [allocation statistics](https://github.com/pingcap/tikv/pull/1877) when receiving SIGUSR1.
* Add the [direct IO](https://github.com/pingcap/tikv/pull/1878) configuration for RocksDB.

## Fixed

* [Check the cluster ID](https://github.com/pingcap/tikv/pull/1842) when re-connecting to PD. 
* Reuse the [timer](https://github.com/pingcap/tikv/pull/1856) to avoid spawning thread frequently.
* Remove the [realtime](https://github.com/pingcap/tikv/pull/1862) signal handler. 
* Prevent [accessing nil store](https://github.com/pingcap/pd/pull/651) when recovering cluster. 
* Check the environment [TZ](https://github.com/pingcap/tikv/pull/1876) setting. 
* Use the [forward](https://github.com/pingcap/tikv/pull/1880) mode for scanning data in GC command. 
* Check  the [last apply](https://github.com/pingcap/tikv/pull/1885) index to determine handing snapshot.

## Improved

* Increase the [region size](https://github.com/pingcap/tikv/pull/1449) from 64 MB to 96 MB. 
* Split total [region peer cache](https://github.com/pingcap/tikv/pull/1859).
* Use [FlatMap](https://github.com/pingcap/tikv/pull/1861) instead of HashMap to improve performance.
* Modify the [default compression](https://github.com/pingcap/tikv/pull/1875) in RocksDB.