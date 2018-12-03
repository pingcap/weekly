---
title: Weekly update (November 26 ~ December 02, 2018)
date: 2018-12-03
summary: Last week, we landed 72 PRs in the TiDB repository, 2 PRs in the TiSpark repository, and 25 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [72 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-11-26..2018-12-02+) in the TiDB repository.

## Added

- [Visualize the `trace` output using the HTTP interface](https://github.com/pingcap/tidb/pull/8430)
- [Add the `tidb_parse_tso` built-in function](https://github.com/pingcap/tidb/pull/8385)
- [Add the `json_depth` built-in function](https://github.com/pingcap/tidb/pull/8347)
- [Close the client connection when the server waiting time exceeds `wait_timeout`](https://github.com/pingcap/tidb/pull/8346)
- [Add a constraint propagation framework to be used by partition pruning](https://github.com/pingcap/tidb/pull/7643)

## Improved

- [Release the datum memory after the transaction is finished](https://github.com/pingcap/tidb/pull/8458)
- [Simplify the session level `domain` pool](https://github.com/pingcap/tidb/pull/8456)
- [Record the current database information in the `CRUCIAL OPERATION` log](https://github.com/pingcap/tidb/pull/8447)
- [Kill all connections when the server is not gracefully shut down](https://github.com/pingcap/tidb/pull/8446)
- [Support `PREPARE FROM @var_name`](https://github.com/pingcap/tidb/pull/8437)
- [Implement `GoString()` for `TxnState` to make the generated log more user-friendly](https://github.com/pingcap/tidb/pull/8434)
- [Improve the privilege check for `set password`](https://github.com/pingcap/tidb/pull/8426)
- [Return scanned rows of Coprocessor operators in `EXPLAIN ANALYZE`](https://github.com/pingcap/tidb/pull/8423)
- [Improve the privilege check for `use DB`](https://github.com/pingcap/tidb/pull/8418)
- [Improve the MySQL compatibility of `SHOW` commands](https://github.com/pingcap/tidb/pull/8417)
- [Do not push down filters containing `SetVar` or `GetVar`](https://github.com/pingcap/tidb/pull/8412)
- [Add a limit to constrain the maximum number of prepared statements](https://github.com/pingcap/tidb/pull/8405)
- [Prevent `Order By table_name.column_name` for the `Union` statement](https://github.com/pingcap/tidb/pull/8389)
- [Make `round` work when converting a float string to an integer string](https://github.com/pingcap/tidb/pull/8279)
- [Add the correctness check for the `validate_password_*` system variables](https://github.com/pingcap/tidb/pull/8227)

## Fixed

- [Fix a bug of wrong duplicate results in left outer join](https://github.com/pingcap/tidb/pull/8505)
- [Set a default value for the `Enum` type correctly when inserting rows](https://github.com/pingcap/tidb/pull/8469)
- [Fix an error message when the updated value overflows](https://github.com/pingcap/tidb/pull/8457)
- [Fix a panic when dumping statistics for a dropped column](https://github.com/pingcap/tidb/pull/8448)
- [Fix wrong result length of `Union`](https://github.com/pingcap/tidb/pull/8442)
- [Prohibit the DML execution when TiDB loses connection to `etcd`](https://github.com/pingcap/tidb/pull/8441)
- [Fix data race caused by concurrent access to `do.infoHandle`](https://github.com/pingcap/tidb/pull/8287)
- [Fix a server hang issue when canceling the `Add Index` DDL job](https://github.com/pingcap/tidb/pull/8171)

# Weekly update in TiSpark

Last week, we landed [2 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-11-26..2018-12-02+) in the TiSpark repository.

## Fixed

- [Fix `NullPointException` when counting empty tables](https://github.com/pingcap/tispark/pull/498)

# Weekly update in TiKV and PD

Last week, we landed [25 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-11-26..2018-12-02&type=Issues) in the TiKV and PD repositories.

## Added

- [Add support for adding the learner operator to PD](https://github.com/pingcap/pd/pull/1302)
- [Add the `week_with_mode` built-in function](https://github.com/tikv/tikv/pull/3857)
- [Add the `space` built-in function](https://github.com/tikv/tikv/pull/3841)
- [Add the `SubstringBinary2Args` and `SubstringBinary3Args` built-in functions](https://github.com/tikv/tikv/pull/3813)
- [Support modifying TiKV's maximum background jobs](https://github.com/tikv/tikv/pull/3810)
- [2.1 cherry pick: Support ambiguous time](https://github.com/tikv/tikv/pull/3854)

## Improved

- [Collect component logs](https://github.com/tikv/tikv/pull/3859)
- [Improve tombstone command's error message](https://github.com/tikv/tikv/pull/3850)
- Improve tests: 

    - [Move the tests directory](https://github.com/tikv/tikv/pull/3839) 
    - [Fix `test_follower_slow_split`](https://github.com/tikv/tikv/pull/3797) 
    - [Add more `seek` and `seek_for_prev` tests](https://github.com/tikv/tikv/pull/3722) 
    - [Provide the seeded KV generator](https://github.com/tikv/tikv/pull/3853)

- Improve PD documentation:
    
    - [Update the API document](https://github.com/pingcap/pd/pull/1346)
    - [Update the API HTML file](https://github.com/pingcap/pd/pull/1345)

- [Abandon the PD vendor directory](https://github.com/pingcap/pd/pull/1337)

## Fixed

- [Fix the TiKV redundant raftstore heartbeat](https://github.com/tikv/tikv/pull/3864)
- [Fix the issue of watching leader with invalid revision in PD](https://github.com/pingcap/pd/pull/1347)
- [Fix small bugs of tikv-ctl](https://github.com/tikv/tikv/pull/3840)
- [2.1 cherry pick: Fix tikv-ctl help messages](https://github.com/tikv/tikv/pull/3846)

# New contributors (Thanks!)

docs:

- [lucperkins](https://github.com/lucperkins)

tidb:

- [alapha23](https://github.com/alapha23)
- [exialin](https://github.com/exialin)
- [leoppro](https://github.com/leoppro)
- [pingyu](https://github.com/pingyu)


