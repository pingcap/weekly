---
title: TiDB Monthly Update (July 2020)
date: 2020-08-03
summary: Here's what TiDB has achieved in July.
tags: ['TiDB', 'TiUP', 'TiDB Dashboard', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Monthly Update for July 2020

## Releases

We have four releases this month:

+ [TiDB 4.0.4 Release Notes](https://docs.pingcap.com/tidb/stable/release-4.0.4)

    + Bug fixes

+ [TiDB 4.0.3 Release Notes](https://docs.pingcap.com/tidb/stable/release-4.0.3)

    + New features

        - Display detailed version information for TiDB Dashboard [#679](https://github.com/pingcap-incubator/tidb-dashboard/pull/679)
        - Implement file encryption in the TiFlash proxy
        - Support configuring `kafka-client-id` in MQ sink-uri [#706](https://github.com/pingcap/ticdc/pull/706)
        - Support the specialized CSV separator and delimiter [#116](https://github.com/pingcap/dumpling/pull/116)

    + Bug fixes

+ [TiDB 4.0.2 Release Notes](https://docs.pingcap.com/tidb/stable/release-4.0.2)

    + New features

        - Support the `MEMORY_QUOTA()` hint in `INSERT` statements [#18101](https://github.com/pingcap/tidb/pull/18101)
        - Support authentication based on the `SAN` field of TLS certificate [#17698](https://github.com/pingcap/tidb/pull/17698)
        - Support the `encryption-meta` command in TiKV Control [#8103](https://github.com/tikv/tikv/pull/8103)
        - Enable TiFlash to run on the ARM architecture
        - Add a `cli` command to delete the TiCDC GC TTL [#652](https://github.com/pingcap/ticdc/pull/652)

    + Bug fixes

+ [TiDB 3.0.16 Release Notes](https://docs.pingcap.com/tidb/stable/release-3.0.16)

    + Improvements

        - Support the `is null` filter condition in hash partition pruning [#17308](https://github.com/pingcap/tidb/pull/17308)
        - Split separate Regions for the newly added partition [#17668](https://github.com/pingcap/tidb/pull/17668)
        - Avoid sending store heartbeats to PD after snapshots are received [#8145](https://github.com/tikv/tikv/pull/8145)
        - Improve the PD client log [#8091](https://github.com/tikv/tikv/pull/8091)

    + Bug fixes

## Blog posts

In [Announcing Chaos Mesh® as a CNCF Sandbox Project](https://pingcap.com/blog/announcing-chaos-mesh-as-a-cncf-sandbox-project/), we are thrill to announce that [Chaos Mesh®](https://chaos-mesh.org/) is now officially accepted as a CNCF Sandbox project.

We have published [Heterogeneous Database Replication to TiDB](https://pingcap.com/blog/heterogeneous-database-replication-to-tidb/) based on Tianshuang Qin's talk at [TiDB DevCon 2020](https://pingcap.com/community/devcon2020/). This article introduces TiDB's best practices of migrating heterogeneous databases between different database platforms and application scenarios.

[Horizontally Scaling the Hive Metastore Database by Migrating from MySQL to TiDB](https://pingcap.com/success-stories/horizontally-scaling-hive-metastore-database-by-migrating-from-mysql-to-tidb/), written by Mengyu Hu, the Platform Engineer at Zhihu, introduces how Zhihu uses TiDB to horizontally scale Hive Metastore to meet their growing business needs.

Shawn Ma's article [How TiDB's HTAP Makes Truly Hybrid Workloads Possible](https://pingcap.com/blog/how-tidb-htap-makes-truly-hybrid-workloads-possible/) looks at the design details of TiDB's HTAP architecture, including the real-time updatable columnar engine, the multi-Raft replication strategy, and smart selection.

Heng Long and Shuang Chen has written [Cluster Diagnostics: Troubleshoot Cluster Issues Using Only SQL Queries](https://pingcap.com/blog/cluster-diagnostics-troubleshoot-cluster-issues-using-only-sql-queries/) to elaborate on cluster diagnostics's diagnostic reports, and show you examples of how cluster diagnostics can help you quickly find system problems.

## Notable pull requests

### Planner

+ [Support `except` and `intersect` operators](https://github.com/pingcap/tidb/pull/18459)
+ [Re-implement hash partition pruning to support `in` and `or` and some other functions](https://github.com/pingcap/tidb/pull/18574)

### DDL

[Support the `ALTER PARTITION` clause](https://github.com/pingcap/tidb/pull/18611)

### TiDB Dashboard

[Keep consistent search behaviors for log search, statements, and slow queries](https://github.com/pingcap-incubator/tidb-dashboard/pull/682)

### Kubernetes

+ [Make `spec.pd`, `spec.tidb`, `spec.tikv`, and `spec.discovery` optional in the TidbCluster CR](https://github.com/pingcap/tidb-operator/pull/3009)
+ [Support `cleanPolicy` for the backup CR](https://github.com/pingcap/tidb-operator/pull/3002)

### Execution

+ [Record checksums for temporary chunks in disk](https://github.com/pingcap/tidb/pull/18649)
+ [Add the `Statscache` exchange](https://github.com/pingcap/tidb/pull/18788)

### Tools

+ [Speed up DDL execution for Backup & Restore (BR)](https://github.com/pingcap/br/pull/377)
+ Support Avro in TiCDC [#762](https://github.com/pingcap/ticdc/pull/762) [#687](https://github.com/pingcap/ticdc/pull/687) [#733](https://github.com/pingcap/ticdc/pull/733) [753](https://github.com/pingcap/ticdc/pull/753)
+ [Support the TLS in TiDB Data Migration (DM)](https://github.com/pingcap/dm/pull/569)

### Engine

[Fix the segment fault on creating the compaction filter when the base compaction filter is `NULL`](https://github.com/tikv/titan/pull/181)

### Scheduling

+ [Support checking Regions after the scheduling rule is updated](https://github.com/pingcap/pd/pull/2664)
+ [Fix the issue that when enabling placement rules, sometimes Region replicas cannot be scheduled to the optimal states](https://github.com/pingcap/pd/pull/2639)

### TiUP

[Support deploying and managing DM 2.0](https://github.com/pingcap/tiup/pull/587)

## Notable issues

### Planner

[To provide settings to prefer index scans over table scans](https://github.com/pingcap/tidb/issues/18808)

### Coprocessor

The `Chunk`-based computing for [data types of fixed sizes](https://github.com/tikv/tikv/pull/8214) and [data types of varying sizes](https://github.com/tikv/tikv/pull/8239)

### DDL

+ [To fix the issue of different behaviors on foreign keys with MySQL](https://github.com/pingcap/tidb/issues/18756)
+ [To show the host IP via API when the TiDB server runs without `--advertise-address`](https://github.com/pingcap/tidb/issues/18399)
+ [To allow row functions in the TiDB expression index](https://github.com/pingcap/tidb/issues/18150)
+ [To fix the compatibility issue of `SELECT ... FOR SHARE` statements](https://github.com/pingcap/parser/issues/945)

### TiDB Dashboard

### Kubernetes

[To improve the robustness and stability of TiDB Operator](https://github.com/pingcap/tidb-operator/issues/2821)

### Execution

[To dump memory status of all SQL statements when the server is consuming a lot of memory](https://github.com/pingcap/tidb/issues/17095)

### Tools

[To support point-in-time recovery (PITR) in TiCDC and BR](https://github.com/pingcap/br/issues/325)

### Scheduling

[To support the atomic helper API for placement rules](https://github.com/pingcap/pd/issues/2680)

### TiUP

[To fix the issue that Prometheus configuration files cannot be edited using TiUP](https://github.com/pingcap/tiup/issues/604)

## Call for participation

### Tools

+ [To properly handle `infinity` in TiCDC](https://github.com/pingcap/ticdc/issues/781)
+ [The exit code should not be `0` if the command is failed to run in DM](https://github.com/pingcap/dm/issues/841)

### TiUP

[TiUP issues to be resolved](https://github.com/pingcap/tiup/issues?q=is%3Aopen+is%3Aissue+label%3Astatus%2Fhelp-wanted)

### Scheduling

[To use one tool with sub-commands instead of many tools](https://github.com/pingcap/pd/issues/2527)

## New contributors

We’d like to welcome the following new contributors to TiDB and thank them for their work!

tidb:

+ [BurtonQin](https://github.com/BurtonQin)
+ [thomasten](https://github.com/thomasten)
+ [tina77fritz](https://github.com/tina77fritz)
+ [sundb](https://github.com/sundb)
+ [xiaodong-ji](https://github.com/xiaodong-ji)

tikv:

+ [ekexium](https://github.com/ekexium)
+ [abbccdda](https://github.com/abbccdda)
+ [Phosphorus15](https://github.com/Phosphorus15)
+ [xxchan](https://github.com/xxchan)
+ [SASUKE40](https://github.com/SASUKE40)
+ [skyzh](https://github.com/skyzh)
+ [weihanglo](https://github.com/weihanglo)

parser:

+ [wangggong](https://github.com/wangggong)
+ [ldeng-ustc](https://github.com/ldeng-ustc)

pd:

+ [howardlau1999](https://github.com/howardlau1999)
+ [ZenoTan](https://github.com/ZenoTan)

tidb-operator:

+ [8398a7](https://github.com/8398a7)

docs:

+ [miaoqingli](https://github.com/miaoqingli)

docs-cn:

+ [WuShaoQiang](https://github.com/WuShaoQiang)
+ [Rubik-W](https://github.com/Rubik-W)

rust-prometheus:

+ [iffyio](https://github.com/iffyio)

## This Month in TiKV

For more detailed and comprehensive information about TiKV, we have TiKV Monthly Update. The following covers July.

[This Month in TiKV - July 2020](https://tikv.org/blog/monthly-july-2020/)
