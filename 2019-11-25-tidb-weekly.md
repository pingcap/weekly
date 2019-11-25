---
title: Weekly update (November 18 ~ November 24, 2019)
date: 2019-11-25
summary: Last week, we landed 145 PRs in the TiDB repository, 4 PRs in the TiSpark repository, and 76 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog posts

In recent years, building a large-scale distributed storage system has become a hot topic. Distributed consensus algorithms like Paxos and Raft are the focus of many technical articles. Last week, we published a post to share some of our firsthand experience in designing a large-scale distributed storage system based on the Raft consensus algorithm.

The full article is here:

[Building a Large-scale Distributed Storage System Based on Raft](https://pingcap.com/blog/building-a-large-scale-distributed-storage-system-based-on-raft/)

## Community

### New contributors

tidb:

- [AerysNan](https://github.com/AerysNan)
- [Lanearth](https://github.com/Lanearth)
- [YourLovely](https://github.com/YourLovely)
- [zouhuan1215](https://github.com/zouhuan1215)
- [SilvaXiang](https://github.com/SilvaXiang)
- [catror](https://github.com/catror)
- [someblue](https://github.com/someblue)
- [koushiro](https://github.com/koushiro)
- [Baytwt](https://github.com/Baytwt)
- [silver--bullet](https://github.com/silver--bullet)

tikv:

- [MaiCw4J](https://github.com/MaiCw4J)
- [AerysNan](https://github.com/AerysNan)
- [TommyCpp](https://github.com/TommyCpp)
- [Renkai](https://github.com/Renkai)
- [wangwangwar](https://github.com/wangwangwar)

pd:

- [qinggniq](https://github.com/qinggniq)
- [hrbeuyz24](https://github.com/hrbeuyz24)

docs-cn:

- [baiyuqing](https://github.com/baiyuqing)

## Call for participation

- [Vectorized Expression Working Group](https://github.com/pingcap/community/blob/master/working-groups/wg-vec-expr.md)
    - [`Date` or `Time` built-in functions (30/65)](https://github.com/pingcap/tidb/issues/12101)
    - [`Decimal` built-in functions (20/31)](https://github.com/pingcap/tidb/issues/12102)
    - [`Int` built-in functions (155/187)](https://github.com/pingcap/tidb/issues/12103)
    - [`JSON` built-in functions (22/27)](https://github.com/pingcap/tidb/issues/12104)
    - [`Real` built-in functions (46/49)](https://github.com/pingcap/tidb/issues/12105)
    - [`String` built-in functions (89/133)](https://github.com/pingcap/tidb/issues/12106)
    - [`Duration` built-in functions (17/45)](https://github.com/pingcap/tidb/issues/12176)
    - Last week, [43 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+sort%3Aupdated-desc+merged%3A2019-11-18..2019-11-24+label%3Acomponent%2Fexpression+) were landed in the expression component.

- Coprocessor SIG:
    - [Improve the performance of Chunk Encoder](https://github.com/tikv/tikv/issues/5729)
    - [Implement more UDFs](https://github.com/tikv/tikv/issues/5727)
    - [Implement the new row format](https://github.com/tikv/tikv/issues/5726)
    - [Port `BinaryJSON`](https://github.com/tikv/tikv/issues/5715)
    - [Tracing](https://github.com/tikv/tikv/issues/5714)
    - [The maximum execution time of Per-request](https://github.com/tikv/tikv/issues/5712)

- [More issues to solve for TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)
- [More issues to solve for TiKV](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

Last week, we landed [145 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-11-18..2019-11-24) in the TiDB repository, [4 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-11-18..2019-11-24) in the TiSpark repository, and [76 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-11-18..2019-11-24&type=Issues) in the TiKV and PD repositories.

### Critical PRs

TiDB:

- [Enable the push-down of 19 functions](https://github.com/pingcap/tidb/pull/13683)
- [Do not set the statement priority when `tidb_force_priority` is set](https://github.com/pingcap/tidb/pull/13633)
- [Allocate continuous `RowID` for the single `INSERT` statement](https://github.com/pingcap/tidb/pull/13648)
- [Support the SQL bindings management](https://github.com/pingcap/tidb/pull/13608)
- [Make the error message more readable when dropping the primary key](https://github.com/pingcap/tidb/pull/13582)
- [Fix the bug that the cached store cannot be updated when the store address is changed and the original address is made offline](https://github.com/pingcap/tidb/pull/13495)
- [Implement the non-block read when Coprocessor meets the lock of a large transaction](https://github.com/pingcap/tidb/pull/11986)

TiSpark:

- [Fix TiKV `DAGRequest`'s `outputOffsets`](https://github.com/pingcap/tispark/pull/1231)

TiKV and PD:

- [Update the blob file format for the ZSTD dictionary compression](https://github.com/tikv/tikv/pull/5992)
- [Replace `crc` by `crc32fast` and `crc64fast`](https://github.com/tikv/tikv/pull/5982)
- [Reduce the size of `tikv::storage::errors::Error`](https://github.com/tikv/tikv/pull/5979)
- [Update RocksDB and Titan](https://github.com/tikv/tikv/pull/5968)
- [Return `commit_ts` in the commit response](https://github.com/tikv/tikv/pull/5966)
- [Fix the maximum receivable message size for the client](https://github.com/pingcap/pd/pull/1952)
- [Delay the Replica read when applying a snapshot](https://github.com/tikv/tikv/pull/5919)
- [Add more engine abstraction that works towards `Peekable` and `Iterable` for the snapshot](https://github.com/tikv/tikv/pull/5901)
- [Add the rollback reason for `check_txn_status`](https://github.com/tikv/tikv/pull/5878)
- [Encapsulate `IOLimiter` and remove the RocksDB dependency from `sst_importer`](https://github.com/tikv/tikv/pull/5835)

## Upcoming TiDB events

[Apache Pulsar Meetup x PingCAP Infra Meetup](https://www.huodongxing.com/event/7520647658000?layout=EN)

Date: November 30th, 2019

Location: PingCAP office in Beijing
