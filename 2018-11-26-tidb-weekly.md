---
title: Weekly update (November 19 ~ November 25, 2018)
date: 2018-11-26
summary: Last week, we landed 46 PRs in the TiDB repository, 2 PRs in the TiSpark repository, and 20 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [46 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-11-19..2018-11-25+) in the TiDB repository.

## Added

- [Add the http API to get database and table information](https://github.com/pingcap/tidb/pull/8256)
- [Propose the table partition design](https://github.com/pingcap/tidb/pull/7969)
- [Support creating hash partitioned tables](https://github.com/pingcap/tidb/pull/8026)

## Improved

- [Add missing columns for `information_schema.files`](https://github.com/pingcap/tidb/pull/8387)
- [Impose user authentication for unix socket connections](https://github.com/pingcap/tidb/pull/8381)
- [Redesign the `trace` statement with JSON output](https://github.com/pingcap/tidb/pull/8357)
- [Support JSON as the return type for the `case` expression](https://github.com/pingcap/tidb/pull/8355)
- [Preallocate the columns array in `MutRow` to avoid array resizing](https://github.com/pingcap/tidb/pull/8348)
- [Support subqueries in the `Do` statement](https://github.com/pingcap/tidb/pull/8343)
- [Add the memory guard to prevent OOM caused by the plan cache](https://github.com/pingcap/tidb/pull/8339)
- [Clean up the plan cache entry in the `Deallocate` statement](https://github.com/pingcap/tidb/pull/8332)
- [Support `ADMIN CHECK TABLE`/`ADMIN CHECK INDEX` using specified `tidb_snapshot`](https://github.com/pingcap/tidb/pull/8172)

## Fixed

- [Fix incorrect privilege check for the `UPDATE` statement](https://github.com/pingcap/tidb/pull/8376)
- [Fix the bootstrap error when the SQL mode is set to `ANSI`](https://github.com/pingcap/tidb/pull/8353)
- [Make sure goroutines of HashJoin exit before its `Close` returns](https://github.com/pingcap/tidb/pull/8338)
- [Remove partition IDs for partition tables in `DROP DATABASE`](https://github.com/pingcap/tidb/pull/8319)
- [Fix the panic caused by EOF when Coprocessor is in the streaming mode](https://github.com/pingcap/tidb/pull/8297)

# Weekly update in TiSpark

Last week, we landed [2 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-11-19..2018-11-25+) in the TiSpark repository.

## Added

- [Support raw partition Read](https://github.com/pingcap/tispark/pull/495)

# Weekly update in TiKV and PD

Last week, we landed [20 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-11-19..2018-11-25&type=Issues) in the TiKV and PD repositories.

## Added

- [Support interactive Region scan in pd-ctl](https://github.com/pingcap/pd/pull/1320)
- [Add the history index to `sync` when `stream` is established](https://github.com/pingcap/pd/pull/1305)
- [Add normal index scan benchmarks](https://github.com/tikv/tikv/pull/3814)

## Improved

- [Improve Region key print](https://github.com/pingcap/pd/pull/1335)
- [Move unrelated benchmarks into individual directories](https://github.com/tikv/tikv/pull/3809)
- [Check the `conf` version for `split`](https://github.com/tikv/tikv/pull/3807)

## Fixed

- [Fix a deadlock in `GetOpInfluence`](https://github.com/pingcap/pd/pull/1340)
- [Fix the issue that configurations cannot be set to zero values](https://github.com/pingcap/pd/pull/1334)
- [Fix `go mod tidy` in PD](https://github.com/pingcap/pd/pull/1330)

# New contributor (Thanks!)

docs-cn: [bugwz](https://github.com/bugwz)