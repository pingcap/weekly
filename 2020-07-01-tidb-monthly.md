---
title: TiDB Monthly Update (June 2020)
date: 2020-07-01
summary: Here's what TiDB has achieved in June.
tags: ['TiDB', 'TiUP', 'TiDB Dashboard', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Monthly Update for June 2020

## Releases

We have four releases this month:

+ [TiDB 4.0.1 Release Notes](https://docs.pingcap.com/tidb/v4.0/release-4.0.1)

    + New features
        + Add the `--advertise-status-addr` start flag to specify the status address to `advertise` [#8046](https://github.com/tikv/tikv/pull/8046)
        + Support the internal proxy for the built-in TiDB Dashboard [#2511](https://github.com/pingcap/pd/pull/2511)
        + Support the TiDB new collation framework
    + Bug fixes

+ [TiDB 3.1.2 Release Notes](https://docs.pingcap.com/tidb/v4.0/release-3.1.2)

    + Bug fixes

+ [TiDB 3.0.15 Release Notes](https://docs.pingcap.com/tidb/v4.0/release-3.0.15)

    + New features
        + Support the `admin recover index` and  `admin check index` statements on partitioned tables [#17315](https://github.com/pingcap/tidb/pull/17315) [#17390](https://github.com/pingcap/tidb/pull/17390)
        + Add a policy in which PD performs scheduling in terms of the number of leaders [#2479](https://github.com/pingcap/pd/pull/2479)
        + Optimize the output of `SHOW CREATE TABLE` and add quotation marks to the partition name [#16315](https://github.com/pingcap/tidb/pull/16315)
    + Bug fixes

+ [TiDB Cloud Beta](https://docs.pingcap.com/tidbcloud/beta)

## Blog posts

Siddon Tang, the Chief Architect at PingCAP, in his article [TiDB 4.0 GA, Gearing You Up for an Unpredictable World with a Real-Time HTAP Database](https://pingcap.com/blog/tidb-4.0-ga-gearing-you-up-for-an-unpredictable-world-with-real-time-htap-database) announces that TiDB 4.0 has reached general availability (GA).

In [Announcing TiDB as a Service, Fully-Managed TiDB Offering](https://pingcap.com/blog/announcing-tidb-as-a-service-fully-managed-tidb-offering), we are thrilled to announce the beta release of TiDB Cloud, the fully-managed TiDB service delivered by PingCAP.

[VLDB 2020: TiDB, A Raft-based HTAP Database](https://pingcap.com/blog/vldb-2020-tidb-a-raft-based-htap-database) introduces how we will contribute our novel ideas on databases and distributed systems back to the academic community.

Wei Liu's article [How We Improved TPC-C Performance by 50% and TPC-H Performance by 100%](https://pingcap.com/blog/how-we-improved-tpcc-performance-50-percent-and-tpch-performance-100-percent) shows you how we significantly enhanced TiDB 4.0's TPC-C and TPC-H performance.

Brian Anderson has written [Rust's Huge Compilation Units](https://pingcap.com/blog/rust-huge-compilation-units) and [Generics and Compile-Time in Rust](https://pingcap.com/blog/generics-and-compile-time-in-rust) to explore Rust's compile times within the context of TiKV, the key-value store behind the TiDB database.

## Notable pull requests

### Planner

+ [Support building the clustered index range for the table scan](https://github.com/pingcap/tidb/pull/18018)
+ [Support clustered indexes for the double read](https://github.com/pingcap/tidb/pull/18127)

### DDL

+ [Fix the issue that `ALTER TABLE EXCHANGE PARTITION` does not work if the table has TiFlash replicas](https://github.com/pingcap/tidb/pull/17940)
+ [Add warnings for constraints and checks](https://github.com/pingcap/tidb/pull/17830)

### TiDB Dashboard

+ [Provide a better UI for the multi-selection and the instance selection](https://github.com/pingcap-incubator/tidb-dashboard/pull/632)
+ [Support the headless mode](https://github.com/pingcap-incubator/tidb-dashboard/pull/628)
+ [Add the telemetry feature](https://github.com/pingcap-incubator/tidb-dashboard/pull/644)

### Tools

+ [Support the pipelined restore in Backup & Restore (BR)](https://github.com/pingcap/br/pull/266)
+ [Add the local backend in TiDB Lightning](https://github.com/pingcap/tidb-lightning/pull/326)

### Engine

+ [Split SSTs by Region boundaries](https://github.com/tikv/tikv/pull/8115)
+ [Improve the TiKV Region size estimation by counting deleted tombstones](https://github.com/tikv/tikv/pull/8079)
+ [Support dynamically changing `rate-bytes-per-sec`](https://github.com/tikv/tikv/pull/8124)

### Scheduling

+ [Support scattering Regions in stores with special engines (like TiFlash)](https://github.com/pingcap/pd/pull/2531)
+ [Make the operator fail immediately if the leader is changed to `RemovePeer`](https://github.com/pingcap/pd/pull/2530)
+ [Introduce `StoreCandidates` and replace `RandomSelector`](https://github.com/pingcap/pd/pull/2552)
+ [Improve the way to set the store limit and deprecate `store-balance-rate`](https://github.com/pingcap/pd/pull/2437)
+ [Set a suitable default store limit of the TiFlash stores](https://github.com/pingcap/pd/pull/2559)

### TiUP

+ [Enable TiFlash in TiUP Playground on Mac](https://github.com/pingcap/tiup/pull/527)
+ [Support scaling-in and scaling-out in TiUP Playground](https://github.com/pingcap/tiup/pull/416)

## Notable issues

### Planner

+ [To improve the correctness and robustness of the index selection](https://github.com/pingcap/tidb/issues/18065)

### DDL

+ [To try to increase the success rate of pessimistic transaction commits with concurrent DDL operations](https://github.com/pingcap/tidb/issues/17932)
+ [To add placement rules for a table through the DDL statement](https://github.com/pingcap/tidb/issues/18200)
+ [To support adding multiple indexes in one statement](https://github.com/pingcap/tidb/issues/18053)

### Tools

+ [To fix the issue that the DDL operation through `CREATE DATABASE` or `CREATE TABLE` gets wrong queries in BR](https://github.com/pingcap/br/issues/364)
+ [To fix the duplicated replication when `cyclic-replication` is enabled in TiCDC](https://github.com/pingcap/ticdc/issues/700)

### Engine

[To support RocksDB-Cloud](https://github.com/tikv/rust-rocksdb/issues/514)

### Scheduling

+ [To reduce the difference of size amplification between the new node and the original node](https://github.com/pingcap/pd/issues/2535)
+ [To increase the probability of balancing new Regions](https://github.com/pingcap/pd/issues/2524)

### TiUP

+ [To fetch `manifest`s concurrently](https://github.com/pingcap/tiup/issues/521)
+ [To reduce the memory usage when downloading components](https://github.com/pingcap/tiup/issues/443)

### Call for participation

Wanna participate with us? Take a look at the following help-wanted issues, which are mentoring available:

#### TiUP

+ [To add unit tests](https://github.com/pingcap/tiup/issues/344)

### DDL

+ [To allow the row function in TiDB expression indexes](https://github.com/pingcap/tidb/issues/18150)
+ [To fix the issue that `SHOW TABLE t next_row_id` shows dropped tables](https://github.com/pingcap/tidb/issues/18254)

### Scheduling

+ [To support changing the store limit according to the label](https://github.com/pingcap/pd/issues/2568)

### Tools

+ [To add test cases for more data types in sync-diff-inspector](https://github.com/pingcap/tidb-tools/issues/350)

## New contributors

We'd like to welcome the following new contributors to TiDB and thank them for their work!

tidb:

+ [raygift](https://github.com/raygift)
+ [JmPotato](https://github.com/JmPotato)
+ [lvvvl](https://github.com/lvvvl)
+ [markjenny](https://github.com/markjenny)
+ [chanme](https://github.com/chanme)
+ [xhebox](https://github.com/xhebox)
+ [songyzh](https://github.com/songyzh)

docs:

+ [littlesmilelove](https://github.com/littlesmilelove)
+ [lidaobing](https://github.com/lidaobing)

docs-cn:

+ [eastfisher](https://github.com/eastfisher)
+ [HuGanghui](https://github.com/HuGanghui)
+ [lemontree8801](https://github.com/lemontree8801)

parser:

+ [chanme](https://github.com/chanme)

pd:

+ [mgkanani](https://github.com/mgkanani)
+ [sunzhuohang](https://github.com/sunzhuohang)

## This Monthly in TiKV

For more detailed and comprehensive information about TiKV, we have TiKV Monthly Update. The following covers June.

[This Month in TiKV - June 2020](https://tikv.org/blog/monthly-june-2020/)
