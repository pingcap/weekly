---
title: Weekly update (December 17 ~ December 23, 2018)
date: 2018-12-24
summary: Last week, we landed 48 PRs in the TiDB repository and 29 PRs in the TiKV and PD repositories.
tags: ['TiDB', 'TiKV', 'PD']
---

# Weekly update in TiDB

Last week, we landed [48 PRs](https://github.com/pingcap/tidb/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+merged%3A2018-12-17..2018-12-23) in the TiDB repository.

## Added

- [Add the `CFB` mode for the `AES` encryption](https://github.com/pingcap/tidb/pull/8760)
- [Implement the basic `CreateView` feature](https://github.com/pingcap/tidb/pull/8571)
- [Add the HTTP API to query hot tables/indexes](https://github.com/pingcap/tidb/pull/7890)

## Improved

- [Make `Admin Check Table` only check the public index](https://github.com/pingcap/tidb/pull/8748)
- [Handle non-BMP characters in the UTF-8 charset](https://github.com/pingcap/tidb/pull/8738)
- [Specify the sort order for the columns in the `physical` property](https://github.com/pingcap/tidb/pull/8715)
- [Refactor error handling of transactions](https://github.com/pingcap/tidb/pull/8712)
- [Close all connections directly when terminating TiDB](https://github.com/pingcap/tidb/pull/8692)
- [Ignore the unknown hint and return a warning](https://github.com/pingcap/tidb/pull/8685)
- [Support specifying the ending of a range to be scanned](https://github.com/pingcap/tidb/pull/8602)
- [Add the extra information message to be sent to the MySQL client](https://github.com/pingcap/tidb/pull/8285)

## Fixed

- [Fix the wrong output of `Show Master Status`](https://github.com/pingcap/tidb/pull/8737)
- [Fix the incorrect result related to the `Duration` columns](https://github.com/pingcap/tidb/pull/8725)
- [Fix the compatibility problem of renaming tables](https://github.com/pingcap/tidb/pull/8709)
- [Correct the column name with the unary plus sign](https://github.com/pingcap/tidb/pull/8702)
- [Handle corner cases for `auto_increment` columns](https://github.com/pingcap/tidb/pull/8181)

# Weekly update in TiKV and PD

Last week, we landed [29 PRs](https://github.com/search?utf8=%E2%9C%93&q=repo%3Atikv%2Ftikv+repo%3Apingcap%2Fpd+is%3Apr+is%3Amerged+merged%3A2018-12-17..2018-12-23&type=Issues) in the TiKV and PD repositories.

## Added

- [Add `lpad` and `lpad_binary` built-in functions](https://github.com/tikv/tikv/pull/3943)
- [Add `add_datetime_and_duration`, `add_datetime_and_string` and `add_time_datetime_null` built-in functions](https://github.com/tikv/tikv/pull/3899)
- [Add an HTTP port for Prometheus](https://github.com/tikv/tikv/pull/3855)
- [Introduce the Raftstore router](https://github.com/tikv/tikv/pull/3916)

## Improved

- [Check overlapped Regions for the new Region](https://github.com/pingcap/pd/pull/1377)
- [Remove the disturbing log when the store is `tombstone`](https://github.com/pingcap/pd/pull/1382)

## Fixed

- [Fix the possible panic issue caused by `Approximate Size Split`](https://github.com/tikv/tikv/pull/3942)
- [Fix a bug about Region merge in the case of multiple snapshots](https://github.com/tikv/tikv/pull/3873)

# New contributors (Thanks!)

tidb-operator:

- [queenliuxx](https://github.com/queenliuxx)

tidb:

- [cuining](https://github.com/cuining)
- [kjzz](https://github.com/kjzz)

parser:

- [TennyZhuang](https://github.com/TennyZhuang)
- [caohe](https://github.com/caohe)
- [exialin](https://github.com/exialin)
- [hanchuanchuan](https://github.com/hanchuanchuan)
- [honestold3](https://github.com/honestold3)
- [kangkaisen](https://github.com/kangkaisen)
- [knarfeh](https://github.com/knarfeh)
- [tony612](https://github.com/tony612)