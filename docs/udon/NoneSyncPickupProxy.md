---
title: NoneSyncPickupProxy
parent: "Udonコンポーネント"
nav_order: 8
---

# NoneSyncPickupProxy

Pickupオブジェクトにおいて、「VRCObjectSyncによる位置の同期」と「UdonSynced変数のManual同期」とを両立するためのコンポーネントです。  
[INoneSyncPickupEntity]の派生クラスを紐づけて使います。

```mermaid
flowchart LR
    accTitle: class relationship
    accDescr: NoneSyncPickupProxy inherits UdonSharpBehaviour.

    proxy("<u>**NoneSyncPickupProxy**</u>")
    behaviour("UdonSharpBehaviour")
    entity(["INoneSyncPickupEntity"])
    
    behaviour -->|継承| proxy
    proxy <-.->|依存| entity
```

### 関連コンポーネント

- [INoneSyncPickupEntity]

---

## 概要

VRCObjectSyncは、UdonBehaviourの同期モードでContinuousに相当する機能を持ちます。  
そのため、Manual同期したいUdonBehaviourとVRCObjectSyncを同じオブジェクトへ付与すると変数の同期に不都合が生じる場合があり、推奨されません。

本アセットではこれを解決するため、「Pickupイベントの呼び出し」と「変数の同期を含むメイン機能」とを別スクリプトに分割することで機能の両立を図っています。  
NoneSyncPickupProxyはイベントの呼び出し機能を実装するコンポーネントです。


## 機能について

- 本コンポーネントと同時に以下のコンポーネントが必要です。
  - VRCPickup
    - RigidBody
- 以下のPickupオブジェクト関連イベントに反応して、対応する[INoneSyncPickupEntity]の関数をローカルで呼び出します。
  - `OnPickup()`: Pickupオブジェクトを持ったとき
  - `OnDrop()`: Pickupオブジェクトを手放したとき
  - `OnPickupUseDown()`: Pickupオブジェクトを持って、トリガーを引いたとき
  - `OnPickupUseUp()`: Pickupオブジェクトを持って、トリガーを離したとき
  

## 設定項目

| Components | 説明 |
| ---- | ---- |
| Entity | イベントを呼び出したい[INoneSyncPickupEntity]派生コンポーネントを紐づけます。 |



[INoneSyncPickupEntity]: {{site.baseurl}}/docs/udon/INoneSyncPickupEntity

