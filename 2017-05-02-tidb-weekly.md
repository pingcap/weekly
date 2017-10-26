---
date: 2017-05-02T00:00:00Z
title: Weekly Update
---

## Weekly update in TiDB

# 2017-05-02

Last week, we landed [49 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20merged%3A2017-04-24..2017-04-30%20) in the TiDB repositories.

## Added

* Add builtin function [`truncate`](https://github.com/pingcap/tidb/pull/3077), [`makedate`](https://github.com/pingcap/tidb/pull/3102), [`utc_time`](https://github.com/pingcap/tidb/pull/3145)

* [Add pre-commit hook.](https://github.com/pingcap/tidb/pull/3112)

* [Add a plan for `Analyze`.](https://github.com/pingcap/tidb/pull/3130)

* [Add a check list about the things that contributors should think about before sending a PR.](https://github.com/pingcap/tidb/pull/3137)

* [Support `ENGINE` option with partition option in table definition.](https://github.com/pingcap/tidb/pull/3140)

* [Add code review guide.](https://github.com/pingcap/tidb/pull/3166)


## Fixed

* [Fix bug in converting string to hex/bit.](https://github.com/pingcap/tidb/pull/3115)

* [Fix a few panic when infering type for some functions without argument.](https://github.com/pingcap/tidb/pull/3137)

* [Fix a data race in Join operator.](https://github.com/pingcap/tidb/pull/3159)

## Improved

* [Add `countReliable` attribute in physicalPlanInfo:](https://github.com/pingcap/tidb/pull/3011) In CBO phrase, when row count is estimated by real statistics or limit clause, the cost is reliable.

* Refactor TypeInferer: [Add a few interfaces for evaluate expression](https://github.com/pingcap/tidb/pull/3094), [Refine `EvalBool`](https://github.com/pingcap/tidb/pull/3139), 

* Refactor planner: [Union](https://github.com/pingcap/tidb/pull/3085), [Hash Aggregate](https://github.com/pingcap/tidb/pull/3093), [Union Scan](https://github.com/pingcap/tidb/pull/3098), [Join](https://github.com/pingcap/tidb/pull/3126), [`Apply`](https://github.com/pingcap/tidb/pull/3152), [Refine code](https://github.com/pingcap/tidb/pull/3173)

* Refactor executor: [Table Scan](https://github.com/pingcap/tidb/pull/3133)

* [Improve contribute guide.](https://github.com/pingcap/tidb/pull/3102)

* Make `goword` happy in the following package: [ddl](https://github.com/pingcap/tidb/pull/3119), [util](https://github.com/pingcap/tidb/pull/3121), [tablecodec](https://github.com/pingcap/tidb/pull/3122), [expression](https://github.com/pingcap/tidb/pull/3123), [bootstrap](https://github.com/pingcap/tidb/pull/3182), [model](https://github.com/pingcap/tidb/pull/3183), [table](https://github.com/pingcap/tidb/pull/3184), [ast](https://github.com/pingcap/tidb/pull/3185), [perfschema](https://github.com/pingcap/tidb/pull/3186)

* [Add a few empty memory tables in `information_schema`:](https://github.com/pingcap/tidb/pull/3127) Make `DTS` happy.

* [When where expresion can be converted to `false`, use dual table instead of a read table.](https://github.com/pingcap/tidb/pull/3144)

## New Contributors

**Thank you guys!**

* [lkk2003rty](https://github.com/lkk2003rty)

* [Ce Gao](https://github.com/gaocegege)

* [Zejun Li](https://github.com/bobotu)

# Weekly update in TiKV

# 2017-05-02

Last week, We landed [16 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Apingcap%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2017-04-23..2017-04-29&type=Issues) in the TiKV repositories.

## Added

* Let the [right split region](https://github.com/pingcap/tikv/pull/1747) derive the parent region information.

* Add a [hot region](https://github.com/pingcap/pd/pull/611) scheduler. 

* Introduce [structure log](https://github.com/pingcap/pd/pull/612) and support [JSON](https://github.com/pingcap/pd/pull/626) format. 

* Use [`--data-dir`](https://github.com/pingcap/tikv/pull/1803) instead of `--store` for TiKV storage path.

## Fixed

* Support [idempotent bootstrap](https://github.com/pingcap/tikv/pull/1774) for TiKV.

* Detect [snapshot](https://github.com/pingcap/tikv/pull/1793) in all nodes. 

* Use [non-system port](https://github.com/pingcap/pd/pull/630) to avoid test failed.

## Improved

* [Throttle big query](https://github.com/pingcap/tikv/pull/1778) to reduce the influence on the point query.  

* Add test for [applying entries](https://github.com/pingcap/tikv/pull/1783). 

* Use a [better mechanism](https://github.com/pingcap/tikv/pull/1792) when re-connecting PD. 

* Ignore unnecessary message [size computing](https://github.com/pingcap/tikv/pull/1799).
