---
title: TiDB Monthly Update (September 2020)
date: 2020-10-01
summary: Here's what TiDB has achieved in September.
tags: ['TiDB', 'TiUP', 'TiDB Dashboard', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Monthly Update for September 2020

## Releases

We have five releases this month:

+ [TiDB 4.0.7 Release Notes](https://docs.pingcap.com/tidb/stable/release-4.0.7)

    + New features

        - Add the `GetAllMembers` function in the PD client to get PD member information
        - Support generating the metrics relationship graph

    + Improvements

        - Add more runtime information for the `join` operator
        - Support the JSON log format
        - Improve the error handling of the Region meta change that occurs during reads

    + Bug Fixes

+ [TiDB 4.0.6 Release Notes](https://docs.pingcap.com/tidb/stable/release-4.0.6)

    + New features

        - Support outer join in TiFlash broadcast join
        - Add Query Editor and execution UI in TiDB Dashboard (experimental) [#713](https://github.com/pingcap-incubator/tidb-dashboard/pull/713)
        - Support outputting data in the `maxwell` format [#869](https://github.com/pingcap/ticdc/pull/869)
        - TiCDC has become an feature for general availability (GA).

    + Improvements

        - Replace error codes and messages with standard errors [#19888](https://github.com/pingcap/tidb/pull/19888)
        - Reduce QPS drop when `DropTable` or `TruncateTable` is being executed [#8627](https://github.com/tikv/tikv/pull/8627)
        - Update TiDB Dashboard to v2020.09.08.1 [#2928](https://github.com/pingcap/pd/pull/2928)

    + Bug fixes

+ [TiDB 3.0.19 Release Notes](https://docs.pingcap.com/tidb/stable/release-3.0.19)

    + Compatibility changes

        - Change the import path from `pingcap/pd` to `tikv/pd`
        - Change the copyright information from `PingCAP, Inc` to `TiKV Project Authors`

    + Improvements

        - Mitigate the impact of failure recovery on QPS performance
        - Support adjusting the concurrency of the `union` operator
        - Add an alert rule for PD restart

    + Bug fixes

+ [TiDB Data Migration 2.0 RC.2 Release Notes](https://docs.pingcap.com/tidb-data-migration/v2.0/2.0.0-rc.2)

+ [TiDB Operator 1.1.5 Release Notes](https://docs.pingcap.com/tidb-in-kubernetes/stable/release-1.1.5)

## Blog posts

We published [Celebrate TiKV Graduation within CNCF](https://pingcap.com/blog/celebrate-tikv-graduation-within-cncf/) to celebrate TiKV's graduation from the CNCF.

Aylei Wu wrote an article [TiDB Operator: Your TiDB Operations Expert in Kubernetes](https://pingcap.com/blog/tidb-operator-your-tidb-operations-expert-in-kubernetes/) to answer the question of whether or not to run TiDB in Kubernetes and introduce to you TiDB Operator, your database operations expert for Kubernetes.

In [How to Migrate Data from Amazon Aurora MySQL to TiDB Cloud](https://pingcap.com/blog/how-to-migrate-data-from-amazon-aurora-mysql-to-tidb-cloud/), Yiwen Chen showed you how to migrate your data from Amazon Aurora MySQL to TiDB Cloud using the open-source Dumpling and TiDB Lightning tools.

Jiaqing Xu, the DBA at BIGO, wrote an article [Why We Chose an HTAP Database over MySQL for Horizontal Scaling and Complex Queries](https://pingcap.com/case-studies/why-we-chose-an-htap-database-over-mysql-for-horizontal-scaling-and-complex-queries) to talk about how BIGO has benefited from TiDB and its new features in TiDB 4.0.

In [Chaos Mesh 1.0: Chaos Engineering on Kubernetes Made Easier](https://pingcap.com/blog/Chaos-Mesh-1.0-Chaos-Engineering-on-Kubernetes-Made-Easier/), Chaos Mesh Maintainers were proud to announce the general availability of Chaos Mesh® 1.0, following its entry into CNCF as a sandbox project in July, 2020.

[chaos-mesh-action: Integrate Chaos Engineering into Your CI](https://pingcap.com/blog/chaos-mesh-action-integrate-chaos-engineering-into-your-ci/), written by Xiang Wang, introduced how we use chaos-mesh-action, a GitHub action to integrate Chaos Mesh into the CI process.

[How We Build an HTAP Database That Simplifies Your Data Platform](https://pingcap.com/blog/how-we-build-an-htap-database-that-simplifies-your-data-platform/), an article based on Shawn Ma's talk given at TiDB DevCon 2020, shared with you what HTAP is and how TiDB makes the most of the HTAP architecture.

In [Announcing HTAP support in TiDB Cloud](https://pingcap.com/blog/announcing-htap-support-in-tidb-cloud/#announcing-htap-support-in-tidb-cloud), we were glad to announce that TiDB Cloud, our fully managed database service powered by TiDB, now supports Hybrid Transactional/Analytical Processing (HTAP) workloads.

[ZaloPay: Using a Scale-Out MySQL Alternative to Serve Millions of Users](https://pingcap.com/case-studies/zalopay-using-a-scale-out-mysql-alternative-to-serve-millions-of-users), an article based on Tan To Nguyen Duy (the DevOps Engineer at VNG Corporation)'s sharing at TiDB DevCon 2020, explained why his team chose TiDB as ZaloPay's merchant platform core database.

Haodong Ji, the head DBA at Zhuan Zhuan, wrote an article [A Scale-Out Database Powers China's Letgo with Reduced Maintenance Costs](https://en.pingcap.com/case-studies/scale-out-database-powers-china-letgo-with-reduced-maintenance-costs) to introduce how TiDB 4.0's new features make TiDB easier to use and reduce their operations and maintenance costs.

## Important pull requests

### Raft

[Support using the joint consensus in Raftstore](https://github.com/tikv/tikv/pull/8401/)

### Transaction

[Allow async commit by default](https://github.com/tikv/tikv/pull/8630)

### DDL

+ [Add a framework for placement rules cache](https://github.com/pingcap/tidb/pull/20086)
+ [Support changing column types between string types](https://github.com/pingcap/tidb/pull/20032)
+ [Improve the processing speed of general DDL jobs](https://github.com/pingcap/tidb/pull/19997)
+ [Support renaming multiple tables](https://github.com/pingcap/tidb/pull/19962)

### Kubernetes

+ [Support passing raw toml configuration for TiDB as a string](https://github.com/pingcap/tidb-operator/pull/3327)
+ [Support recovering from failover for TiFlash and TiKV](https://github.com/pingcap/tidb-operator/pull/3189)

### Migrate

+ [BR: Support restoring data from the TiCDC log](https://github.com/pingcap/br/pull/482)
+ [TiCDC: Support zendesk/maxwell data format](https://github.com/pingcap/ticdc/pull/869)
+ [Dumpling: Support writing data directly to S3](https://github.com/pingcap/dumpling/pull/155)
+ [TiDB Lightning: Support restoring data from S3](https://github.com/pingcap/tidb-lightning/pull/361)

### Engine

+ [RocksDB: Add checks for compaction order and data block cache](https://github.com/tikv/rocksdb/pull/195)
+ [RocksDB: Improve the auto-tuned rate limiter](https://github.com/tikv/rocksdb/pull/193)
+ [Titan: Add dictionary compression support for the blob file](https://github.com/tikv/titan/pull/189)

### Scheduling

+ [Add the basic TSO generation logic to the local allocator](https://github.com/tikv/pd/pull/2986)
+ [Add the basic election logic to the local allocator](https://github.com/tikv/pd/pull/2894)
+ [Implement the joint consensus builder](https://github.com/tikv/pd/pull/2740)
+ [Add some operator steps related to the joint consensus](https://github.com/tikv/pd/pull/2895)
+ [Support scattering Regions by group](https://github.com/tikv/pd/pull/2905)
+ [Make use of the new bundle API](https://github.com/tikv/pd/pull/2927)

### TiUP

+ [Download component in the streaming mode to avoid memory explosion](https://github.com/pingcap/tiup/pull/755)
+ [Automatically check whether TiKV's label is set](https://github.com/pingcap/tiup/pull/800)

## Important issues

### DDL

+ [To support the `wait`/`nowait` syntax on DDL operations](https://github.com/pingcap/tidb/issues/19928)
+ [To support displaying the process of some DDL operations](https://github.com/pingcap/tidb/issues/19923)

### Kubernetes

+ [To fix the issue that some configuration parameters are missing in the TidbCluster CR](https://github.com/pingcap/tidb-operator/issues/3212)
+ [To refactor the Tidbmonitor design](https://github.com/pingcap/tidb-operator/issues/3292)

### Migrate

+ [BR: To fix the issue that TiKV's S3 does not support Virtual Host Style requests](https://github.com/pingcap/br/issues/484)
+ [TiCDC: To support clustered index](https://github.com/pingcap/ticdc/issues/919)
+ [TiDB Lightning: To fix the issue the Local-backend misses a lot of index KVs with partitioned tables](https://github.com/pingcap/tidb-lightning/issues/401)

### Engine

[RocksDB: To fix the issue that the cache key conflict leads to data corruption](https://github.com/tikv/tikv/issues/8243)

### Scheduling

+ [To implement the global TSO generation algorithm](https://github.com/tikv/pd/issues/2984)
+ [To split Regions handled by PD](https://github.com/tikv/pd/issues/2965)

### TiUP

+ [Not to pull up the whole cluster while scaling out the cluster](https://github.com/pingcap/tiup/issues/823)
+ [To support merging offline packages](https://github.com/pingcap/tiup/issues/814)

## Call for participation

### DDL

[To solve the issue that creating table with the invalid `double(50)` data type should return a syntax error](https://github.com/pingcap/tidb/issues/20217)

### Kubernetes

[To generate CRD manifest with more validation schemas](https://github.com/pingcap/tidb-operator/issues/3213)

### Scheduling

+ [To add some tests to check Region size in Region tree](https://github.com/tikv/pd/issues/3034)
+ [To record the API modification history](https://github.com/tikv/pd/issues/2971)

### TiUP

[To add a lock to avoid multiple tiup-cluster instances running on the same time](https://github.com/pingcap/tiup/issues/809)

## New contributors

We'd like to welcome the following new contributors to TiDB and thank them for their work!

tidb:

* [hesper-guo](https://github.com/hesper-guo)
* [pengdaqian2020](https://github.com/pengdaqian2020)
* [blueseason](https://github.com/blueseason)
* [Howie66](https://github.com/Howie66)
* [YangKian](https://github.com/YangKian)
* [Hunsmore](https://github.com/Hunsmore)
* [Patrick0308](https://github.com/Patrick0308)
* [Lvnszn](https://github.com/Lvnszn)
* [TszKitLo40](https://github.com/TszKitLo40)
* [SailerNote](https://github.com/SailerNote)
* [asiafrank](https://github.com/asiafrank)

tinysql:

* [divanodestiny](https://github.com/divanodestiny)

rust-prometheus:

* [thatdevsherry](https://github.com/thatdevsherry)

pd:

* [yassun](https://github.com/yassun)
* [duduainankai](https://github.com/duduainankai)

parser:

* [LENSHOOD](https://github.com/LENSHOOD)

docs-cn:

* [XiaoGe2030](https://github.com/XiaoGe2030)
* [sultan8252](https://github.com/sultan8252)
* [Jingyuma](https://github.com/Jingyuma)

dm:

* [fossabot](https://github.com/fossabot)

client-rust:

* [georgeteo](https://github.com/georgeteo)

pingcap.github.io:

* [manyu-li](https://github.com/manyu-li)
