---
layout: post
title: Weekly Update
---
## Weekly update in TiDB

# 2017-05-08

Last week, we landed [28 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-05-08..2017-05-14%20) in the TiDB repositories.

## Added

* Add builtin function [`umcompress` and `uncompressdlength`](https://github.com/pingcap/tidb/pull/3136), [`convert_tz`](https://github.com/pingcap/tidb/pull/3222), [`period-diff`](https://github.com/pingcap/tidb/pull/3237)

* [Fill data into `information_schema.key_column_usage`.](https://github.com/pingcap/tidb/pull/2721)

* [Add `Open` interface for Executor.](https://github.com/pingcap/tidb/pull/3221)

* [Show warnings for `Load Data` statement.](https://github.com/pingcap/tidb/pull/3224)

* [Support `Json` type and functions in parser.](https://github.com/pingcap/tidb/pull/3228)

* [Support `top-n` operator in new planner.](https://github.com/pingcap/tidb/pull/3242)

## Fixed

* [Consider session variable `time_zone` for timestamp datum.](https://github.com/pingcap/tidb/pull/3167)

* [Fix data race problem in IndexLookup Executor.](https://github.com/pingcap/tidb/pull/3212)

* [Fix a bug in HashJoin Executor encoding/decoding.](https://github.com/pingcap/tidb/pull/3225)

* [Return right value for `@@version`.](https://github.com/pingcap/tidb/pull/3238)

## Improved

* [Refator range calculation related code.](https://github.com/pingcap/tidb/pull/3208)

* Refactor expression evaluation framework: [Add self attribute in builtin function.](https://github.com/pingcap/tidb/pull/3218)[Return panic when calling wrong function on baseXBuiltinFunc.](https://github.com/pingcap/tidb/pull/3247)

# Weekly update in TiKV

# 2017-05-15

Last week, We landed [17 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-05-07..2017-05-13&type=Issues) in the TiKV repositories.

## Added

* Use [`clap`](https://github.com/pingcap/tikv/pull/1806) to parse command line options.

*  Show store [down](https://github.com/pingcap/pd/pull/633) state in `pd-ctl`.

* Show [operator history](https://github.com/pingcap/pd/pull/637) in `pd-ctl`.

* Show [cluster ID](https://github.com/pingcap/pd/pull/640) in `pd-ctl`.

* Introduce [`SmallGroupFirstQueue`](https://github.com/pingcap/tikv/pull/1822) to speedup point get later. 

* Use [zstd](https://github.com/pingcap/tikv/pull/1831) compression type. 

* Add [process metrics](https://github.com/pingcap/tikv/pull/1830) in Prometheus.

## Fixed

* Fix dial wrong [listening address](https://github.com/pingcap/pd/pull/642) bug. 

* Remove the ￼[offline peer￼](https://github.com/pingcap/pd/pull/639) directly.

* Mark peer as `pending_remove` to avoid following operations.

## Improved

* Add cluster ID mismatched [reason](https://github.com/pingcap/tikv/pull/1825) in error log.

* Add [log](https://github.com/pingcap/tikv/pull/1823) for apply delegate register and deregister.