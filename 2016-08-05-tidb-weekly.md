---
title: Weekly update (July 30 ~ August 05, 2016)
date: 2016-08-05
summary: Last week, we landed 28 PRs in the TiDB repositories and 32 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV', 'Placement Driver']
---

# Weekly update (July 30 ~ August 05, 2016)

Last week, we landed [28 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-07-30..2016-08-05%20) in the TiDB repositories and [32 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2016-07-30..2016-08-05+&type=Issues&ref=searchresults) in the TiKV repositories.

## Notable changes to `TiDB`

+ Add support for constant folding in the SQL optimizer.
+ Optimize the query speed of the secondary index. In certain scenarios, only the data in the index needs to be read.
+ Use dynamic programing to decide the join path for multiple tables.
+ Adjust the command line to support setting the listening address.
+ Prometheus metrics and golang pprof share the same port.
+ Update the  [Documents](https://github.com/pingcap/docs) repository.
+ Fix several bugs.
## Notable changes to `TiKV`

+ Split the operations on RocksDB from scheduler thread to a worker pool.
+ Support leader lease mechanism when the quorum check is enabled. 
+ Use `pending snapshot regions check` to avoid receiving multiple overlapping snapshots at the same time.
+ Check down peers and report to Placement Driver(PD).
+ Support time monitor to check whether time jumps back or not.

## Notable changes to `Placement Driver`

+ Reduce the "1234" and "9090" ports in PD. Now PD has only "2379" and "2380" ports for external use. 
+ Support the `join` flag to let PD join an existing cluster dynamically.
+ Support the `remove PD member` API to remove a PD from a cluster dynamically.
+ Support the `list PD members` API.
