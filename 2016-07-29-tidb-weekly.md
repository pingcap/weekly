---
date: 2016-07-29T00:00:00Z
title: Weekly Update
url: /2016/07/29/tidb-weekly/
---

Last week, we landed [27 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-07-23..2016-07-29%20) in the TiDB repositories and [34 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2016-07-23..2016-07-29+&type=Issues&ref=searchresults) in the TiKV repositories.

## Notable changes to `TiDB`
+ Support cost based query optimization. 
+ Set the new query optimizer as default to improve the speed of complex queries. Meanwhile, a start-up parameter is provided to switch to the old query optimizer.
+ Use Varint to encode the Column Value with integer type and Column ID, which saves storage space significantly.
+ Add a [Documents](https://github.com/pingcap/docs) repository.
+ Supprt the [Hex Function](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_hex).
+ Simplify the compling and deployment for better usability.
+ Fix several bugs.

## New Contributor
[Huaiyu Xu](https://github.com/XuHuaiyu)

## Notable changes to `TiKV`

+ Support building TiKV by linking static RocksDB automatically. You can build TiKV in one machine and copy the binary to other machines to use directly as long as the  machines have the same architecture and operation system.
+ Supprt getting snapshot asynchronously for higher throughput and better performance, see [benchmark](#Benchmark).
+ Use PipeBuf to receive data to reduce system call and memory allocation. 
+ Use Varint to encode un-comparable integers to save disk space. 
+ Use one `SendCh` to clean up duplicated code. 
+ Add [user documents](https://github.com/pingcap/docs/) on how to build and use TiKV.

## Notable changes to `Placement Driver`

+ Embed etcd to for easier deployment.
+ Add a health check for Store.
+ Add [user documents](https://github.com/pingcap/docs/) on how to build and use PD.
+ Clean up the command flags.

## Benchmark

Use [sysbench](https://github.com/pingcap/tidb-bench/tree/master/sysbench) to benchmark getting snapshot asynchronously and synchronously in 3-node TiKV.

```bash
# Prepare data
sysbench --test=./lua-tests/db/oltp.lua --mysql-host=${host} --mysql-port=${port} \
 --mysql-user=${user} --mysql-password=${password} --oltp-tables-count=1 \
 --oltp-table-size=5120000 --rand-init=on prepare

# Run benchmark
sysbench --test=./lua-tests/db/select.lua --mysql-host=${host} --mysql-port=${port} \
 --mysql-user=${user} --mysql-password=${password} --oltp-tables-count=1 \
 --oltp-table-size=5120000 --num-threads=${threads} --report-interval=60 \
 --max-requests=5120000 --percentile=99 run
```

|Threads|Async qps|Async avg/.99 latency|Sync qps|Sync avg/.99 latency|
|---|---|---|---|---|---|
|32|13347|2.4/4.61|12345|2.59/4.78|
|64|14210|4.50/7.78|11868|5.39/8.50|
128|14075|9.09/15.22|12324|10.38/16.68|

As we can see, the qps is increased by about 15%, and the latency is decreased by about 10%.


