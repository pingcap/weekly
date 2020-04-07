---
title: Weekly update (March 30 ~ April 05, 2020)
date: 2020-04-07
summary: Last week, we landed 179 PRs in the TiDB repository and 38 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD']
---

# TiDB Weekly

## Community

### New contributors

tidb:

* [qian9qian10](https://github.com/qian9qian10)
* [krzysztofpioro](https://github.com/krzysztofpioro)
* [longfangsong](https://github.com/longfangsong)

pd:

* [hsqlu](https://github.com/hsqlu)

docs-cn:

* [mmyj](https://github.com/mmyj)

tidb-operator:

* [hsqlu](https://github.com/hsqlu)

chaos-mesh:

* [silentred](https://github.com/silentred)

## Call for participation

### TiDB

* [To distinguish TiKV and TiFlash in the TiKV client metrics](https://github.com/pingcap/tidb/issues/16107)
* [To fix the issue that the expression calculation might lose precision in the special order](https://github.com/pingcap/tidb/issues/15884)
* [To fix the mocktikv panic](https://github.com/pingcap/tidb/issues/15662)
* [All help-wanted issues in TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aopen+is%3Aissue+label%3Ahelp-wanted)

### TiKV

* [To fix the empty log after `welcome`](https://github.com/tikv/tikv/issues/7327)
* [All help-wanted issues in TiKV](https://github.com/tikv/tikv/issues?q=is%3Aopen+is%3Aissue+label%3Astatus%2Fhelp-wanted)

## Updates of the week

### Progress

Last week, we landed [179 PRs](https://github.com/pingcap/tidb/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-03-30..2020-04-05+) in the TiDB repository and [38 PRs](https://github.com/tikv/tikv/pulls?q=is%3Apr+is%3Amerged+merged%3A2020-03-30..2020-04-05+) in the TiKV and PD repositories.

#### TiDB

* [Fix the partition selection on the Hash partitioned table](https://github.com/pingcap/tidb/pull/16070)
* [Implement the exclusive lock for the temporary storage directory per TiDB instance](https://github.com/pingcap/tidb/pull/15203)
* [Fix the charset and collation for `current_role`](https://github.com/pingcap/tidb/pull/16019)
* [Fix the wrong outer join elimination when the join key is empty](https://github.com/pingcap/tidb/pull/15894)
* [Fix the issue that if the aggregation function is `avg(distinct)` or `sum(distinct)` when `tidb_opt_distinct_agg_push_down` is set to `1`, the planner needs to inject a projection to cast the `cop` data from the integer type to the decimal type](https://github.com/pingcap/tidb/pull/15997)
* [Fix the issue that the query with `NATURAL LEFT JOIN` unexpectedly results in an error](https://github.com/pingcap/tidb/pull/15913)
* [Fix the repetitive selectivity accounting and stabilize the result](https://github.com/pingcap/tidb/pull/15536)
* [Add `(ddl.DDL).Create{Table,Schema}WithInfo`](https://github.com/pingcap/tidb/pull/15806)
* [Fix the privilege check for the sequence function usage](https://github.com/pingcap/tidb/pull/15838)
* [Fix an unexpected error when altering a table's default collation](https://github.com/pingcap/tidb/pull/15876)
* [Use the revertible sandbox to buffer mutations](https://github.com/pingcap/tidb/pull/15931)
* [Fix the panic of `merge join` for tables with redundant indexes](https://github.com/pingcap/tidb/pull/15840)
* [Fix the wrong result of `Not`/`IsTrue`/`IsFalse` functions](https://github.com/pingcap/tidb/pull/10498)

#### TiUP

TiUP v0.4.4 is released.

#### TiDB Change Data Capture (CDC)

* [Combine the session of captures, manager, and processors](https://github.com/pingcap/ticdc/pull/358)
* [Support the Region Merge feature](https://github.com/pingcap/ticdc/pull/385)
* [Improve the sorter performance and avoid performance regressions caused by data backlogs](https://github.com/pingcap/ticdc/pull/412)

#### TiKV

* [Support the AWS KMS backend](https://github.com/tikv/tikv/pull/7173)
* [Fix the coredump when TLS is enabled](https://github.com/tikv/tikv/pull/7251)
* [Release Bump v3.1.0-rc](https://github.com/tikv/tikv/pull/7352)
* [Add the `min_commit_ts` field to pessimistic locks](https://github.com/tikv/tikv/pull/7291)
* [Update `raft-rs` to use the aggressive flow control](https://github.com/tikv/tikv/pull/7285)
* [Add the vectorized `last_day`](https://github.com/tikv/tikv/pull/7086)

#### PD

* [Add the state switch](https://github.com/pingcap/pd/pull/2313)
* [Add the `swagger` support](https://github.com/pingcap/pd/pull/2276)
* [Add the replication mode and synchronize the status with TiKV](https://github.com/pingcap/pd/pull/2283)
* Add Placement Rules commands [#2293](https://github.com/pingcap/pd/pull/2293) [#2306](https://github.com/pingcap/pd/pull/2306)
* [Add the auto-completion for pd-ctl](https://github.com/pingcap/pd/pull/2299)

## On-going TiDB event

[TiDB Usability Challenge Program](https://pingcap.com/community/tidb-usability-challenge/)
