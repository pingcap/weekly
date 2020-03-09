---
title: Weekly update (February 24 ~ March 01, 2020)
date: 2020-03-01
summary: Last week, we landed 68 PRs in the TiDB repository and 58 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog post

Nick Cameron is a long-time Rust programmer who has recently started using Go. Last week, we published a post in which he talks about his early impressions of Go. Read this post to learn more:

[Early Impressions of Go from a Rust Programmer](https://pingcap.com/blog/early-impressions-of-go-from-a-rust-programmer/)

## Community

### New contributors

tidb:

* [mgkanani](https://github.com/mgkanani)
* [wangwangwar](https://github.com/wangwangwar)

tikv:

* [ZiheLiu](https://github.com/ZiheLiu)
* [govardhangdg](https://github.com/govardhangdg)
* [lsampras](https://github.com/lsampras)

docs:

* [ldnvnbl](https://github.com/ldnvnbl)

tidb-operator:

* [u5surf](https://github.com/u5surf)
* [Smana](https://github.com/Smana)

parser:

* [dasinlsb](https://github.com/dasinlsb)

chaos-mesh:

* [Gallardot](https://github.com/Gallardot)

## Call for participation

* [Issues to solve for TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)
* [Issues to solve for TiKV](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

Last week, we landed [68 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2020-02-24..2020-03-01+) in the TiDB repository and [58 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2020-02-24..2020-03-01&type=Issues) in the TiKV and PD repositories.

### Critical PRs

TiDB:

* [Add more metrics table for the diagnosis report](https://github.com/pingcap/tidb/pull/14964)
* [Support changing more configuration items online](https://github.com/pingcap/tidb/pull/14952)
* [Show the `CAST` type in the `EXPLAIN` statement](https://github.com/pingcap/tidb/pull/14942)
* [Fold the constant in the projection elimination and Top-N push-down](https://github.com/pingcap/tidb/pull/14927)
* [Consider collations when comparing strings](https://github.com/pingcap/tidb/pull/14913)
* [Support index encoding or decoding for the new collation](https://github.com/pingcap/tidb/pull/14876)
* [Disable pushing down the `Duration` or JSON-related function to TiFlash](https://github.com/pingcap/tidb/pull/14861)
* [Support the `SELECT INTO ... OUTFILE` syntax](https://github.com/pingcap/tidb/pull/14848)
* [Implement the sequence allocator](https://github.com/pingcap/tidb/pull/14829)
* [Enable the inline projection for Hash Join](https://github.com/pingcap/tidb/pull/14783)
* [Improve the projection to keep the order or keep the index in some cases](https://github.com/pingcap/tidb/pull/14510)

TiKV and PD:

* [Avoid handling requests for multiple times](https://github.com/tikv/tikv/pull/6677)
* [Let the collated `GROUP BY` column return the original data](https://github.com/tikv/tikv/pull/6716)
* [Return values when acquiring pessimistic locks successfully](https://github.com/tikv/tikv/pull/6696)
* [Fix the panic caused by not destroying `apply fsm` in some cases](https://github.com/tikv/tikv/pull/6692)
* [Wake up the hibernated leader after the failed read index](https://github.com/tikv/tikv/pull/6648)
* [Wake up the Raft leader for more cases](https://github.com/tikv/tikv/pull/6672)
* [Wake up the Raft leader on the proposal](https://github.com/tikv/tikv/pull/6736)
* [Introduce the solution-based balance solver](https://github.com/pingcap/pd/pull/2141)

## Upcoming TiDB event

[TiDB Usability Challenge Program](https://pingcap.com/community/tidb-usability-challenge/)
