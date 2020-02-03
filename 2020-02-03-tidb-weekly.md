---
title: Weekly update (January 20 ~ February 02, 2020)
date: 2020-02-03
summary: Last two weeks, we landed 25 PRs in the TiDB repository and 7 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## News & blog post

One of the fundamental tradeoffs of programming language design is run-time performance vs. compile-time performance. The Rust team nearly always (if not always) chose run-time over compile-time.

Last week, we published a post that discusses the following topics as the first episode in a series of posts:

- The spectre of poor Rust compile times at PingCAP
- The TiKV compile-time adventure so far
- Rust's designs for poor compilation time
    - Bootstrapping Rust
    - (Un)virtuous cycles
    - Early decisions that favored run-time over compile-time
- Recent work on Rust compile times

The full post is here:

[The Rust Compilation Model Calamity](https://pingcap.com/blog/rust-compilation-model-calamity/)

## Community

### New contributors

tidb:

- [ldnvnbl](https://github.com/ldnvnbl)
- [ZiheLiu](https://github.com/ZiheLiu)

tikv:

- [silathdiir](https://github.com/silathdiir)

parser:

- [rubb1sh](https://github.com/rubb1sh)

## Call for participation

- [More issues to solve for TiDB](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)
- [More issues to solve for TiKV](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

Last two weeks, we landed [25 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2020-01-20..2020-02-02+) in the TiDB repository and [7 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2020-01-20..2020-02-02&type=Issues) in the TiKV and PD repositories.

### Critical PRs

TiDB:

- [Use the 8-byte `MysqlTime` format](https://github.com/pingcap/tidb/pull/14278)
- [Handle events of adding or truncating partitions](https://github.com/pingcap/tidb/pull/14500)
- [Fix the bug that the table's existence is not checked when granting privileges on this table to users](https://github.com/pingcap/tidb/pull/14540)
- [Enhance the rule of partition pruning](https://github.com/pingcap/tidb/pull/14544)
- [Fix the issue that the `RowKVClient` scan method cannot correctly break the loop](https://github.com/pingcap/tidb/pull/14365)

TiKV and PD:

- [Ensure that the peer with pending reads does not become hibernate](https://github.com/tikv/tikv/pull/6438)
- [Support using S3 as the external storage](https://github.com/tikv/tikv/pull/6209)
- [Enable the default protocol feature flag](https://github.com/tikv/tikv/pull/6436)
- [Switch the `Chunk` time to use the new 8-byte format](https://github.com/tikv/tikv/pull/6418)
