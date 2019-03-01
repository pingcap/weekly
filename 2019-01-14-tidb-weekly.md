---
title: Weekly update (January 07 ~ January 13, 2019)
date: 2019-01-14
summary: Last week, we landed 51 PRs in the TiDB repository, 5 PRs in the TiSpark repository, and 32 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [51 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-01-07..2019-01-13+) in the TiDB repository.

## Added

- [Add the `SHOW CREATE USER` syntax](https://github.com/pingcap/tidb/pull/8970)
- [Support the named window feature](https://github.com/pingcap/tidb/pull/8937)
- [Add support for `JSON_MERGE_PRESERVE`](https://github.com/pingcap/tidb/pull/8931)
- [Propose the design for the plugin framework](https://github.com/pingcap/tidb/pull/8802)
- [Add support for the distributed GC](https://github.com/pingcap/tidb/pull/6833)

## Improved

- [Add the `row` format for `trace`](https://github.com/pingcap/tidb/pull/9029)
- [Restrict `tidb_ddl_reorg_worker_cnt` and `tidb_ddl_reorg_batch_size` to be global](https://github.com/pingcap/tidb/pull/8941)
- [Build the hash table in parallel for radix hash join](https://github.com/pingcap/tidb/pull/8927)
- [Improve Unix socket handling](https://github.com/pingcap/tidb/pull/8836)
- [Try closing connections gracefully first in the `SIGTERM` case](https://github.com/pingcap/tidb/pull/8711)
- [Improve the compatibility with MySQL when inserting a negative value into an unsigned column](https://github.com/pingcap/tidb/pull/8544)

## Fixed

- [Fix the mistaken privilege check failure for `Update`](https://github.com/pingcap/tidb/pull/9003)
- [Fix bound overflow of the histogram](https://github.com/pingcap/tidb/pull/8984)
- [Get the global value when the system variable only has a global scope](https://github.com/pingcap/tidb/pull/8968)
- [Skip the SQL execution if the transaction is aborted](https://github.com/pingcap/tidb/pull/8942)
- [Return an error if `autoid` overflows `shard bits`](https://github.com/pingcap/tidb/pull/8936)
- [Fix the wrong result when `int` joins `decimal`](https://github.com/pingcap/tidb/pull/8930)
- [Report an error for `CAST(AS TIME)` if the precision is too big](https://github.com/pingcap/tidb/pull/8907)
- [Fix an error of canceling the `Rename Index` DDL](https://github.com/pingcap/tidb/pull/8610)
- [Fix an incorrect behavior of the `STR_TO_DATE()` function](https://github.com/pingcap/tidb/pull/8517)

# Weekly update in TiSpark

Last week, we landed [5 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-01-07..2019-01-13+) in the TiSpark repository.

## Fixed

- [Fix the possible `NullPointerException` issue when `show_row_id` is set to `true`](https://github.com/pingcap/tispark/pull/552)
- [Fix the `Set` type when inserting multiple `Set` values](https://github.com/pingcap/tispark/pull/548)

# Weekly update in TiKV and PD

Last week, we landed [32 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-01-07..2019-01-13&type=Issues) in the TiKV and PD repositories.

## Added

- [Add a new metric for delayed Raft messages](https://github.com/tikv/tikv/pull/4061)
- [Introduce the `Steady` timer](https://github.com/tikv/tikv/pull/4060)
- [Implement `Locate2Args`, `Locate3Args`, `LocateBinary2Args`, and `LocateBinary3Args` in Coprocessor](https://github.com/tikv/tikv/pull/4016)
- [Add the scheduling configuration metrics](https://github.com/pingcap/pd/pull/1406)
- [Implement `AddDurationAndString` in Coprocessor](https://github.com/tikv/tikv/pull/4010)
- [Implement the `FIELD()` function in Coprocessor](https://github.com/tikv/tikv/pull/4007)
- [Implement `run_afl` and add seeds for the fuzzer](https://github.com/tikv/tikv/pull/3999)

## Improved

- [Provide efficient codecs](https://github.com/tikv/tikv/pull/3629)
- [Use the `batch_raft` RPC and batch channel to reduce gRPC CPU usage](https://github.com/tikv/tikv/pull/3913)
- [Make `apply` scale](https://github.com/tikv/tikv/pull/4044)
- [Switch the gRPC event engine from `epollsig` to `epollex`](https://github.com/tikv/tikv/pull/4028)
- [Enable the GC worker to do GC by itself](https://github.com/tikv/tikv/pull/3179)

## Fixed

- [Fix the useless log level](https://github.com/tikv/tikv/pull/4046)
- [Fix the panic when getting overlapping Regions with version 0](https://github.com/tikv/tikv/pull/4030)
- [Fix the gRPC log redirection](https://github.com/tikv/tikv/pull/4050)

# New contributors (Thanks!)

tidb:

- [alex-lx](https://github.com/alex-lx)
- [invzhi](https://github.com/invzhi)
- [lnhote](https://github.com/lnhote)
- [nange](https://github.com/nange)
- [shinytang6](https://github.com/shinytang6)
- [snithish](https://github.com/snithish)

tikv:

- [DCjanus](https://github.com/DCjanus)
- [aylei](https://github.com/aylei)
- [gaodayue](https://github.com/gaodayue)
- manifoldQAQ

parser:

- [firekillice](https://github.com/firekillice)
- [zhaoxiaojie0415](https://github.com/zhaoxiaojie0415)

docs:

- [lastzero](https://github.com/lastzero)