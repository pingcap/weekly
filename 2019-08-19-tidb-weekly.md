---
title: Weekly update (August 12 ~ August 18, 2019)
date: 2019-08-19
summary: Last week, we landed 41 PRs in the TiDB repository, 24 PRs in the TiSpark repository, and 31 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [41 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-08-12..2019-08-18+) in the TiDB repository.

## Added

- [Introduce `columnBufferAllocator` for the vectorized evaluation](https://github.com/pingcap/tidb/pull/11743)
- [Add the reserve methods to `Column` for the var-length types](https://github.com/pingcap/tidb/pull/11699)
- [Make `baseBuiltinFunc` support the conversion from row-based evaluation to vectorized evaluation](https://github.com/pingcap/tidb/pull/11630)
- [Add the support of follower read to TiDB](https://github.com/pingcap/tidb/pull/11347)

## Improved

- [Add the `Times` interface for `chunk.Column`](https://github.com/pingcap/tidb/pull/11742)
- [Add the new `rowcodec` library](https://github.com/pingcap/tidb/pull/7597)

## Fixed

- [Increase the default concurrency factor of cost computing](https://github.com/pingcap/tidb/pull/11752)
- [Rewrite `in` as `eq` when the `rhs` list has only one item](https://github.com/pingcap/tidb/pull/11749)
- [Fix the incorrect behavior of index join](https://github.com/pingcap/tidb/pull/11724)
- [Change the `select ... for update` statement to the normal `select ...` statement in the auto-commit case](https://github.com/pingcap/tidb/pull/11715)
- [Fix the automatic retry when a transaction has the `select for update` statement](https://github.com/pingcap/tidb/pull/11714)
- [Fix the panic when fetching date from the `processlist` table in some cases](https://github.com/pingcap/tidb/pull/11688)

# Weekly update in TiSpark

Last week, we landed [24 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-08-12..2019-08-18+) in the TiSpark repository and released TiSpark [2.1.3](https://github.com/pingcap/tispark/releases/tag/v2.1.3).

## Fixed

- [Prohibit the `Aggregation` or `GroupBy` pushdown in the case of double read](https://github.com/pingcap/tispark/pull/1004)
- [Fix the error of Spark version reflection for the HDP release](https://github.com/pingcap/tispark/pull/1017)

# Weekly update in TiKV and PD

Last week, we landed [31 PRs](https://github.com/search?p=1&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-08-12..2019-08-18&type=Issues) in the TiKV and PD repositories.

## Added

- [Support the validating parameters in `rpn_expr/test_util.rs`](https://github.com/tikv/tikv/pull/5282)
- [Set the `not_found` field to `true` in `Getresponse` when a key does not exist](https://github.com/tikv/tikv/pull/5240)
- [Exclude the shared block cache from the core dump](https://github.com/tikv/tikv/pull/5227)

## Improved

- [Refine `Res`s and handle all `Res`s via `EvalContext`](https://github.com/tikv/tikv/pull/5255)
- [Replace `std`'s HashMap to `tikv_util`'s HashMap](https://github.com/tikv/tikv/pull/5252)
- [Migrate `json_unquote` to the RPN function](https://github.com/tikv/tikv/pull/5226)

## Fixed

- [Fix the deadlock problem in Raft clusters](https://github.com/pingcap/pd/pull/1678)
- [Fix the duplicate `ctx` in the `Readindex` request](https://github.com/tikv/tikv/pull/5213)
- [Fix the bugs of `float_str_to_int_str` and refactor the implementation to the same as TiDB](https://github.com/tikv/tikv/pull/5134)

# New contributors (Thanks!)

tidb：

- [francis0407](https://github.com/francis0407)
- [lance6716](https://github.com/lance6716)

tikv：

- ethan-daocloud
- [you06](https://github.com/you06)
- [wujy-cs](https://github.com/wujy-cs)

parser:

- [lauhg](https://github.com/lauhg)
- [doggeral](https://github.com/doggeral)
- [tangwz](https://github.com/tangwz)
- [ichn-hu](https://github.com/ichn-hu)
- [qiukun](https://github.com/qiukun)
- [huaouo](https://github.com/huaouo)
