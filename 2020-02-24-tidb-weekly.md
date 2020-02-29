---
title: Weekly update (February 17 ~ February 23, 2020)
date: 2020-02-24
summary: Last week, we landed 52 PRs in the TiDB repository, 1 PR in the TiSpark repository, and 43 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog posts

High read latency and network traffic are common issues for a multi-region architecture. At TiDB Hackathon 2019, a team won 2nd place by reducing multi-region read latency and network traffic by 50%.

Last week, we published a post that introduces how the team reduced the read latency and network traffic by half for a multi-region architecture. If you have similar problems, we hope this post will help you.

The full post is here:

[How We Reduced Multi-region Read Latency and Network Traffic by 50%](https://pingcap.com/blog/how-we-reduced-multi-region-read-latency-and-network-traffic-by-50/)

Last week, we also published the third (and last, for now) post in a series on remote work by Nick Cameron. This post talks a bit about some of the practicalities, specifically around work/life balance.

The full post is here:

[Remote Work - Part 3](https://pingcap.com/blog/remote-work-part-3/)

## Community

### New Committer

Congratulations to [TennyZhuang](https://github.com/TennyZhuang) as the new TiKV Committer!

Before becoming a Committer, TennyZhuang had been reviewing PRs for the TiKV community as a Reviewer, and gradually got familiar with the Coprocessor module. He made the following contributions to the TiKV community:

* Greatly improved the performance of `LIKE()`: tikv/tikv [#5866](https://github.com/tikv/tikv/pull/5866)
* Greatly improved the performance of `IN()`: tikv/tikv [#6000](https://github.com/tikv/tikv/pull/6000)
* Refined TiDB's time format to be 8 bytes as TiKV: tikv/tikv [#6418](https://github.com/tikv/tikv/pull/6418)
* Participated in implementing the collation for TiKV: tikv/tikv [#6592](https://github.com/tikv/tikv/pull/6592)
* Accepted the RPN expression to support complex expressions: tikv/tikv [#6313](https://github.com/tikv/tikv/pull/6313)
* Implemented the metadata framework: tikv/tikv [#5993](https://github.com/tikv/tikv/pull/5993)

Thank him for his contributions to the community!

### New contributors

tikv:

* [Poytr1](https://github.com/Poytr1)

docs:

* [oraluben](https://github.com/oraluben)
* [qqbuby](https://github.com/qqbuby)

tidb-operator:

* [mightyguava](https://github.com/mightyguava)

chaos-mesh:

* [oraluben](https://github.com/oraluben)

## Call for participation

* [Issues to solve for TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)
* [Issues to solve for TiKV](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

Last week, we landed [52 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2020-02-17..2020-02-23+) in the TiDB repository, [1 PR](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2020-02-17..2020-02-23) in the TiSpark repository, and [43 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2020-02-17..2020-02-23&type=Issues) in the TiKV and PD repositories.

### Critical PRs

TiDB:

* [Support defining `decimal` for the virtual table in `information_schema`](https://github.com/pingcap/tidb/pull/14896)
* [Add more diagnosis rules to check some metrics thresholds](https://github.com/pingcap/tidb/pull/14882)
* [Make `CLUSTER_SLOW_QUERY` support querying slow logs at any time](https://github.com/pingcap/tidb/pull/14878)
* [Specify the time range via the `TIME_RANGE` hint for the metrics or inspection tables](https://github.com/pingcap/tidb/pull/14874)
* [Fix the wrong result of `BatchPointGet` when the plan cache is enabled](https://github.com/pingcap/tidb/pull/14855)
* [Consider collations when calculating hash values in `HashJoin`](https://github.com/pingcap/tidb/pull/14836)
* [Reload the TiKV or TiDB cluster TLS for every newly established connection](https://github.com/pingcap/tidb/pull/14833)
* [Add a check to reject changing some configuration items during the runtime](https://github.com/pingcap/tidb/pull/14830)
* [Implement the non-stream physical scan lock for the GC worker](https://github.com/pingcap/tidb/pull/14812)
* [Resolve the left secondary lock to avoid the dead loop](https://github.com/pingcap/tidb/pull/14787)

TiSpark:

* [Fix the partition pruning](https://github.com/pingcap/tispark/pull/1385)

TiKV and PD:

* [Add the stack size and the maximum task number to the unified read pool](https://github.com/tikv/tikv/pull/6597)
* [Add the `Cmd` observer to Raftstore](https://github.com/tikv/tikv/pull/6602)
* [Implement non-streaming `physical_scan_lock` to the GC worker](https://github.com/tikv/tikv/pull/6631)
* [Make the `Vec-TonN` executor aware of the collation of ordering expressions in Coprocessor](https://github.com/tikv/tikv/pull/6608)
* [Migrate TiKV to abstract `TablePropertiesCollection` types](https://github.com/tikv/tikv/pull/6630)
* [Add the component sub-command](https://github.com/pingcap/pd/pull/2092)
* [Improve the performance of leader transferring by returning multiple operators in batches](https://github.com/pingcap/pd/pull/2081)
* [Modify `TopN` to support the multidimensional load](https://github.com/pingcap/pd/pull/2140)
