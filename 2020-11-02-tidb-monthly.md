---
title: TiDB Monthly Update (October 2020)
date: 2020-11-02
summary: Here's what TiDB has achieved in October.
tags: ['TiDB', 'TiUP', 'TiDB Dashboard', 'TiSpark', 'PD']
---

# TiDB Monthly Update for October 2020

## Releases

We have three releases this month:

+ [TiDB 4.0.8 Release Notes](https://docs.pingcap.com/tidb/stable/release-4.0.8)

    + New features

        + Support the new aggregate function `APPROX_PERCENTILE`
        + Support pushing down `CAST` functions
        + Support the snapshot-level consistent replication

    + Improvements

        + Prioritize low-selectivity indexes in the greedy search procedure of `Selectivity()` in TiDB
        + Add the Fast-Tune panel page to assist performance diagnostics in TiKV
        + Add monitoring metrics of Raft logs in TiFlash

    + Bug Fixes

+ [TiDB Data Migration 2.0 GA Release Notes](https://docs.pingcap.com/tidb-data-migration/stable/2.0.0-ga)

    + Improvements

        + Optimize the `safe-mode` setting to ensure the eventual consistency of data when the upstream database, such as Amazon Aurora and Aliyun RDS, does not support FTWRL in the full export [#981](https://github.com/pingcap/dm/pull/981) [#1017](https://github.com/pingcap/dm/pull/1017)
        + Support automatic configuration of `sql_mode` for data migration based on the global `sql_mode` of upstream and downstream databases and `sql_mode` of binlog events [#1005](https://github.com/pingcap/dm/pull/1005) [#1071](https://github.com/pingcap/dm/pull/1071) [#1137](https://github.com/pingcap/dm/pull/1137)
        + Support automatic configuration of `max_allowed_packet` from DM to the downstream TiDB, based on the global `max_allowed_packet` value of the downstream TiDB [#1071](https://github.com/pingcap/dm/pull/1071)

    + Bug fixes

+ [TiDB Operator 1.1.6 Release Notes](https://docs.pingcap.com/tidb-in-kubernetes/stable/release-1.1.6)

## Blog posts

Yihao Zhang, the Senior development engineer at Xiaohongshu, wrote an article [How We Use a Scale-Out HTAP Database for Real-Time Analytics and Complex Queries](https://pingcap.com/success-stories/how-we-use-a-scale-out-htap-database-for-real-time-analytics-and-complex-queries/) that described why they chose TiDB and how TiDB's real-time HTAP capabilities help them manage their data in some scenarios.

In [Lessons from TiDB's No. 1 Bug Hunters Who've Found 400+ Bugs in Popular DBMSs](https://pingcap.com/blog/lessons-from-tidb-no.-1-bug-hunters-who-have-found-over-400-bugs-in-popular-dbmss/), Manuel Rigger, the postdoctoral fellow at ETH Zurich, described the techniques that have made him and his colleague, Professor Zhendong Su, TiDB's #1 bug hunters.

[How We Use a Distributed Database to Achieve Horizontal Scaling Without Downtime](https://pingcap.com/success-stories/how-we-use-a-distributed-database-to-achieve-horizontal-scaling-without-downtime/), written by Zhendong Chen, the software development engineer at Bank of Beijing, shared with you why they chose TiDB and how they use it to achieve horizontally scalable, always-on infrastructure.

Yu Han, the engineer at Information Technology Operations Center, Bank of China, wrote an article [How Bank of China Uses a Scale-Out Database to Support Zabbix Monitoring at Scale](https://pingcap.com/success-stories/how-bank-of-china-uses-a-scale-out-database-to-support-zabbix-monitoring-at-scale/) that introduced the traditional Zabbix monitoring solution they adopted and their pain points at the time, how they used TiDB in Zabbix, and their further plans to optimize TiZabbix.

We published [TiDB X Hacktoberfest 2020 - An Invitation to Open Source](https://pingcap.com/blog/tidb-x-hacktoberfest-2020-an-invitation-to-open-source/) to invite you to be part of us, starting from our handpicked issues with proper mentoring and assistance along your journey.

We also published [TiCDC GA: Offering High-Availability Replication Services for Production Environments](https://pingcap.com/blog/ticdc-ga-offer-high-availability-replication-services-for-production-environments/) to announce the general availability of TiCDC, and to walk you through TiCDC's features, application scenarios, and real-world case studies.

Youzhi Zhu, the big data architect at ZTO Express, wrote an article [Why We Migrated from Exadata to a Scale-Out HTAP Database for Near Real-Time Analytics](https://pingcap.com/success-stories/why-we-migrated-from-exadata-to-a-scale-out-htap-database-for-near-real-time-analytics/), described why they chose TiDB as their solution and how TiDB helps scale out their database and supports their multi-dimensional analytics with query response times in minutes.

In [Making an HTAP Database a Reality: What I Learned from PingCAP's VLDB Paper](https://pingcap.com/blog/making-htap-database-reality-what-i-learned-from-pingcap-vldb-paper/), Xianlin Chen, the DBA at PalFish, shared with you his thoughts about TiDB's implementation of an HTAP database that provides strong data consistency and resource isolation, as well as his expectations of TiDB in the future.

[Running a Scale-Out Database on ARM as a MySQL Alternative](https://pingcap.com/success-stories/running-a-scale-out-database-on-arm-as-mysql-alternative/), written by Birong Huang, the senior engineer at U-Next, shared with you why they chose to put their data in TiDB and run it on ARM, and the detailed benchmarking tests of TiDB on ARM.

Our engineer Shuang Chen wrote an article [Metrics Relation Graph Helps DBAs Quickly Locate Performance Problems in TiDB](https://pingcap.com/blog/metrics-relation-graph-helps-dba-quickly-locate-performance-problems/) to introduce a new feature in its web UI TiDB Dashboard: the metrics relation graph.

## Important pull requests

### Planner

+ [Support using the variable to prefer index scan](https://github.com/pingcap/tidb/pull/18996)
+ [Estimate the count of index rows using extended correlation statistics](https://github.com/pingcap/tidb/pull/20160)
+ [Do not push down `NULL`-sensitive join conditions](https://github.com/pingcap/tidb/pull/19620/)

### DDL

+ [Support dropping multiple indexes in one statement](https://github.com/pingcap/tidb/pull/20457)
+ [Handle the placement rule cache for dropping/truncating/recovering/flashing back tables](https://github.com/pingcap/tidb/pull/20622)

### Kubernetes

+ [Support mounting multiple PVCs for TiKV](https://github.com/pingcap/tidb-operator/pull/3425)
+ [Support passing the raw toml configuration for TiKV/PD as the string type](https://github.com/pingcap/tidb-operator/pull/3342)

### Execution

+ [Support querying the backoff detail in `SLOW_QUERY` and add the column of runtime statistics to `STATEMENTS_SUMMARY` and `SLOW_QUERY`](https://github.com/pingcap/tidb/pull/20300)
+ [Enable the inline projection for `Limit`](https://github.com/pingcap/tidb/pull/20288)
+ [Support the variable-setting hint `SET_VAR`](https://github.com/pingcap/tidb/pull/20232)

### Migrate

+ [Make `split` and `restore` pipelined in BR](https://github.com/pingcap/br/pull/427)
+ [Support a snapshot-map in replication for TiCDC](https://github.com/pingcap/ticdc/pull/932)

### TiUP

+ [Support the offline package merge](https://github.com/pingcap/tiup/pull/860)

## Important issues

### Planner

+ [To fix the issue that the plan binding evolution rejects improved plans](https://github.com/pingcap/tidb/issues/20417)

### DDL

+ [To fix the issue that column flags are cleared after the `CHANGE COLUMN` operation](https://github.com/pingcap/tidb/issues/20720)

### Kubernetes

+ [To fix the issue that `recoverFailover` might be forgotten to unset](https://github.com/pingcap/tidb-operator/issues/3335)
+ [To upgrade TiDB gracefully](https://github.com/pingcap/tidb-operator/issues/3318)

### Execution

+ [To support the cloud storage as the source or destination of `SELECT ... INTO OUTFILE` and `LOAD DATA`](https://github.com/pingcap/tidb/issues/20582)
+ [To make the stream aggregation operators in parallel by using shuffle operators](https://github.com/pingcap/tidb/issues/20651)

### TiUP

[To patch the command corner case that occurs when using a wrong `tar.gz` file](https://github.com/pingcap/tiup/issues/846)

## Call for participations

### Planner

+ [To support showing the TiDB-executed tasks of collecting the historical and cluster-level statistics](https://github.com/pingcap/tidb/issues/20141)

### DDL

+ [To fix the issue that altering placement rules misreports `ErrBuildRuleList`](https://github.com/pingcap/tidb/issues/20669)

### Kubernetes

+ [To update `crd.yaml` for the latest kubernetes version](https://github.com/pingcap/tidb-operator/issues/3436)

### Execution

+ [To fix the different error code from MySQL returned when inserting the incorrect time value](https://github.com/pingcap/tidb/issues/20207)

### Migrate

+ [To record the store ID when `download`/`ingest` fails in BR](https://github.com/pingcap/br/issues/556)
+ [To support TLS `skip-verify` in Dumpling](https://github.com/pingcap/dumpling/issues/170)
+ [To add a guide in the document of the incremental mode](https://github.com/pingcap/dm/issues/1155)

### TiUP

[To fix the issue that components quit in an unexpected order in TiUP Playground](https://github.com/pingcap/tiup/issues/859)

## New contributors

We'd like to welcome the following new contributors to TiDB and thank them for their work!

tidb:

* [William0423](https://github.com/William0423)
* [jianyilyu](https://github.com/jianyilyu)
* [Howie59](https://github.com/Howie59)

tikv:

* [hbina](https://github.com/hbina)

docs-cn:

* [wanjuntham](https://github.com/wanjuntham)
* [ofey404](https://github.com/ofey404)

dumpling:

* [Abingcbc](https://github.com/Abingcbc)

pingcap-incubator:

* [Sahil-Sinha](https://github.com/Sahil-Sinha)

tibigdata:

* [youngwookim](https://github.com/youngwookim)

tidb-operator:

* [L3T](https://github.com/L3T)

tinysql:

* [zstone12](https://github.com/zstone12)

tispark:

* [Dieken](https://github.com/Dieken)

website:

* [cw1997](https://github.com/cw1997)
* [carsonoid](https://github.com/carsonoid)
