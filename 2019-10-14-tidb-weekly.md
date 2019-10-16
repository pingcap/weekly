---
title: Weekly update (September 30 ~ October 13, 2019)
date: 2019-10-14
summary: Last two weeks, we landed 131 PRs in the TiDB repository, 4 PRs in the TiSpark repository, and 46 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiSpark', 'TiKV', 'PD']
---

# TiDB Weekly

## Community

### New contributors

tidb:

* [big747386](https://github.com/big747386)
* [liuhao2050](https://github.com/liuhao2050)
* [xiaoronglv](https://github.com/xiaoronglv)
* [gtygo](https://github.com/gtygo)
* [shldreams](https://github.com/shldreams)

tikv:

* [hk1997](https://github.com/hk1997)
* [ming-relax](https://github.com/ming-relax)
* [pentium3](https://github.com/pentium3)

docs-cn:

* [llussy](https://github.com/llussy)
* [qiukun](https://github.com/qiukun)

tidb-operator:

* [nyurik](https://github.com/nyurik)

## Call for participation

TiDB:

* [Issues to solve](https://github.com/pingcap/tidb/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)

TiKV:

* [Issues to solve](https://github.com/tikv/tikv/labels/S%3A%20HelpWanted)

## Updates of the week

### Progress

TiDB:

Last week, we landed [131 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-09-30..2019-10-13+) in the TiDB repository, and [48 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-09-30..2019-10-13+in%3Atitle%3Avectorized+evaluation) on the [Vectorized Expressions](https://github.com/pingcap/tidb/issues/12058) issue.

TiSpark:

Last week, we landed [4 PRs](https://github.com/pingcap/tispark/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2019-09-30..2019-10-13+) in the TiSpark repository.

TiKV and PD:

Last week, we landed [46 PRs](https://github.com/search?q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2019-09-30..2019-10-13&type=Issues) in the TiKV and PD repositories.

### Critical PRs

TiDB:

* [Fix the panic when checking the `NULL` rejection for `from_unixtime`](https://github.com/pingcap/tidb/pull/12413)
* [Fix incorrect `OriginDefaultValue` in `ColumnInfo`](https://github.com/pingcap/tidb/pull/12168)
* [Calculate the GC `safePoint` based on the global `MinStart` timestamp](https://github.com/pingcap/tidb/pull/12223)
* [Replace the cost model factor constants with the system variable](https://github.com/pingcap/tidb/pull/12367)
* [Do not return the first row until the frame is completed](https://github.com/pingcap/tidb/pull/12480)

TiSpark:

* [Forbid adding the TiDB password to `SparkConf`](https://github.com/pingcap/tispark/pull/1139)

TiKV and PD:

* [Fix a resource leak bug about `mpsc::batch`](https://github.com/tikv/tikv/pull/5566)
* [Introduce the `engine_rocks` component](https://github.com/tikv/tikv/pull/5541)

## Upcoming TiDB events

* [TiDB Hackathon 2019 (in Chinese)](http://nc9hsk15y2xczuor.mikecrm.com/PiwBPaL)
* [Infra Meetup No.115: Infra Meetup X Kubernetes & Cloud Native Meetup (in Chinese)](https://pingcap.com/meetup/)
* [Infra Meetup No.116 Chengdu (in Chinese)](https://pingcap.com/meetup/)
* [Infra Meetup No.117 Shanghai (in Chinese)](https://pingcap.com/meetup/)
