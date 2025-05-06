---
title: NoneSyncPickupProxy
parent: "Udonコンポーネント"
nav_order: 8
---

# NoneSyncPickupProxy

Pickupオブジェクトについて、VRCObjectSyncによる位置の同期とUdonSynced変数のManual同期とを両立するためのコンポーネントです。  
[INoneSyncPickupEntity]の派生クラスを登録して使います。

## 概要
VRCObjectSyncは、UdonBehaviourの同期モードでいえばContinuousに相当する機能を持ちます。そのため、Manual同期したいUdonBehaviourとVRCObjectSyncを同じオブジェクトへ付与すると変数の同期に不都合が生じる場合があり、推奨されません。

本アセットではこの不都合を解決するため、本コンポーネントが[INoneSyncPickupEntity]の関数をローカルイベントとして呼び出すことで機能の両立を図っています。

## 設定項目

- `Entity`
  - イベントを呼び出したい[INoneSyncPickupEntity]派生クラスを登録します。
    - 通常、本コンポーネントが付与されたPickupオブジェクトの子オブジェクトとして配置されています。

## 仕様
- 本コンポーネントと同時に、以下のコンポーネントが必要です。
  - VRCPickup
    - RigidBody
- 以下のPickupオブジェクト関連イベントに反応します。
  - `OnPickup()`: Pickupオブジェクトを持ったとき
  - `OnDrop()`: Pickupオブジェクトを手放したとき
  - `OnPickupUseDown()`: Pickupオブジェクトを持って、トリガーを引いたとき
  - `OnPickupUseUp()`: Pickupオブジェクトを持って、トリガーを離したとき



[INoneSyncPickupEntity]: /docs/udon/INoneSyncPickupEntity

