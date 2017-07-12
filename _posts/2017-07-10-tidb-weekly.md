---
layout: post
title: Weekly Update
---
## Weekly update in TiDB
2017-07-10

Last week, we landed [45 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-07-03..2017-07-09%20) in the TiDB repositories.

## Added
* [Introduce a `Selectivity` interface in the statistics module.](https://github.com/pingcap/tidb/pull/3161)
* [Support dropping statistics with the `Drop Stats TableName` statement.](https://github.com/pingcap/tidb/pull/3615)
* [Support showing statistics with the `Show Stats_meta [where clause]` statement.](https://github.com/pingcap/tidb/pull/3633)
* [Support the `NO_AUTO_VALUE_ON_ZERO` SQL mode.](https://github.com/pingcap/tidb/pull/3661)

## Fixed
* [Fix a bug in converting date to MySQL timestamp.](https://github.com/pingcap/tidb/pull/3587)
* [Change the instance name for Prometheus metrics to `host:port`,](https://github.com/pingcap/tidb/pull/3588) in case multiple instances are deployed on a single machine.
* [Consider timezone in the `now()` function.](https://github.com/pingcap/tidb/pull/3590)
* [Disable the `skip_constraint_check` option.](https://github.com/pingcap/tidb/pull/3602)
* [Fix a bug in updating multiple tables.](https://github.com/pingcap/tidb/pull/3605)
* [Add a `NoDefaultValueFlag` flag in the `AlterTable` statement.](https://github.com/pingcap/tidb/pull/3634)


## Improved
* Refactor optimizer:
  - [Consider multiple children in `getPushedProp`.](https://github.com/pingcap/tidb/pull/3589)
* Refactor the builtin function evaluation framework:
  - [Simplify the type inference work for builtin functions.](https://github.com/pingcap/tidb/pull/3617)
  - [cast](https://github.com/pingcap/tidb/pull/3629)
  - [strcmp](https://github.com/pingcap/tidb/pull/3559)
  - [json_object, json_array](https://github.com/pingcap/tidb/pull/3562)
  - [password](https://github.com/pingcap/tidb/pull/3593)
  - [cos](https://github.com/pingcap/tidb/pull/3607)
  - [sin](https://github.com/pingcap/tidb/pull/3609)
  - [tan](https://github.com/pingcap/tidb/pull/3621)
  - [degree](https://github.com/pingcap/tidb/pull/3642)
  - [ord](https://github.com/pingcap/tidb/pull/3671)
* Refactor [`tikv.NewMockTikvStore`](https://github.com/pingcap/tidb/pull/3573) and [`statistics.Table`](https://github.com/pingcap/tidb/pull/3586) to make code cleaner.]
* [Simplify the implementation of `IPv4Mapped` and `IPv4Compat`.](https://github.com/pingcap/tidb/pull/3596)
* [Set length and decimal for constant values.](https://github.com/pingcap/tidb/pull/3608)

## Weekly update in TiKV

Last week, We landed [30 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-07-02..2017-07-08&type=Issues) in the TiKV repositories.

## Added

* Add the [aggregation](https://github.com/pingcap/tikv/pull/1959) executor for coprocessor.
* Add the [status](https://github.com/pingcap/pd/pull/664) API for PD.
* Allow skipping [bcast commit](https://github.com/pingcap/tikv/pull/1976).
* Add [Raft log entry cache](https://github.com/pingcap/tikv/pull/1984).
* Enable [buffer hint](https://github.com/pingcap/tikv/pull/1989) to speed up sending Raft messages.
* Add [`json_type`](https://github.com/pingcap/tikv/pull/1992), [`json_merge`](https://github.com/pingcap/tikv/pull/1994), [`json_unquote`](https://github.com/pingcap/tikv/pull/1995), [`json_extract`](https://github.com/pingcap/tikv/pull/1997) evaluator for coprocessor. 
* Add printing [region size](https://github.com/pingcap/tikv/pull/2002) for `tikv-ctl`.

## Fixed

* Fix [wrong error messages](https://github.com/pingcap/pd/pull/668) when PD recovers.
* Fix [wrong definition](https://github.com/pingcap/tikv/pull/1979) for signal handler.
* [Report store information](https://github.com/pingcap/tikv/pull/1986) before starting a Raft store thread.
* Avoid [removing leader](https://github.com/pingcap/pd/pull/671) peer directly.
* Fix a wrong [split record](https://github.com/pingcap/pd/pull/670) in history operations.
* [Allocate peer ID](https://github.com/pingcap/pd/pull/673) only when finding a better replacement. 
* Fix [`test_peer_resove`](https://github.com/pingcap/tikv/pull/2010) failed test.

## Improved

* Register the propose callbacks [in batches](https://github.com/pingcap/tikv/pull/1972).
* [Push](https://github.com/pingcap/pd/pull/669) schedule commands to TiKV directly to speed up balancing.
* [Refactor the coprocessor](https://github.com/pingcap/tikv/pull/2005) code directory.