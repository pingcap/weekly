---
title: TiDB Monthly Update (May 2020)
date: 2020-06-01
summary: Here's what TiDB has achieved in May.
tags: ['TiDB', 'TiUP', 'TiDB Dashboard', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Monthly Update for May 2020

## Releases

We have three releases this month:

+ [TiDB 4.0 RC.2 Release Notes](https://pingcap.com/docs/stable/releases/release-4.0.0-rc.2/)
    + New features
        + Add support for the `BACKUP` and `RESTORE` commands to back up and restore data [#16960](https://github.com/pingcap/tidb/pull/16960)
        + Support pre-checking the data volume in a single Region before committing and pre-splitting the Region when the data volume exceeds the threshold [#16959](https://github.com/pingcap/tidb/pull/16959)
        + Support recording the `Cop_time` information in slow logs and the `SLOW_LOG` table [#16904](https://github.com/pingcap/tidb/pull/16904)
    + Bug fixes
+ [TiDB 3.0.14 Release Notes](https://pingcap.com/docs/stable/releases/release-3.0.14/)
    + New features
        + Add the schema name column and the table name column to the query results of the `ADMIN SHOW DDL JOBS` statement [16428](https://github.com/pingcap/tidb/pull/16428)
        + Enhance the `RECOVER TABLE` syntax to support recovering truncated tables [#15458](https://github.com/pingcap/tidb/pull/15458)
    + Bug fixes
+ [TiDB Operator 1.1.0 GA Release Notes](https://github.com/pingcap/tidb-operator/releases/tag/v1.1.0)

## Blog posts

Nick Cameron has written [Large Transactions in TiDB](https://pingcap.com/blog/large-transactions-in-tidb/) that describes how we implemented support for large transactions.

Fei Yang's article [TiCDC: Replication Latency in Milliseconds for 100+ TB Clusters](https://pingcap.com/blog/replication-latency-in-milliseconds-for-100-tb-clusters/) dives deep into why we built TiCDC and how we implement its key features.

In [TiDB Dashboard: Easier Troubleshooting for Distributed Databases](https://pingcap.com/blog/easier-troubleshooting-for-distributed-databases/), Wenxuan Shi, Ming Zhang, and Shuang Chen walks you through the dashboards's main widgets: Key Visualizer, SQL statement analysis, slow query viewing, cluster diagnostics, log search, and instance profiling.

## Notable pull requests

### Planner

+ [Adopt another way to estimate the cost of `join reorder`](https://github.com/pingcap/tidb/pull/17414)
+ [Add a proposal document for the clustered index feature](https://github.com/pingcap/tidb/pull/17044)
+ [Support the `IN` expression for the `Range` partition](https://github.com/pingcap/tidb/pull/17210)

### DDL

+ [Support exchanging partitions](https://github.com/pingcap/tidb/pull/17149)

### Dashboard

+ [Support persisting the Key Visualizer data](https://github.com/pingcap-incubator/tidb-dashboard/pull/449)
+ [Support customizing the public path prefix behind a reverse proxy](https://github.com/pingcap-incubator/tidb-dashboard/pull/504)
+ [Add GZIP for the static server](https://github.com/pingcap-incubator/tidb-dashboard/pull/514)
+ [Support highlighting log search keywords](https://github.com/pingcap-incubator/tidb-dashboard/pull/522)

### Execution

+ [Improve the performance of `min`/`max` aggregation functions by using the sliding window](https://github.com/pingcap/tidb/pull/16819)
+ [Add an `apply` cache to speed up `NestedLoopJoin`](https://github.com/pingcap/tidb/pull/17039)
+ [Support `GROUP_CONCAT(ORDER BY)`](https://github.com/pingcap/tidb/pull/17184)

### Tools

+ Improve the robustness of Backup & Restore (BR) [#247](https://github.com/pingcap/br/pull/247) [#298](https://github.com/pingcap/br/pull/298) [#7917](https://github.com/tikv/tikv/pull/7917)
+ [BR supports views and sequences](https://github.com/pingcap/br/pull/242)
+ [TiCDC supports the cyclic replication](https://github.com/pingcap/ticdc/pull/509)
+ [TiDB Data Migration (DM) supports the leader eviction](https://github.com/pingcap/dm/pull/670)

### Transaction

+ [Check the size of a lock column family when considering large CFs](https://github.com/tikv/tikv/pull/7676)
+ [Pre-split Regions during two-phase commit execution to avoid hotspots](https://github.com/pingcap/tidb/pull/16920)

### Engine

+ [Titan supports the compaction filter](https://github.com/tikv/titan/pull/164)

### Scheduling

+ [Add an engine filter to exclude special stores](https://github.com/pingcap/pd/pull/2426)

### Kubernetes

+ [Support noise reduction for auto-scaling](https://github.com/pingcap/tidb-operator/pull/2307)
+ [Support arbitrary topology-based HA in TiDB Scheduler](https://github.com/pingcap/tidb-operator/pull/2366)

## Notable issues

### Planner

+ [To improve the usability of SQL Plan Management](https://github.com/pingcap/tidb/issues/17466)
+ [To support the adaptive query execution](https://github.com/pingcap/tidb/issues/17471)

### Tools

+ [To simplify DM configuration](https://github.com/pingcap/dm/issues/691)
+ [To fix the issue that Dumpling cannot dump heavily skewed data in parallel](https://github.com/pingcap/dumpling/issues/75)
+ [Sync-diff-inspector needs a better checksum algorithm](https://github.com/pingcap/tidb-tools/issues/344)
+ [To pre-split a Region before the Region becomes a write hotspot to avoid the `server is busy` error in TiKV](https://github.com/pingcap/tidb/issues/16573)
+ [To make the writes of a large transaction more graceful](https://github.com/tikv/tikv/issues/7624)

### Engine

+ [To support auto-compaction in the Raw KV mode](https://github.com/tikv/tikv/issues/7870)

### Scheduling

+ [To separate the effect of `balance-region-limit` on `balance Region` and `merge Region`](https://github.com/pingcap/pd/issues/2432)

### Kubernetes

+ [To support incremental backup and restore with BR](https://github.com/pingcap/tidb-operator/issues/2409)

### Call for participation

Wanna participate with us? Take a look at the following help-wanted issues, which are mentoring available:

+ [To provide a more convenient way to modify the TiKV data directory](https://github.com/pingcap/tidb-operator/issues/1525)
+ [TiCDC should support more data formats in a message queue sink](https://github.com/pingcap/ticdc/issues/607)
+ [Support not merging some small Regions](https://github.com/pingcap/pd/issues/2171)
+ [Call For Participation: SIG DDL 2020/Q1 Plan](https://github.com/pingcap/tidb/issues/14800)

## New contributors

We’d like to welcome the following new contributors to TiDB and thank them for their work!

tidb:

+ [@crodjer](https://github.com/crodjer)

tikv:

+ [@longfangsong](https://github.com/longfangsong)

pd:

+ [@ccw1996](https://github.com/ccw1996)
+ [@TennyZhuang](https://github.com/TennyZhuang)

docs:

+ [@Hangzhi](https://github.com/Hangzhi)

docs-cn:

+ [@glkappe](https://github.com/glkappe)
+ [@ica10888](https://github.com/ica10888)
+ [@AdamKorcz](https://github.com/AdamKorcz)

tidb-operator:

+ [@PengJi](https://github.com/PengJi)
+ [@vincent178](https://github.com/vincent178)

parser:

+ [@PengJi](https://github.com/PengJi)

## This Monthly in TiKV

For more detailed and comprehensive information about TiKV, we have TiKV Monthly Update. The following covers May.

[This Month in TiKV - May 2020](https://tikv.org/blog/monthly-may-2020/)
