---
title: TiDB Monthly Update (February 2021)
date: 2021-03-01
summary: Here's what TiDB has achieved in February 2021.
tags: ['TiDB', 'TiUP', 'TiDB Dashboard', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Monthly Update for February 2021

## Releases

We have two releases this month:

[TiDB 4.0.11 release notes](https://docs.pingcap.com/tidb/stable/release-4.0.11)

+ New features

    - Support the `utf8_unicode_ci` and `utf8mb4_unicode_ci` collations
    - Support the `cast_year_as_time` collation
    - Add a Coprocessor thread pool to queue Coprocessor requests for execution, which avoids out of memory (OOM) in some cases, and add the `cop_pool_size` and `batch_cop_pool_size` configuration items with the default values of `NumOfPhysicalCores * 2`

+ Improvements

    - Reorder inner joins that are simplified from outer joins
    - Add metrics of server information for DBaaS
    - Report RocksDB metrics to TiDB

+ Bug fixes

[TiDB Operator 1.1.11 release notes](https://docs.pingcap.com/tidb-in-kubernetes/stable/release-1.1.11)

+ New features

    - Support configuring durations for leader election
    - Add the `tidb_cluster` label for the scrape jobs in TidbMonitor to support monitoring multiple clusters
    - Support setting customized store labels according to the node labels

+ Improvements

    - Add TiFlash rolling upgrade logic to avoid all TiFlash stores being unavailable at the same time during the upgrade
    - Retrieve the Region leader count from TiKV Pod directly instead of from PD to get the accurate count

## Blog posts

Wenbo Zhang's article [Linux Kernel vs. Memory Fragmentation (Part I)](https://pingcap.com/blog/linux-kernel-vs-memory-fragmentation-1) introduced some common extensions to the buddy allocator that helped prevent memory fragmentation in the Linux 3.10 kernel, the principle of memory compaction, how to view the fragmentation index, and how to quantify the latency overheads caused by memory compaction.

In [TiGraph: 8,700x Computing Performance Achieved by Combining Graphs + the RDBMS Syntax](https://pingcap.com/blog/tigraph-8700x-computing-performance-achieved-by-combining-graphs-+-rdbms-syntax), Heng Long, Shuang Chen, and Wenjun Huang, the second prize winners of TiDB Hackathon 2020, shared TiGraph's architecture, its benchmarks, their project innovations, potential uses for TiGraph, and their future plans.

JD Cloud database team wrote an article [TiDB on JD Cloud: A Cloud-native Distributed Database Service](https://pingcap.com/blog/tidb-on-jd-cloud-a-cloud-native-distributed-database-service) to introduce Cloud-TiDB, a distributed database service on the cloud in cooperation with PingCAP.

Leitao Guo, the database and middleware manager at iQIYI in his article [How to Efficiently Choose the Right Database for Your Applications](https://pingcap.com/blog/how-to-efficiently-choose-the-right-database-for-your-applications) shared with you what criteria to use for selecting a database, what databases they used at iQIYI, some decision models to help you efficiently pick a database, and tips for choosing your database.

In [Celebrating One Year of Chaos Mesh: Looking Back and Ahead](https://pingcap.com/blog/celebrating-one-year-of-chaos-mesh-looking-back-and-ahead), Cwen Yin and Calvin Weng shared with you how Chaos Mesh had grown and changed in the past year and also discussed its future goals and plans.

## Important pull requests

### Planner

+ [Support scanning the `Enum` index](https://github.com/pingcap/tidb/pull/22691)
+ [Merge the partition-level histograms to a global-level histogram](https://github.com/pingcap/tidb/pull/22603)

### SQL-Infra

+ [Support the status command of MySQL Shell](https://github.com/pingcap/tidb/pull/22752)

### Execution

+ [Fix bugs in the logic of `builtinfunction ArithmeticMinusInt`](https://github.com/pingcap/tidb/pull/22426)
+ [Refactor the `RestrictedSQLExecutor` interface](https://github.com/pingcap/tidb/pull/22579)

### Kubernetes

+ [Make sure that the TiFlash service is available during upgrade](https://github.com/pingcap/tidb-operator/pull/3789)
+ [Retrieve the Region leader count from TiKV during upgrade](https://github.com/pingcap/tidb-operator/pull/3801)

### Migrate

+ [Merge the TiDB Lightning code into the `br` repository](https://github.com/pingcap/br/pull/665)
+ [Automatically switch Data Migration (DM)'s replication source or replica](https://github.com/pingcap/dm/pull/1364)

### TiUP

+ [Upgrade code to fit Golang v1.16](https://github.com/pingcap/tiup/pull/1151)

## Important issues

### Planner

+ [To fix the issue that the prefix column in the secondary index in the clustered index table might return wrong results](https://github.com/pingcap/tidb/issues/22960)

### SQL-Infra

+ [To truncate partition results in the incorrect schema diff](https://github.com/pingcap/tidb/issues/22819)

### Execution

+ [To fix the performance regression on TPC-H multiple queries](https://github.com/pingcap/tidb/issues/22881)
+ [To fix the issue that the aggregation function `COUNT(NULL)` returns an error](https://github.com/pingcap/tidb/issues/22629)

### Kubernetes

+ [To handle multiple PVC cases during scaling](https://github.com/pingcap/tidb-operator/issues/3802)

### Migrate

+ [To fix the TiCDC issue that the log folder name is unstable when `CREATE` and `DROP` operations are performed, which affects BR restore using `cdclog`](https://github.com/pingcap/ticdc/issues/1415)

### TiUP

+ [Add support for `darwin`/`arm64` (Apple M1)](https://github.com/pingcap/tiup/issues/1122)

## Call for participations

### Planner

+ [To fix the issue that the current statistics histogram of a multi-column index actually serves as a single column index](https://github.com/pingcap/tidb/issues/22589)

### SQL-Infra

+ [To fix the error returned when executing `show table regions`](https://github.com/pingcap/tidb/issues/22794)

### Kubernetes

+ [To deprecate the Pod validating and mutating webhook](https://github.com/pingcap/tidb-operator/issues/3497)
+ [To fix the `MaxBackups` behavior on `BackupSchedule`](https://github.com/pingcap/tidb-operator/issues/3660)

### Migrate

+ [To fix the DM issue that the content in the `cfg` field is not pretty printed](https://github.com/pingcap/dm/issues/1429)

### TiUP

+ [To resume rollback or checkpoint if DM's scale-out fails](https://github.com/pingcap/tiup/issues/1113)

## New contributors

We'd like to welcome the following new contributors to TiDB and thank them for their work!

tidb:

+ [Lifeistrange](https://github.com/Lifeistrange)
+ [yzwqf](https://github.com/yzwqf)
+ [LindaSummer](https://github.com/LindaSummer)
+ [krzysztofpioro](https://github.com/krzysztofpioro)
+ [qian9qian10](https://github.com/qian9qian10)
+ [hidehalo](https://github.com/hidehalo)

tikv:

+ [SSebo](https://github.com/SSebo)
+ [Hexilee](https://github.com/Hexilee)
+ [skyzh](https://github.com/skyzh)
+ [trabbart](https://github.com/trabbart)

pd:

+ [wangrzneu](https://github.com/wangrzneu)
+ [Sullivan12138](https://github.com/Sullivan12138)
+ [wq1019](https://github.com/wq1019)
+ [ccw1996](https://github.com/ccw1996)

tidb-dashboard:

+ [zzh-wisdom](https://github.com/zzh-wisdom)

client-rust:

+ [weihanglo](https://github.com/weihanglo)

dm:

+ [Kuri-su](https://github.com/Kuri-su)

chaos-mesh:

+ [Gallardot](https://github.com/Gallardot)
+ [vincent178](https://github.com/vincent178)
+ [AngleNet](https://github.com/AngleNet)
