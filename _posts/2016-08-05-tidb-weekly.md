---
layout: post
title: TiDB Weekly
---

Last week, we landed [28 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-07-30..2016-08-05%20) in the TiDB repositories.

## Notable changes to `TiDB`

+ Add support for constant folding in the SQL optimizer.
+ Optimize the query speed of the secondary index. In certain scenarios, only the data in the index needs to be read.
+ Use dynamic programing to decide the join path for multiple tables.
+ Adjust the command line to support setting the listening address.
+ Prometheus metrics and golang pprof share the same port.
+ Update the  [Documents](https://github.com/pingcap/docs) repository.
+ Fix several bugs.
