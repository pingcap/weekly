---
title: TiDB Monthly Update (November 2020)
date: 2020-12-01
summary: Here's what TiDB has achieved in November.
tags: ['TiDB', 'TiUP', 'TiDB Dashboard', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Monthly Update for November 2020

## Releases

We have one release this month:

[TiDB Operator 1.1.7 Release Notes](https://docs.pingcap.com/tidb-in-kubernetes/stable/release-1.1.7)

## Blog posts

We were thrilled to announce that we have raised $270 million in Series D funding. See [PingCAP, the Company Behind TiDB, Raises $270 Million in Series D Funding](https://pingcap.com/blog/pingcap-the-company-behind-tidb-raises-$270-million-in-series-d-funding) for details.

In [Choosing the Right Enterprise-Grade Disaster Recovery Solution for the Financial Industry](https://pingcap.com/blog/tidb-financial-level-backup-and-multi-center-disaster-recovery), Jun Yu walked us through how different types of databases handled high availability and disaster recovery. By understanding their limitations, we can see why TiDB, an open-source, distributed SQL database, is an excellent choice for the financial industry.

DM 2.0 has reached general availability, and it supports highly available migration tasks and shard merging and migration in optimistic mode. See [DM 2.0 GA: Secure, Easy, Highly Available Data Migration](https://pingcap.com/blog/dm-2.0-ga-secure-easy-highly-available-data-migration) for details.

Zhi Qi, the Real-time analytics R&D engineer at PingCAP, in his article [Flink + TiDB: A Scale-Out Real-Time Data Warehouse for Second-Level Analytics](https://pingcap.com/blog/flink-+-tidb-a-scale-out-real-time-data-warehouse-for-second-level-analytics), described what a real-time data warehouse was, the Flink + TiDB real-time data warehouse's architecture and advantages, this solution's real-world case studies, and a testing environment with Docker Compose.

[TiDB on KubeSphere: Run a Cloud-Native Distributed Database on a Hybrid-Cloud Kubernetes Platform](https://pingcap.com/blog/tidb-on-kubesphere), an article written by Will Zhang, an SRE engineer at iSoftStone, introduced how he ran TiDB on a hybrid-cloud Kubernetes platform.

Xinye Tao wrote an article [How to Run a Database on AWS with Better Performance and Lower Cost](https://pingcap.com/blog/run-database-on-aws-with-better-performance-and-lower-cost) that demonstrated how we at PingCAP deployed and optimized TiDB for production on AWS Cloud. It's our hope that recommendations provided here will also help you configure the TiDB service most suitable for your own workload.

In [How a Top Game Company Uses Chaos Engineering to Improve Testing](https://pingcap.com/blog/how-a-top-game-company-uses-chaos-engineering-to-improve-testing), Hui Zhang at Fuxi Lab, NetEase, discussed one of our most valuable testing tools, Chaos Mesh.

## Important pull requests

### Planner

+ [Support SQL bindings for `UPDATE`, `DELETE`, `INSERT`, and `REPLACE`](https://github.com/pingcap/tidb/pull/20686)

### DDL

+ [Support amending transactions with `ADD UNIQUE INDEX`](https://github.com/pingcap/tidb/pull/20693)

### Kubernetes

+ [Add the local volume support for backup or restore operations using BR](https://github.com/pingcap/tidb-operator/pull/3517)
+ [Migrate the deployment resource of TidbMonitor to StatefulSet](https://github.com/pingcap/tidb-operator/pull/3440)

### Migrate

+ [Support clustered index in TiCDC](https://github.com/pingcap/ticdc/pull/968)
+ [Use range properties to optimize the Region range estimate in TiDB Lightning](https://github.com/pingcap/tidb-lightning/pull/422)
+ [Add the `glue.Glue` interface in TiDB Lightning](https://github.com/pingcap/tidb-lightning/pull/456)

### TiUP

+ [Fix the issue of duplicated `pd_servers.name` in the topology before the cluster is truly deployed](https://github.com/pingcap/tiup/pull/922)

## Important issues

### DDL

+ [To fix the issue of index data inconsistency after randomly committing transactions with DDL statements](https://github.com/pingcap/tidb/issues/21289)

### Diagnosis

+ [TiDB Dashboard has been graduated from PingCAP-incubator](https://github.com/pingcap/community/issues/332)

### Kubernetes

+ [To fix the issue that `recoverFailover` might be forgotten to unset](https://github.com/pingcap/tidb-operator/issues/3335)
+ [To deprecate Pod validating and mutating webhook](https://github.com/pingcap/tidb-operator/issues/3497)

### Migrate

+ [To fix the issue that the backup checksum has a great impact on QPS and duration in BR](https://github.com/pingcap/br/issues/611)
+ [To fix the failure to handle tables with names that start with "sql" in TiDB Data Migration (DM)](https://github.com/pingcap/dm/issues/1255)

### TiUP

+ [To fix a command corner case that occurs when using a wrong `tar.gz` file](https://github.com/pingcap/tiup/issues/846)

## Call for participations

### DDL

+ [To fix the issue that altering placement rules misreports `ErrBuildRuleList`](https://github.com/pingcap/tidb/issues/20669)
+ [To refine the error message of the expression index](https://github.com/pingcap/tidb/issues/20318)

### Kubernetes

+ [To deprecate Pod validating and mutating webhook](https://github.com/pingcap/tidb-operator/issues/3497)

### Migrate

+ [To enhance the progress bar to align with non-integer `pk` in Dumpling](https://github.com/pingcap/dumpling/issues/204)

### TiUP

+ [To add a file lock for TiUP commands](https://github.com/pingcap/tiup/issues/809)

## New contributors

We'd like to welcome the following new contributors to TiDB and thank them for their work!

tidb:

+ [RogerYK](https://github.com/RogerYK)
+ [huang-b](https://github.com/huang-b)
+ [sev7ndayyoo](https://github.com/sev7ndayyoo)
+ [Aaaaaaron](https://github.com/Aaaaaaron)
+ [ou-bing](https://github.com/ou-bing)
+ [erwadba](https://github.com/erwadba)

tikv:

+ [Fedalto](https://github.com/Fedalto)
+ [pramodbiligiri](https://github.com/pramodbiligiri)
+ [Saigyouji-Yuyuko](https://github.com/Saigyouji-Yuyuko)
+ [LiuYuHui](https://github.com/LiuYuHui)
+ [gozssky](https://github.com/gozssky)
+ [bobrik](https://github.com/bobrik)
+ [Folyd](https://github.com/Folyd)
+ [yaozongyou](https://github.com/yaozongyou)
+ [hcbdfinity](https://github.com/hcbdfinity)
+ [davidor](https://github.com/davidor)
+ [dvermd](https://github.com/dvermd)

tiup:

+ [fln](https://github.com/fln)

tidb-operator:

+ [BinChenn](https://github.com/BinChenn)

blog-cn:

+ [Yolanda18-star](https://github.com/Yolanda18-star)

rust-prometheus:

+ [Fedalto](https://github.com/Fedalto)
+ [bobrik](https://github.com/bobrik)
+ [Folyd](https://github.com/Folyd)
+ [davidor](https://github.com/davidor)

sig-transaction:

+ [pramodbiligiri](https://github.com/pramodbiligiri)

parser:

+ [GoWebProd](https://github.com/GoWebProd)

dumpling:

+ [cxt90730](https://github.com/cxt90730)

grpc-rs:

+ [hcbdfinity](https://github.com/hcbdfinity)

ticdc:

+ [dengqee](https://github.com/dengqee)

website:

+ [yaozongyou](https://github.com/yaozongyou)

docs-cn:

+ [seekingua](https://github.com/seekingua)
+ [callmePicacho](https://github.com/callmePicacho)

docs:

+ [spencerkee](https://github.com/spencerkee)
+ [dveeden](https://github.com/dveeden)
