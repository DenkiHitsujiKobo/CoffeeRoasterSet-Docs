---
title: INoneSyncPickupEntity
parent: "Udonコンポーネント"
nav_order: 7
---

# INoneSyncPickupEntity

Pickupオブジェクトについて、VRCObjectSyncによる位置の同期とUdonSynced変数のManual同期とを両立するための抽象クラスです。  
[NoneSyncPickupProxy]と組み合わせて使われます。

## 概要

VRCObjectSyncは、UdonBehaviourの同期モードでいえばContinuousに相当する機能を持ちます。そのため、Manual同期したいUdonBehaviourとVRCObjectSyncを同じオブジェクトへ付与すると変数の同期に不都合が生じる場合があり、推奨されません。

本アセットではこの不都合を解決するため、[NoneSyncPickupProxy]が本スクリプトの関数をローカルイベントとして呼び出すことで機能の両立を図っています。

## 仕様

- 本スクリプトは抽象クラスとして定義しているため、コンポーネントとしてGameObjectへ付与することはできません。継承先のクラスをご利用ください。



[NoneSyncPickupProxy]: /docs/udon/NoneSyncPickupProxy

