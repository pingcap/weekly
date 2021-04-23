---
title: TiDB Monthly Update (August 2020)
date: 2020-09-01
summary: Here's what TiDB has achieved in August.
tags: ['TiDB', 'TiUP', 'TiDB Dashboard', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Monthly Update for August 2020

## Releases

We have five releases this month:

+ [TiDB 4.0.5 Release Notes](https://docs.pingcap.com/tidb/stable/release-4.0.5)

    + New features

        + Define error code for errors in TiKV [#8387](https://github.com/tikv/tikv/pull/8387)
        + Support the unified log format with TiDB in TiFlash
        + Support Kafka SSL connection in TiCDC [#764](https://github.com/pingcap/ticdc/pull/764)
        + Support outputting the old value in TiCDC [#708](https://github.com/pingcap/ticdc/pull/708)

    + Improvements

        + Optimize the performance of `DecodePlan` for big union queries [#18941](https://github.com/pingcap/tidb/pull/18941)
        + Reduce the number of GC lock scans when the Region cache miss error occurs [#18876](https://github.com/pingcap/tidb/pull/18876)
        + Support canceling operations before the RPC response is returned [#18580](https://github.com/pingcap/tidb/pull/18580)

    + Bug fixes

+ [TiDB 3.0.18 Release Notes](https://docs.pingcap.com/tidb/stable/release-3.0.18)

    + Improvements

        + Support the time duration format of Go for the Pump GC configuration in TiDB Binlog [#996](https://github.com/pingcap/tidb-binlog/pull/996)

    + Bug fixes

+ [TiDB 3.0.17 Release Notes](https://docs.pingcap.com/tidb/stable/release-3.0.17)

    + Improvements

        + Decrease the default value of the `query-feedback-limit` configuration item from `1024` to `512`, and improve the statistics feedback mechanism to ease its impact on the cluster [#18770](https://github.com/pingcap/tidb/pull/18770)
        + Limit the batch split count for one request [#18694](https://github.com/pingcap/tidb/pull/18694)
        + Add the `hibernate-timeout` configuration that delays Region hibernation to improve rolling update performance [#8207](https://github.com/tikv/tikv/pull/8207)
        + `[black-white-list]` has been deprecated with a newer, easier-to-understand filter format [#332](https://github.com/pingcap/tidb-lightning/pull/332)

    + Bug fixes

+ [TiDB Data Migration (DM) 2.0 RC Release Notes](https://docs.pingcap.com/tidb-data-migration/v2.0/2.0.0-rc)

    + New features

        + Support high availability for data migration tasks [#473](https://github.com/pingcap/dm/pull/473)
        + Add an optimistic mode for sharding DDL statements [#568](https://github.com/pingcap/dm/pull/568)
        + Add the `handle-error` command to handle errors during DDL incremental replication [#850](https://github.com/pingcap/dm/pull/850)
        + Add a `workaround` field in the error returned by `query-status` to suggest the error handling method [#753](https://github.com/pingcap/dm/pull/753)

    + Improvements

        + Improve the monitoring dashboards and alert rules [#853](https://github.com/pingcap/dm/pull/853)
        + Replace Mydumper with Dumpling as the full export unit [#540](https://github.com/pingcap/dm/pull/540)

    + Bug fixes

+ [TiDB Operator 1.1.14 Release Notes](https://github.com/pingcap/tidb-operator/blob/master/CHANGELOG-1.1.md#tidb-operator-v114-release-notes)

## Blog posts

We published a post based on the keynote speech that Max Liu, CEO at PingCAP, gave at [TiDB DevCon 2020](https://pingcap.com/community/devcon2020/), the TiDB community's annual technical conference.

In [PingCAP Successfully Completes SOC 2 Type 1 Examination for TiDB Cloud](https://pingcap.com/blog/pingcap-successfully-completes-soc-2-type-1-examination-for-tidb-cloud/), we announced that we have successfully completed a Type 1 System and Organization Controls (SOC) 2 examination for our flagship managed service, TiDB Cloud.

In [Announcing PD Transfer to TiKV Project](https://pingcap.com/blog/announcing-pd-transfer-to-tikv-project/), we announced that we decided to move the PD library entirely to TiKV org, happening at 11 AM, UTC+8, August 17, 2020.

[Create a Scale-Out Hive Cluster with a Distributed, MySQL-Compatible Database](https://pingcap.com/blog/create-scale-out-hive-cluster-with-distributed-mysql-compatible-database/), written by Mengyu Hu, the platform engineer at Zhihu, shared with you how to create a Hive cluster with TiDB as the Metastore database at the backend so that you can use TiDB to horizontally scale Hive Metastore without worrying about database capacity.

In [Why We Chose a Distributed SQL Database to Complement MySQL](https://pingcap.com/case-studies/why-we-chose-a-distributed-sql-database-to-complement-mysql), Chao Xu, the Senior DBA Engineer at VIPKid, discussed how they used TiDB to do multi-dimensional queries on sharded data and enhance their real-time analytics capability.

Ben Ye and Chengwen Yin wrote an article [Building an Automated Testing Framework Based on Chaos Mesh® and Argo](https://pingcap.com/blog/building-automated-testing-framework-based-on-chaos-mesh-and-argo/) that described how they used TiPocket, an automated testing framework to build a full Chaos Engineering testing loop for TiDB.

This June, we announced the beta release of TiDB Cloud, the fully managed database service provided by PingCAP. In the article [TiDB Cloud: Managed SQL at Scale on AWS and GCP](https://pingcap.com/blog/tidb-cloud-managed-sql-at-scale-on-aws-and-gcp/), Ken Liu walked you through what TiDB Cloud offers.

[What's New and Improved in TiDB Docs](https://pingcap.com/blog/what-is-new-and-improved-in-tidb-docs/), written by Lilian Lee, covered recent big changes, new content, and improvements in TiDB documentation.

We published a post [PingCAPers Make Their Debut at VLDB](https://pingcap.com/blog/pingcapers-make-their-debut-at-vldb/) that announced PingCAP's upcoming sharing schedule in the 46th International Conference on Very Large Databases (VLDB) that is broadcasted online from August 31st to September 4th.

## Important pull requests

### Raft

+ [Conduct port data-driven tests from CockroachDB](https://github.com/tikv/raft-rs/pull/388)
+ [Add the global entry cache to the Raft engine](https://github.com/tikv/raft-engine/pull/21)

### Planner

+ [Enable the clustered index feature by default](https://github.com/pingcap/tidb/pull/19582)
+ [Expand DNF if it can generate a compound index](https://github.com/pingcap/tidb/pull/18879)

### DDL

+ [Support dropping partitions on the partitioned table with global indexes](https://github.com/pingcap/tidb/pull/19222)
+ [Alter rules when truncating partitions](https://github.com/pingcap/tidb/pull/19505)
+ [Support the `DROP PLACEMENT` clause](https://github.com/pingcap/tidb/pull/19174)
+ [Support the `ALTER PLACEMENT` clause](https://github.com/pingcap/tidb/pull/19065)

### Transaction

+ [Return the lock information in `CheckTxnStatus`](https://github.com/tikv/tikv/pull/8529)
+ [Refactor the `Mode` structure of transaction commands](https://github.com/tikv/tikv/pull/8296)

### TiDB Dashboard

+ [Support the online Query Editor](https://github.com/pingcap-incubator/tidb-dashboard/pull/713)
+ [Visualize store locations](https://github.com/pingcap-incubator/tidb-dashboard/pull/719)

### Kubernetes

+ [Fix the Goroutine leak that occurs when TLS is enabled](https://github.com/pingcap/tidb-operator/pull/3081)
+ [Support TLS for backup and restore operations with Dumpling and TiDB Lightning](https://github.com/pingcap/tidb-operator/pull/3100)

### Execution

+ [Support the `stddev_pop` aggregation function](https://github.com/pingcap/tidb/pull/19195)
+ [Record the detailed RPC runtime information in `CopTask` runtime statistics](https://github.com/pingcap/tidb/pull/18916)

### Tools

+ [Support writing data to S3 directly in TiCDC](https://github.com/pingcap/ticdc/pull/826)
+ [Import and upgrade from a v1.0.x DM cluster to a v2.0 DM cluster](https://github.com/pingcap/dm/pull/861)
+ [Support the file-level routing](https://github.com/pingcap/tidb-lightning/pull/366)

### Engine

+ [Add the RocksDB-Cloud binding](https://github.com/tikv/rust-rocksdb/pull/517)

### Scheduling

+ [Forbid multiple leader replicas and require at least one leader](https://github.com/tikv/pd/pull/2761)
+ [Support the `RuleGroup` configuration in placement rules](https://github.com/tikv/pd/pull/2740)
+ [Support the batch deletion and insertion](https://github.com/tikv/pd/pull/2699)

### TiUP

+ [Support the TLS encryption for the TiDB cluster](https://github.com/pingcap/tiup/pull/673)
+ [Support using the local file or directory in the configuration for monitoring components](https://github.com/pingcap/tiup/pull/712)

## Important issues

### DDL

+ [To support transitions between the same types, including unsigned transitions](https://github.com/pingcap/tidb/issues/19116)
+ [To support dropping columns with composite indices](https://github.com/pingcap/tidb/issues/19196)
+ [To execute the non-dependent DDL job as soon as possible](https://github.com/pingcap/tidb/issues/19476)
+ [To design and implement a scheduling algorithm for DDL jobs](https://github.com/pingcap/tidb/issues/19397)
+ [To add indexes in parallel](https://github.com/pingcap/tidb/issues/19386)

### Transaction

+ [To fix the issue that `acquire_pessimistic_lock` has a very poor performance when there are many `Write::Lock`s](https://github.com/tikv/tikv/issues/7024)

### Kubernetes

+ [Fix the issue that failed stores cannot be removed for TiKV or TiFlash](https://github.com/pingcap/tidb-operator/issues/3177)
+ [Fix the TiDB OOM issue that occurs when TLS is enabled](https://github.com/pingcap/tidb-operator/issues/3079)

### Execution

### Tools

+ [To fix `SEGFAULT` when backing up data](https://github.com/pingcap/br/issues/450)
+ [To do: the global `ResolvedTs` should be reset to `CheckpointTs` when a `capture` fails in TiCDC](https://github.com/pingcap/ticdc/issues/860)
+ [The `--no-locks` argument does not work in TiDB Data Migration v2.0.0-rc](https://github.com/pingcap/dm/issues/956)

### Scheduling

+ [To fix the issue that many heartbeat update operations might cause the `GetRegion` timeout](https://github.com/tikv/pd/issues/2843)
+ [To add the roadmap of the cross-DC deployment of the local/global transaction](https://github.com/tikv/pd/issues/2759)

### TiUP

+ [To support deploying and managing TiDB Data Migration v2.0](https://github.com/pingcap/tiup/issues/557)

## Call for participations

### Kubernetes

+ [To support the canary upgrade of TiDB Operator](https://github.com/pingcap/tidb-operator/issues/3166)

### Tools

+ [To support RocketMQ as the MQ sink in TiCDC](https://github.com/pingcap/ticdc/issues/823)
+ [To do: the temporal directory should not be used in a task to save the dumped files in DM](https://github.com/pingcap/dm/issues/893)
+ [To support IPv6 for `binlogctl` in TiDB Binlog](https://github.com/pingcap/tidb-binlog/issues/995)

### Scheduling

+ [To add more metrics of heartbeat](https://github.com/tikv/pd/issues/2800)

### TiUP

+ [To do: the PD leader should be reloaded at last](https://github.com/pingcap/tiup/issues/597)

## New contributors

We’d like to welcome the following new contributors to TiDB and thank them for their work!

tidb:

* [liangyuanpeng](https://github.com/liangyuanpeng)
* [motecshine](https://github.com/motecshine)
* [bestgopher](https://github.com/bestgopher)
* [jyz0309](https://github.com/jyz0309)
* [sweelim20](https://github.com/sweelim20)
* [gentcys](https://github.com/gentcys)

tikv:

* [tehbrut](https://github.com/tehbrut)
* [maoueh](https://github.com/maoueh)

docs-cn:

* [xxj123go](https://github.com/xxj123go)
* [EspenDai](https://github.com/EspenDai)
* [2014BDuck](https://github.com/2014BDuck)
* [yufan022](https://github.com/yufan022)
* [kemingy](https://github.com/kemingy)
* [XiaoJenny](https://github.com/XiaoJenny)
* [David7653](https://github.com/David7653)

log:

* [kzh125](https://github.com/kzh125)

parser:

* [keatonconrad](https://github.com/keatonconrad)

pd:

* [1150310621](https://github.com/1150310621)
* [jiashiwen](https://github.com/jiashiwen)

pprof-rs:

* [umanwizard](https://github.com/umanwizard)

qa:

* [seiya-annie](https://github.com/seiya-annie)

tics:

* [zingdle](https://github.com/zingdle)

tidb-dashboard:

* [ahaha420](https://github.com/ahaha420)

tidb-operator:

* [cvvz](https://github.com/cvvz)
* [sstubbs](https://github.com/sstubbs)
* [serbaut](https://github.com/serbaut)

tinykv:

* [BinacsLee](https://github.com/BinacsLee)
* [imaffe](https://github.com/imaffe)

tiup:

* [wing0wind](https://github.com/wing0wind)
* [darkelf21cn](https://github.com/darkelf21cn)

website:

* [Cindy-Li1997](https://github.com/Cindy-Li1997)

## This Month in TiKV

For more detailed and comprehensive information about TiKV, we have TiKV Monthly Update. The following covers June.

[This Month in TiKV - August 2020](https://tikv.org/blog/monthly-august-2020/)
