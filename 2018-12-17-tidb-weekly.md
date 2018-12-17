---
title: Weekly update (December 10 ~ December 16, 2018)
date: 2018-12-17
summary: Last week, we landed 47 PRs in the TiDB repository, 2 PRs in the TiSpark repository, and 36 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [47 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-12-10..2018-12-16+) in the TiDB repository.

## Added

- [Propose the design for the SQL plan management](https://github.com/pingcap/tidb/pull/8651)
- [Support the `interactive_timeout` system variable](https://github.com/pingcap/tidb/pull/8573)
- [Add a batch commit session variable for large transactions](https://github.com/pingcap/tidb/pull/8293)

## Improved

- [Print the error log if the transaction state is unexpected when calling `Commit`](https://github.com/pingcap/tidb/pull/8687)
- [Raise an error or warning for unsupported isolation levels](https://github.com/pingcap/tidb/pull/8625)
- [Support `ALTER TABLE TRUNCATE PARTITION`](https://github.com/pingcap/tidb/pull/8624)
- [Support altering the character set to `utf8` or `utf8mb4`](https://github.com/pingcap/tidb/pull/8037)

## Fixed

- [Make the join reorder solver stateless](https://github.com/pingcap/tidb/pull/8680)
- [Fix the unexpected data truncation error when the plan cache is enabled](https://github.com/pingcap/tidb/pull/8656)
- [Do not build `dual` for `AntiSemiJoin` when the condition is `constant false`](https://github.com/pingcap/tidb/pull/8648)
- [Fix the wrong result when the client uses `comStmtSendLongData`](https://github.com/pingcap/tidb/pull/8645)
- [Fix the optimizer failure for generating a plan when the `TIDB_SMJ` hint is specified](https://github.com/pingcap/tidb/pull/8635)
- [Fix the wrong result caused by the `abs` function pushdown](https://github.com/pingcap/tidb/pull/8622)
- [Fix the panic when adding an index of the generated column](https://github.com/pingcap/tidb/pull/8620)
- [Preserve the precision information of timestamp columns in the plan cache](https://github.com/pingcap/tidb/pull/8619)
- [Fix data race caused by the flag of `JSON` columns](https://github.com/pingcap/tidb/pull/8564)
- [Move some session variables to the statement context for the correct retry](https://github.com/pingcap/tidb/pull/8034)

# Weekly update in TiSpark

Last week, we landed [2 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-12-10..2018-12-16+) in the TiSpark repository.

## Added

- [Support the `desc` table command](https://github.com/pingcap/tispark/pull/517)

## Fixed

- [Fix the issue that `ScanIterator` fails to read from adjacent empty Regions](https://github.com/pingcap/tispark/pull/519)

# Weekly update in TiKV and PD

Last week, we landed [36 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-12-10..2018-12-16&type=Issues) in the TiKV and PD repositories.

## Added

- [Add `rpad` and `rpad_binary` built-in functions](https://github.com/tikv/tikv/pull/3914)
- [Add `year_week_with_mode` and `year_week_without_mode` built-in functions](https://github.com/tikv/tikv/pull/3876)

## Improved

- [Change the default PD node name to `pd-{hostname}`](https://github.com/pingcap/pd/pull/1366)
- [Fix the redundant header when PD sends commands to TiKV](https://github.com/pingcap/pd/pull/1365)
- [Check and report undefined PD configuration items](https://github.com/pingcap/pd/pull/1362)

## Fixed

- [Set `retryable` instead of the `abort` error when TiKV exits](https://github.com/tikv/tikv/pull/3891)
- [Fix the issue that PD `RaftCluster` cannot be stopped](https://github.com/pingcap/pd/pull/1383)
- [Fix a bug about Region merge when the Raftstore thread is very slow](https://github.com/tikv/tikv/pull/3822)

# New contributors (Thanks!)

tikv:

- [AbnerDBFan](https://github.com/AbnerDBFan)

parser:

- [feloxx](https://github.com/feloxx)
- [haplone](https://github.com/haplone)