---
title: Weekly update (August 26 ~ September 01, 2019)
date: 2019-09-02
summary: Last week, we landed 59 PRs in the TiDB repository, 12 PRs in the TiSpark repository, and 40 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [59 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-08-26..2019-09-01+) in the TiDB repository.

## Added

- [Make the projection executor support the vectorized expression evaluation](https://github.com/pingcap/tidb/pull/11917)
- [Support using query blocks in the optimizer hint](https://github.com/pingcap/tidb/pull/11861)

## Improved

- [Refine the usage of the expression blacklist](https://github.com/pingcap/tidb/pull/11940)
- [Eliminate the top level `Sort` in subqueries](https://github.com/pingcap/tidb/pull/11935)
- [Support pushing down predicates for window functions](https://github.com/pingcap/tidb/pull/11915)
- [Allow inserting `default` into the generated columns](https://github.com/pingcap/tidb/pull/11901)
- [Improve the length and decimal size when a base type adds/minuses/multiplies a decimal](https://github.com/pingcap/tidb/pull/11873)
- [Decrease the memory usage of `hashTable` in `HashJoinExec`](https://github.com/pingcap/tidb/pull/11832)
- [Replace `memdb` with a more efficient memory version](https://github.com/pingcap/tidb/pull/11807)

## Fixed

- [Fix the failure to add a unique index on the partitioned table (by `RANGE COLUMNS`)](https://github.com/pingcap/tidb/pull/11946)
- [Fix an over-quoted bug in the `BinaryJSON.Unquote` function](https://github.com/pingcap/tidb/pull/11934)
- [Limit the number of `TopN` items](https://github.com/pingcap/tidb/pull/11906)
- [Fix the start timestamp in the slow log when a transaction is retried](https://github.com/pingcap/tidb/pull/11851)
- [Set the correct `stmtCtx` for the `EXPLAIN` statement](https://github.com/pingcap/tidb/pull/11186)

# Weekly update in TiSpark

Last week, we landed [12 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-08-26..2019-09-01+) in the TiSpark repository and released TiSpark [2.1.4](https://github.com/pingcap/tispark/releases/tag/v2.1.4).

## Improved

- [Remove useless dependencies](https://github.com/pingcap/tispark/pull/1075)

# Weekly update in TiKV and PD

Last week, we landed [40 PRs](https://github.com/search?q=repo:tikv/tikv+repo:pingcap/pd+is:pr+is:merged+merged:2019-08-26..2019-09-01&type=Issues) in the TiKV and PD repositories.

## Added

- [Add an API to get the store ID and the cluster ID](https://github.com/tikv/tikv/pull/5257)
- [Add an API to clear the tombstone store](https://github.com/pingcap/pd/pull/1705)

## Improved

- [Improve parsing of URLs without HTTP prefixes](https://github.com/pingcap/pd/pull/1703)
- [Improve the GC of Raft logs by a dedicated thread](https://github.com/pingcap/pd/pull/1703)

## Fixed

- [Fix the panic during the Region Merge](https://github.com/tikv/tikv/pull/5354)
- [Fix the panic when starting TiKV](https://github.com/tikv/tikv/pull/5350)
- [Fix building a Docker image](https://github.com/tikv/tikv/pull/5337)
- [Fix a deadlock in the `Scatter` Region](https://github.com/pingcap/pd/pull/1706)
- [Fix the silent `ReadIndex` response](https://github.com/tikv/tikv/pull/5316)

# New contributors (Thanks!)

tidb:

- [newer027](https://github.com/newer027)

parser:

- [zuoRambo](https://github.com/zuoRambo)
- [yunnian](https://github.com/yunnian)
