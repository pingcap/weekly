---
title: Weekly update (August 13 ~ August 21, 2016)
date: 2016-08-22
summary: Last week, we landed 26 PRs in the TiDB repositories and 15 PRs in the TiKV repositories.
tags: ['TiDB', 'TiKV', 'Placement Driver']
---

# Weekly update (August 13 ~ August 21, 2016)

Last week, we landed [26 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-08-13..2016-08-21%20) in the TiDB repositories and [15 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2016-08-15..2016-08-21&type=Issues&ref=searchresults) in the TiKV repositories.

## Notable changes to `TiDB`

+ Upgrade the [query optimizer](https://github.com/pingcap/tidb/pull/1609).
+ Upgrade the [lexer](https://github.com/pingcap/tidb/pull/1566).
+ Replace golang protobuf with [gogo protobuf](https://github.com/pingcap/tidb/pull/1610).
+ Optimize the [distributed executor](https://github.com/pingcap/tidb/pull/1599).
+ Repair the [Time](https://github.com/pingcap/tidb/pull/1592) and [Decimal](https://github.com/pingcap/tidb/pull/1598) types to improve the compatibility with MySQL.
+ Support the [Set names binary](https://github.com/pingcap/tidb/pull/1578) statement.
+ Support [Covering Index](https://github.com/pingcap/tidb/pull/1567).
+ Optimize the table scanning when the condition is [false constant](https://github.com/pingcap/tidb/pull/1589).
+ Fix several bugs.

## Notable changes to `TiKV`

+ Add the [leader lease read](https://github.com/pingcap/tikv/pull/916) support for better performance, see [benchmark](#Benchmark).
+ Use [`delete_file_in_range`](https://github.com/pingcap/tikv/pull/918) from RocksDB to destroy Regions quickly to avoid blocking Raft storage threads.
+ Support [GC](https://github.com/pingcap/tikv/pull/930) for obsolete data versions.
+ Coprocessor supports [covering index](https://github.com/pingcap/tikv/pull/929) for `Select Where` and the aggregation operations. 
+ Check whether the key is [already rolled back](https://github.com/pingcap/tikv/pull/941) when `prewrite` to fix a transaction [bug](https://github.com/pingcap/tikv/pull/921). 
+ Support the [`--log-file`](https://github.com/pingcap/tikv/pull/936) flag to redirect log to the log file.

## Notable changes to `Placement Driver`

+ Refine the [join](https://github.com/pingcap/pd/pull/249) flag to support multiple `join` scenarios. 
+ Use [unix socket](https://github.com/pingcap/pd/pull/266) in test to avoid the "Address Already in Use" error. 
+ [Redirect requests](https://github.com/pingcap/pd/pull/273) to the Leader if the current member is a Follower.

## Benchmark

Use [sysbench](https://github.com/pingcap/tidb-bench/tree/master/sysbench) to benchmark [leader lease read](https://github.com/pingcap/tikv/pull/916) and previous Raft quorum read in 3-node TiKV.

### Insert

```bash
# Prepare data
sysbench --test=./lua-tests/db/oltp.lua --mysql-host=${host} --mysql-port=${port} \
 --mysql-user=${user} --mysql-password=${password} --oltp-tables-count=$1 \
 --oltp-table-size=5120000 --rand-init=on prepare

# Run benchmark
sysbench --test=./lua-tests/db/insert.lua --mysql-host=${host} --mysql-port=${port} \
 --mysql-user=${user} --mysql-password=${password} --oltp-tables-count=1 \
 --oltp-table-size= 5120000 --num-threads=${threads} --report-interval=60 \
 --max-requests=1280000 --percentile=99 run
```

|Threads|Leader lease read qps|Leader lease read avg/.99 latency|Raft quorum read qps|Raft quorum read/.99 latency|
|---|---|---|---|---|---|
|32|2296|13.93/15.28|1315|24.33/94|
|64|2199|29.1/145|1325|48.29/473|
|128|1854|69/931|1290|99/697|

As we can see, the qps is increased by about 70%, and the latency is decreased by about 40%.

### Select

```bash
# Prepare data
sysbench --test=./lua-tests/db/oltp.lua --mysql-host=${host} --mysql-port=${port} \
 --mysql-user=${user} --mysql-password=${password} --oltp-tables-count=1 \
 --oltp-table-size=5120000 --rand-init=on prepare

# Run benchmark
sysbench --test=./lua-tests/db/select.lua --mysql-host=${host} --mysql-port=${port} \
 --mysql-user=${user} --mysql-password=${password} --oltp-tables-count=1 \
 --oltp-table-size=5120000 --num-threads=${threads} --report-interval=60 \
 --max-requests=1280000 --percentile=99 run
```

|Threads|Leader lease read qps|Leader lease read avg/.99 latency|Raft quorum read qps|Raft quorum read/.99 latency|
|---|---|---|---|---|---|
|32|21010|1.52/7.53|12221|2.62/6.69|
|64|25948|2.47/10.20|12637|5.06/11.62|
|128|27283|4.69/13.68|11069|11.56/35.88|

As we can see, the qps is increased by about 130%, and the latency is decreased by about 50%.

## New contributors

+ [hhkbp2](https://github.com/hhkbp2)
