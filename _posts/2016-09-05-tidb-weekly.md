---
layout: post
title: Weekly Update
---

Last week, we landed [29 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-08-29..2016-09-04%20) in the TiDB repositories and [24 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2016-08-29..2016-09-04&type=Issues&ref=searchresults) in the TiKV repositories.

## Notable changes to `TiDB`

+ Support the [unhex](https://github.com/pingcap/tidb/pull/1675) and the [ceiling/ceil](https://github.com/pingcap/tidb/pull/1666) functions
+ Improve the Parser to handle `\r\n`.
+ Solve the potential [concurrency issues](https://github.com/pingcap/tidb/pull/1669)
+ Support [Load Data](https://github.com/pingcap/tidb/pull/1634)
+ Use the [Pipeline model](https://github.com/pingcap/tidb/pull/1622) to filter data through indexes to improve the performance
+ Improve the code to [reduce memory allocation](https://github.com/pingcap/tidb/pull/1663) and improve the performance
+ Fix several bugs.

## Notable changes to `TiKV`

+ Coprocessor supports the [new decimal](https://github.com/pingcap/tikv/pull/977) type.
+ Use the [Raft column family](https://github.com/pingcap/tikv/pull/990) to save Raft meta and logs. See [Benchmark](#Benchmark). 
+ [Tune the write column family](https://github.com/pingcap/tikv/pull/998) to reduce memory usage.

## Notable changes to `Placement Driver`

+ [Check duplicated](https://github.com/pingcap/pd/pull/297) store addresses to prevent user from bootstrapping cluster in the wrong way, see issues [287](https://github.com/pingcap/pd/issues/287), [288](https://github.com/pingcap/pd/issues/288).
+ Support the [remove store](https://github.com/pingcap/pd/pull/298) API to remove a dead TiKV store. 
+ Use [glide](https://github.com/Masterminds/glide) instead of the original [godep](https://github.com/tools/godep) to manage [vendor](https://github.com/pingcap/pd/pull/299).
+ Remove [`join itself`](https://github.com/pingcap/pd/pull/307) to prevent user from starting a removed PD server again.

## Benchmark

Use [sysbench](https://github.com/pingcap/tidb-bench/tree/master/sysbench) to benchmark using the (CF\_RAFT) column family to save the Raft log and previously the default (CF\_DEFAULT) column family in 3-node TiKV.

```bash
# Prepare data
sysbench --test=./lua-tests/db/oltp.lua --mysql-host=${host} --mysql-port=${port} \
 --mysql-user=${user} --mysql-password=${password} --oltp-tables-count=1 \
 --oltp-table-size=${table_size} --rand-init=on prepare

# Run benchmark
sysbench --test=./lua-tests/db/insert.lua --mysql-host=${host} --mysql-port=${port} \
 --mysql-user=${user} --mysql-password=${password} --oltp-tables-count=1 \
 --oltp-table-size=${table_size} --num-threads=${threads} --report-interval=60 \
 --max-requests=1280000 --percentile=99 run
```

|Threads|Table Size|CF_DEFAULT qps|CF_DEFAULT avg/.99 latency|CF_RAFT qps|CF_RAFT avg/.99 latency|
|---|---|---|---|---|---|
|32|6400000|3885|8.24/13.48|3979|8.04/13.70|
|64|7680000|3653|17.52/34.10|4477|14.29/24.49|
128|8960000|3422|37.39/70.10|4642|27.57/57.45|

As we can see, the qps is increased by about 22%, and the latency is decreased by about 18%.

## New contributors

+ [Dagang Wei](https://github.com/weidagang)
