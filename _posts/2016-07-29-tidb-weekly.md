---
layout: post
title: TiDB Weekly
---

Last week, we landed [27 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2016-07-23..2016-07-29%20) in the TiDB repositories.

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