---
title: Weekly update (December 24 ~ December 30, 2018)
date: 2019-01-02
summary: Last week, we landed 57 PRs in the TiDB repository, 9 PRs in the TiSpark repository, and 34 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [57 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-12-24..2018-12-30+) in the TiDB repository.

## Added

- [Add `SHOW FULL TABLES` to display the `View` status](https://github.com/pingcap/tidb/pull/8860)
- [Provide virtual table facilities](https://github.com/pingcap/tidb/pull/8657)

## Improved

- [Generate the logical property for `Group` of the `Cascades` planner](https://github.com/pingcap/tidb/pull/8833)
- [Improve the label of the `QueryDurationHistogram` metric](https://github.com/pingcap/tidb/pull/8819)
- [Improve the compatibility with the old MySQL handshake protocol](https://github.com/pingcap/tidb/pull/8812)
- [Support building `DataS` from `View`](https://github.com/pingcap/tidb/pull/8757)
- [Remove the timezone information of records in `mysql.tidb`](https://github.com/pingcap/tidb/pull/8745)
- [Improve selectivity estimation for the correlated column](https://github.com/pingcap/tidb/pull/8734)
- [Refine transaction commit slow logs](https://github.com/pingcap/tidb/pull/8731)
- [Check the `null` flag when eliminating the `count` aggregation](https://github.com/pingcap/tidb/pull/8664)
- [Add support for recursive virtual columns](https://github.com/pingcap/tidb/pull/8659)
- [Use single `delRange` and `sessionPool` in DDL](https://github.com/pingcap/tidb/pull/8522)
- [Check the privilege of the `ANALYZE TABLE` statement](https://github.com/pingcap/tidb/pull/8486)
- [Adjust the worker number of `Add Index` dynamically](https://internal.pingcap.net/confluence/pages/viewpage.action?pageId=21273537)

## Fixed

- [Avoid the overlapped range for the prefix index](https://github.com/pingcap/tidb/pull/8878)
- [Validate the value for the `time_zone` global system variable](https://github.com/pingcap/tidb/pull/8876)
- [Fix the panic when generating the index join for partitioned tables](https://github.com/pingcap/tidb/pull/8831)
- [Avoid goroutine leak for hash aggregation](https://github.com/pingcap/tidb/pull/8810)
- [Fix the failure when executing `delete...from...join...` with binlog enabled](https://github.com/pingcap/tidb/pull/8805)
- [Fix the problem of adding partitions concurrently](https://github.com/pingcap/tidb/pull/8783)
- [Fix the parser panic caused by hint in the subquery](https://github.com/pingcap/tidb/pull/8781)
- [Return `null` when casting non-binary data to the huge binary type](https://github.com/pingcap/tidb/pull/8768)
- [Fix the bug of canceling `Drop Column`](https://github.com/pingcap/tidb/pull/8545)
- [Fix the bug of canceling `Drop Table`/`Database`](https://github.com/pingcap/tidb/pull/8537)

# Weekly update in TiSpark

Last week, we landed [9 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-12-24..2018-12-30+) in the TiSpark repository.

## Added

- [Add `set` and `enum` type support](https://github.com/pingcap/tispark/pull/528)
- [Add `time` type support](https://github.com/pingcap/tispark/pull/532)
- [Add `year` type support](https://github.com/pingcap/tispark/pull/537)

# Weekly update in TiKV and PD

Last week, we landed [34 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-12-24..2018-12-30&type=Issues) in the TiKV and PD repositories.

## Added

- [Introduce a new storage engine: `Titan`](https://github.com/tikv/tikv/pull/3985)
- [Introduce the batch system](https://github.com/tikv/tikv/pull/3972)
- [Add `left_binary` and `right_binary` built-in functions](https://github.com/tikv/tikv/pull/3982)
- [Add the `add to_days` built-in function](https://github.com/tikv/tikv/pull/3978)
- [Add the `date_diff` built-in function](https://github.com/tikv/tikv/pull/3937)
- [Use `Observer`s to collect Region information to a collection](https://github.com/tikv/tikv/pull/3627)
- [Implement the `Seek` Region on `RegionInfoAccessor`](https://github.com/tikv/tikv/pull/3682)

## Improved

- [Perform a full synchronization of a new member](https://github.com/pingcap/pd/pull/1349)

# New contributors (Thanks!)

tikv:

- [Fullstop000](https://github.com/Fullstop000)
- [GinYM](https://github.com/GinYM)
- [edwardpku](https://github.com/edwardpku)

parser:

- [SwanSpouse](https://github.com/SwanSpouse)
- [liutang123](https://github.com/liutang123)
- [o-oops](https://github.com/o-oops)
- [wangbo](https://github.com/wangbo)

docs-cn:

- [httpcheck](https://github.com/httpcheck)