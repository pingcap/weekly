---
title: TiDB Monthly Update (January 2021)
date: 2021-02-01
summary: Here's what TiDB has achieved in January.
tags: ['TiDB', 'TiUP', 'TiDB Dashboard', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Monthly Update for January 2021

## Releases

We have four releases this month:

+ [TiDB 5.0 RC Release Notes](https://docs.pingcap.com/tidb/v5.0/release-5.0.0-rc)
+ [TiDB 4.0.10 Release Notes](https://docs.pingcap.com/tidb/stable/release-4.0.10)
+ [TiDB Operator 1.2.0-alpha.1 Release Notes](https://docs.pingcap.com/tidb-in-kubernetes/dev/release-1.2.0-alpha.1)
+ [TiDB Operator 1.1.10 Release Notes](https://docs.pingcap.com/tidb-in-kubernetes/stable/release-1.1.10)

## Blog posts

Our CEO Max Liu, in [Five Principles that Guide TiDB and PingCAP (Part I)](https://pingcap.com/blog/five-principles-that-guide-tidb-and-pingcap) and [Five Principles that Guide TiDB and PingCAP (Part II)](https://pingcap.com/blog/five-principles-that-guide-tidb-and-pingcap-II), talked about the philosophy behind TiDB's evolution, and, as a product manager, how he figured out where TiDB would be going and how we finally got there.

In [GitHub Discussions: Bringing the Open Source Community Closer Together and All in GitHub](https://pingcap.com/blog/github-discussions-bringing-the-open-source-community-closer-together-and-all-in-github), Keke Yi explained why the open source community was scattered around the Internet, how GitHub Discussions brought the community closer together, and why the open source community's future tended to be all in GitHub.

[How to Simulate I/O Faults at Runtime](https://pingcap.com/blog/how-to-simulate-io-faults-at-runtime), written by Keao Yang, introduced how we implemented the IOChaos experiment without using a sidecar.

In [Announcing the TiDB Incubator Program](https://pingcap.com/blog/announcing-tidb-incubator-program), we were excited to introduce the TiDB Incubator Program, a program designed to ensure that new projects in the TiDB ecosystem can obtain resources and help from the community towards their desired maturity level.

## Important pull requests

### Planner

+ [Build the global statistics for partitioned tables](https://github.com/pingcap/tidb/pull/22472)
+ [Retry executing SQL statements without TiFlash after TiFlash is down](https://github.com/pingcap/tidb/pull/22459)

### SQL-Infra

+ [Fix the issue that the `UPDATE` statements can see columns that are not public](https://github.com/pingcap/tidb/pull/22307)

### Kubernetes

+ [Support customizing the slow log storage](https://github.com/pingcap/tidb-operator/pull/3731)
+ [Support cancelling backup and restore jobs using the signal and update the status with the failed Pod](https://github.com/pingcap/tidb-operator/pull/3696)

### Migrate

+ [Fix the issue that the changefeed's output is out of order in TiCDC](https://github.com/pingcap/ticdc/pull/1247)
+ [Try to create tables in parallel in TiDB Lightning](https://github.com/pingcap/tidb-lightning/pull/502)

### TiUP

+ [Remove `v0manifest`](https://github.com/pingcap/tiup/pull/1078)
+ [Support the checkpoint](https://github.com/pingcap/tiup/pull/1069)

## Important issues

### Planner

+ [To reduce the optimizer's CPU usage when handling the very large `IN(...)` expression](https://github.com/pingcap/tidb/issues/22412)

### SQL-Infra

+ [To fix the issue that `ALTER TABLE` and `ADD INDEX` report the `panic in the recoverable goroutine` error](https://github.com/pingcap/tidb/issues/22453)
+ [To fix the issue that it fails to create bindings in the database with the name that contains a dash](https://github.com/pingcap/tidb/issues/22388)
+ [To fix the issue that the Region information in `information_schema.tikv_reigon_status` is different from that in HTTP API](https://github.com/pingcap/tidb/issues/22225)

### Execution

+ [To fix the issue that `point_get` gets the wrong result under `@@tidb_snapshot`](https://github.com/pingcap/tidb/pull/22460)

### Kubernetes

+ [To fix the issue that `recoverFailover` might be forgotten to unset](https://github.com/pingcap/tidb-operator/issues/3335)
+ [To deprecate the Pod validating and mutating webhook](https://github.com/pingcap/tidb-operator/issues/3497)

### Migrate

+ [To fix the issue of BR out of memory (OOM) when backing up using the version 4.0.9](https://github.com/pingcap/br/issues/704)
+ [To work on the issue that TiDB Data Migration relay's behavior should align with that of MySQL when using GTID](https://github.com/pingcap/dm/issues/1383)

### TiUP

+ [To import the Ansible cluster to TiUP without the user-defined port parameter in `group_vars`](https://github.com/pingcap/tiup/issues/1034)

## Call for participations

### Planner

+ [To fix the issue that the current statistics histogram of a multi-column index actually serves as a single column index](https://github.com/pingcap/tidb/issues/22589)

### SQL-Infra

+ [To fix the issue that `gocritic` reports many warnings](https://github.com/pingcap/tidb/issues/20859)
+ [To fix the issue that the Digest text changes the SQL semantics](https://github.com/pingcap/tidb/issues/18907)

### Execution

+ [To fix the TiDB panic that occurs when the goroutine stack exceeds the 1000000000-byte limit](https://github.com/pingcap/tidb/issues/22238)
+ [To fix the issue that `delete .. where in` in a transaction does not take effect](https://github.com/pingcap/tidb/issues/22243)

### Kubernetes

+ [To deprecate the Pod validating and mutating webhook](https://github.com/pingcap/tidb-operator/issues/3497)
+ [To fix the `MaxBackup`'s behavior on `BackupSchedule`](https://github.com/pingcap/tidb-operator/issues/3660)

### TiUP

+ [To fix the issue that the Grafana data source is not found when the cluster name contains `test-cluster`](https://github.com/pingcap/tiup/issues/665)

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

dm:

+ [Kuri-su](https://github.com/Kuri-su)

chaos-mesh:

+ [Gallardot](https://github.com/Gallardot)
+ [vincent178](https://github.com/vincent178)
+ [AngleNet](https://github.com/AngleNet)

client-rust:

+ [weihanglo](https://github.com/weihanglo)
