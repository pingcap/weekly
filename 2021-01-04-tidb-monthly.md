---
title: TiDB Monthly Update (December 2020)
date: 2021-01-04
summary: Here's what TiDB has achieved in December.
tags: ['TiDB', 'TiUP', 'TiDB Dashboard', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Monthly Update for December 2020

## Releases

We have five releases in this month:

+ [TiDB 4.0.9 Release Notes](https://docs.pingcap.com/tidb/stable/release-4.0.9)

    + New features
        + TiFlash supports storing the latest data of the storage engine on multiple disks (experimental)
        + TiDB Dashboard supports displaying and sorting by all fields in the SQL Statements page
        + TiDB Dashboard supports customizing the Prometheus address

    + Improvements
        - Avoid the (index) merge join in a heuristic way when converting equal conditions to other conditions in TiDB
        - Differentiate the types of user variables in TiDB
        - Support setting the `GOGC` variable in the configuration file in TiDB
        - Add the tag to trace the source of the `split` command in TiKV

    + Bug fixes

+ [TiDB 3.0.20 Release Notes](https://docs.pingcap.com/tidb/stable/release-3.0.20)

    + Compatibility changes
        - Deprecate the `enable-streaming` configuration item in TiDB

    + Improvements
        - Raise an error when preparing the `LOAD DATA` statement
        - Add the `end_point_slow_log_threshold` configuration item

    + Bug fixes

+ [TiDB Data Migration 2.0.1 Release Notes](https://docs.pingcap.com/tidb-data-migration/stable/2.0.1)

    + Improvements
        - Support the relay log feature in high availability scenarios
        - Restrict the `handle-error` command to only handle DDL errors to avoid misuse
        - Support simultaneously connecting multiple DM-master nodes and automatically switching connected nodes in dmctl

    + Bug fixes

+ [TiDB Operator 1.1.8 Release Notes](https://docs.pingcap.com/tidb-in-kubernetes/stable/release-1.1.8)

    + New features
        - Support arbitrary Volume and VolumeMount for `PD`, `TiDB`, `TiKV`, `TiFlash`, `Backup` and `Restore`, which enables using NFS or any other kubernetes-supported volume source for backup/restore workflow

    + Improvements
        - Support cluster and client TLS for `tidb-lightning` and `tikv-importer` helm charts
        - Support setting additional ports for the TiDB service

    + Bug fixes

+ [TiDB Operator 1.1.9 Release Notes](https://docs.pingcap.com/tidb-in-kubernetes/stable/release-1.1.9)

    + Improvement
        - Support `spec.toolImage` for `Backup` & `Restore` to define the image used to provide the Dumpling/TiDB Lightning binary executables

    + Bug fixes

## Blog posts

In [PingCAP's Top 10 Posts of 2020](https://pingcap.com/blog/pingcap-top-10-posts-of-2020), we took a look back at our 10 most popular posts in 2020.

We also published [PingCAP 2020 Year in Review](https://pingcap.com/blog/pingcap-2020-year-in-review) to look back at some of our important milestones and achievements that we accomplished, while we looked forward to a greater year ahead.

Will Zhang, a TiDB community member, wrote an article [TiDB on KubeSphere: Release a Cloud-Native Distributed Database to the KubeSphere App Store](https://pingcap.com/blog/release-a-cloud-native-distributed-database-on-kubesphere-app-store) that walked you through how to deploy TiDB on KubeSphere by app templates and release TiDB to the App Store.

In [Batch Processing Massive Data Much Quicker with TiSpark](https://pingcap.com/blog/batch-processing-massive-data-much-quicker-with-tispark), our senior solution architect Zhexuan Yang explained why TiSpark is better than the traditional batch processing solution, how you can benefit from TiSpark, and how it works.

In this monthly, our engineer Wenbo Zhang has written four articles:

+ [Why We Switched from BCC to libbpf for Linux BPF Performance Analysis](https://pingcap.com/blog/why-we-switched-from-bcc-to-libbpf-for-linux-bpf-performance-analysis) described why libbpf-tools, a collection of applications based on the libbpf + BPF CO-RE mode, is a better solution than bcc-tools and how we're using libbpf-tools at PingCAP.
+ [Why We Disable Linux's THP Feature for Databases](https://pingcap.com/blog/why-we-disable-linux-thp-feature-for-databases) described how THP causes performance to fluctuate, the typical symptoms, and our recommended solutions.
+ In [Tips and Tricks for Writing Linux BPF Applications with libbpf](https://pingcap.com/blog/tips-and-tricks-for-writing-linux-bpf-applications-with-libbpf), Zhang shared his experience about writing Berkeley Packet Filter (BPF) applications with libbpf. He hopes that this article is helpful to people who are interested in libbpf and inspires them to further develop and improve BPF applications with libbpf.
+ [How to Trace Linux System Calls in Production with Minimal Impact on Performance](https://pingcap.com/blog/how-to-trace-linux-system-calls-in-production-with-minimal-impact-on-performance) introduced perf and traceloop, two commonly used command-line tools, to help you trace system calls in a production environment.

## Important pull requests

### Planner

+ [Fix the behavior of correlated aggregation](https://github.com/pingcap/tidb/pull/21431)
+ [Support the baseline capture for prepared statements](https://github.com/pingcap/tidb/pull/21271)
+ [Improve the statistics for non-index columns](https://github.com/pingcap/tidb/pull/21817)

### SQL-Infra

+ [Fix the incorrect behavior of `NO_ZERO_DATE` when altering tables](https://github.com/pingcap/tidb/pull/21564)
+ [Refine the JSON conversion, throw errors when the object/array is converted to the integer/float/decimal](https://github.com/pingcap/tidb/pull/21826)

### Diagnosis

+ [TiDB Dashboard provides a cluster statistics page](https://github.com/pingcap/tidb-dashboard/pull/815)
+ [TiDB Dashboard supports customizing the Prometheus address](https://github.com/pingcap/tidb-dashboard/pull/815)
+ [TiDB Dashboard supports exporting Statement and Slow Query list](https://github.com/pingcap/tidb-dashboard/pull/778)
+ [Improve slow log system table performance](https://github.com/pingcap/tidb/pull/20750)

### Execution

+ [Support the shuffled `HashJoin`](https://github.com/pingcap/tidb/pull/20894)
+ [Support the new syntax `ALTER TABLE ADD` and `DROP TIDB_STATS`](https://github.com/pingcap/tidb/pull/22127)

### Kubernetes

+ [Fix the issue that `commitTS` in status is missed even if the backup job succeeds](https://github.com/pingcap/tidb-operator/pull/3648)
+ [Update status for `TidbInitializer`](https://github.com/pingcap/tidb-operator/pull/3573)

### Migrate

+ [Make the relay log highly available in TiDB Data Migration](https://github.com/pingcap/dm/pull/1291)
+ [Stabilize the Unified Sorter in TiCDC](https://github.com/pingcap/ticdc/pull/1210)
+ [Sort the index rather than insert it into the skiplist](https://github.com/pingcap/tidb-lightning/pull/520)

### TiUP

+ [Work around the issue that store IDs are not monotonically assigned](https://github.com/pingcap/tiup/pull/1011)

## Important issues

### Planner

+ [To fix the issue that the decorrelation is not supported in some scenarios](https://github.com/pingcap/tidb/issues/21518)

### SQL-Infra

+ [To fix the issue that generated columns can be wrongly moved before its referred columns](https://github.com/pingcap/tidb/issues/21445)

### Kubernetes

+ [To fix the issue that `recoverFailover` might be forgotten to unset](https://github.com/pingcap/tidb-operator/issues/3335)
+ [To deprecate the Pod validating and mutating webhook](https://github.com/pingcap/tidb-operator/issues/3497)

### Migrate

+ [To fix the failure to increment restore when it is already restored in the past in Backup & Restore](https://github.com/pingcap/br/issues/663)
+ [To fix the issue that TiKV storage and CPU usages are not balanced during the process of import in TiDB Lightning](https://github.com/pingcap/tidb-lightning/issues/500)

### TiUP

+ [To support the offline or parallel upgrade](https://github.com/pingcap/tiup/issues/1027)

## Call for participations

### SQL-Infra

+ [To support the session scope variable `tidb_scatter_region`](https://github.com/pingcap/tidb/issues/21991)

### Diagnosis

+ Call for review: [timeline tracing](https://github.com/pingcap/tidb/pull/19557) and join [#wg-tracing](https://tidbcommunity.slack.com/archives/C016BSGC732) if you are interested.

### Kubernetes

+ [To deprecate the Pod validating and mutating webhook](https://github.com/pingcap/tidb-operator/issues/3497)
+ [To fix an issue of `MaxBackups` behavior on `BackupSchedule`](https://github.com/pingcap/tidb-operator/issues/3660)

### TiUP

+ [To support `-N node` in addition to `-N node:port`](https://github.com/pingcap/tiup/issues/1014)

## New contributors

We'd like to welcome the following new contributors to TiDB and thank them for their work!

tidb:

+ [0xflotus](https://github.com/0xflotus)
+ [zhaoxugang](https://github.com/zhaoxugang)
+ [luxinle](https://github.com/luxinle)
+ [StoneDotYang](https://github.com/StoneDotYang)
+ [Andrewmatilde](https://github.com/Andrewmatilde)
+ [jackwener](https://github.com/jackwener)
+ [xuyifangreeneyes](https://github.com/xuyifangreeneyes)
+ [xuhui-lu](https://github.com/xuhui-lu)

tikv:

+ [eliasyaoyc](https://github.com/eliasyaoyc)

pd:

+ [PhotonQuantum](https://github.com/PhotonQuantum)

tidb-operator:

+ [swartz-k](https://github.com/swartz-k)

docs-tidb-operator:

+ [Rick-lee01](https://github.com/Rick-lee01)
+ [grandsail](https://github.com/grandsail)

docs:

+ [killua525](https://github.com/killua525)

docs-cn:

+ [ZhenhanGong](https://github.com/ZhenhanGong)

tinykv:

+ [zhuo1angT](https://github.com/zhuo1angT)

grpc-rs:

+ [heftig](https://github.com/heftig)
+ [hug-dev](https://github.com/hug-dev)
+ [ramosbugs](https://github.com/ramosbugs)

rust-prometheus:

+ [nickelc](https://github.com/nickelc)

rust-rocksdb:

+ [peilun-conflux](https://github.com/peilun-conflux)

client-rust:

+ [humancalico](https://github.com/humancalico)
