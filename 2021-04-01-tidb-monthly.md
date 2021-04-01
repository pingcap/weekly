---
title: TiDB Monthly Update for March 2021
date: 2021-04-01
summary: Here's what TiDB has achieved in March 2021.
tags: ['TiDB', 'TiUP', 'TiDB Dashboard', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Monthly Update for March 2021

## Blog posts

Xiang Wang wrote an article [tidb-lite: A go-sqlmock Alternative for Easily Unit Testing Golang Database-Related Code](https://pingcap.com/blog/tidb-lite-go-sqlmock-alternative-for-easily-unit-testing-golang-database-related-code) to introduce how to use tidb-lite to unit test database-related code. The article looked at the limitations of go-sqlmock, discussed tidb-lite's advantages, and then showed an example of tidb-lite in action.

In [Announcing the TiDB Hacking Camp](https://pingcap.com/blog/announcing-the-tidb-hacking-camp), we announced that we launched an 8-week TiDB Hacking Camp, an incubation program to actually land these projects in the community.

[TiDB on Arm-based Kubernetes Cluster Achieves Up to 25% Better Price-Performance Ratio than x86](https://pingcap.com/blog/tidb-on-arm-based-k8s-cluster-achieves-up-to-25-percent-better-price-performance-ratio-than-x86), an article written by Ron Xing, compared the performance of TiDB, a MySQL compatible NewSQL database, running on an Arm-based Amazon Elastic Kubernetes Service (EKS) cluster and on an x86-based EKS cluster.

Jinpeng Zhang (TiKV Maintainer) and Bokang Zhang (TiKV Committer) wrote an article [TiDB Hackathon: Reducing Cross-AZ Data Transfer Costs by 89%](https://pingcap.com/blog/tidb-hackathon-reducing-cross-az-data-transfer-costs-by-89-percent) that showed you our whole journey through TiDB Hackathon 2020.

[TiDB Operator Source Code Reading (I): Overview](https://pingcap.com/blog/tidb-operator-source-code-reading-1-overview) is the first article of a series that walked you through the TiDB Operator source code. In this article, Yiwen Chen (Committer of TiDB Operator), the author, introduced to you TiDB Operator's architecture, its core components, and what it's used for.

Jun Yu, our solution architect, in his article [Using TiDB in Mission Critical Scenarios of the Financial Industry (Part I)](https://pingcap.com/blog/using-tidb-in-mission-critical-scenarios-of-the-financial-industry-part-1), introduced the critical business scenarios of the financial industry and the pain points our financial adopters had using their current technology. Then, he also showed you three TiDB solutions that tackled these problems.

## Important pull requests

### Planner

[Optimize the performance of restore with the database](https://github.com/pingcap/tidb/pull/22910)

### SQL-Infra

+ [Fix the issue that changing a column from nullable to `NOT NULL` is not 'SQL_MODE'-aware](https://github.com/pingcap/tidb/pull/23430)
+ [Fix the issue that the DDL operation hangs over when it meets panic in the cancelling path](https://github.com/pingcap/tidb/pull/23204)

### Execution

+ [Add telemetry for Coprocessor cache, TiFlash, clustered index, and async commit](https://github.com/pingcap/tidb/pull/23454)

### Kubernetes

+ [Fix the issue of resizing PVC in multiple PVC settings](https://github.com/pingcap/tidb-operator/pull/3858)
+ [Respect the `Spec` settings in `Backup`/`Restore` jobs](https://github.com/pingcap/tidb-operator/pull/3835)

### Migrate

+ [Add the configuration file for the server in TiCDC](https://github.com/pingcap/ticdc/pull/1493)
+ [Restore schemas in parallel in TiDB Data Migration (DM)](https://github.com/pingcap/dm/pull/1466)

### TiUP

+ [Fix the issue that when endpoints are empty in the scaling-out process](https://github.com/pingcap/tiup/pull/1227)

## Important issues

### Planner

+ [To fix the unreasonable behavior of `modify_count` in `show stats_meta`](https://github.com/pingcap/tidb/issues/23453)
+ [To fix the issue that the auto-analyze processing on an unanalyzed table is not controlled by the analysis time range](https://github.com/pingcap/tidb/issues/23160)

### SQL-Infra

+ [To fix the issue that the Range columns partition table does not support the binary data type](https://github.com/pingcap/tidb/issues/23464)

### Execution

+ [To fix the issue that TiFlash reports `BadRequest` when pushing the timestamp down](https://github.com/pingcap/tidb/issues/22917)

### Kubernetes

+ [To fix the issue that `recoverFailover` might be forgotten to unset](https://github.com/pingcap/tidb-operator/issues/3335)
+ [To deprecate the Pod validating and mutating webhook](https://github.com/pingcap/tidb-operator/issues/3497)

### Migrate

+ [To track the compatibility issue of clustered index with BR](https://github.com/pingcap/br/issues/790)
+ [To fix the issue in TiCDC that the atomicity of transactions is broken in the downstream when using async commit](https://github.com/pingcap/ticdc/issues/1498)

### TiUP

+ [To fix the issue that the nightly version cannot be updated](https://github.com/pingcap/tiup/issues/1203)

## Call for participations

### Planner

[To fix the issue that `SHOW ANALYZE STATUS` misses the finish time for each task](https://github.com/pingcap/tidb/issues/23451)

### SQL-Infra

+ [To fix the confusing output of `ADMIN SHOW DDL JOBS` with multiple jobs](https://github.com/pingcap/tidb/issues/23494)

### Kubernetes

+ [To deprecate the Pod validating and mutating webhook](https://github.com/pingcap/tidb-operator/issues/3497)
+ [To fix the `MaxBackups` behavior on `BackupSchedule`](https://github.com/pingcap/tidb-operator/issues/3660)

## New contributors

We'd like to welcome the following new contributors to TiDB and thank them for their work!

tidb:

+ [ankitdobhal](https://github.com/ankitdobhal)
+ [jianzhiyao](https://github.com/jianzhiyao)
+ [Ahacad](https://github.com/Ahacad)
+ [hanlins](https://github.com/hanlins)
+ [knull-cn](https://github.com/knull-cn)
+ [An-DJ](https://github.com/An-DJ)
+ [Willendless](https://github.com/Willendless)

tikv:

+ [iliveforfun](https://github.com/iliveforfun)
+ [ZingLix](https://github.com/ZingLix)

pd:

+ [mantuliu](https://github.com/mantuliu)
+ [bufferflies](https://github.com/bufferflies)

tidb-operator:

+ [hhy5861](https://github.com/hhy5861)
+ [rudeigerc](https://github.com/rudeigerc)
+ [dragonly](https://github.com/dragonly)

tidb-dashboard:

+ [LINKIWI](https://github.com/LINKIWI)

dumpling:

+ [recall704](https://github.com/recall704)

badger:

+ [hslam](https://github.com/hslam)

pprof-rs:

+ [rrbutani](https://github.com/rrbutani)

telemetry-log-collector:

+ [634750802](https://github.com/634750802)

raft-rs:

+ [storagezhang](https://github.com/storagezhang)

test-store:

+ [PragmaTwice](https://github.com/PragmaTwice)

tug-website:

+ [hustKiwi](https://github.com/hustKiwi)

docs:

+ [rkazak](https://github.com/rkazak)
+ [dbsid](https://github.com/dbsid)

docs-cn:

+ [zoujia-cm](https://github.com/zoujia-cm)
+ [xyqcmss](https://github.com/xyqcmss)
+ [hey-hoho](https://github.com/hey-hoho)

qa:

+ [wanliyi](https://github.com/wanliyi)
