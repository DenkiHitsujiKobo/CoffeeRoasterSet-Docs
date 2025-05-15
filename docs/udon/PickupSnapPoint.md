---
title: PickupSnapPoint
parent: "Udonコンポーネント"
nav_order: 10
---

# PickupSnapPoint

Pickupオブジェクトを手放したとき、その置かれた位置を補正 (スナップ) するためのコンポーネントです。  
[PickupSnapHandler]と連携して使います。

```mermaid
flowchart LR
    accTitle: class relationship
    accDescr: PickupSnapPoint inherits UdonSharpBehaviour, and depends to PickupSnapHandler.

    point("<u>**PickupSnapPoint**</u>")
    behaviour("UdonSharpBehaviour")
    snap(["PickupSnapHandler"])

    behaviour -->|継承| point
    point <-.->|依存| snap
```

### 関連コンポーネント

- [PickupSnapHandler]

---

## 機能について

- 本コンポーネントと同時に以下のコンポーネントが必要です。
  - Collider系コンポーネント(`Is Trigger`オン)
- [PickupSnapHandler]がCollider判定に入ると、後述の設定に応じてスナップ先を知らせます。
  - オブジェクトがCollider判定を抜けると、スナップ先から外れます。


## 設定項目

| Settings | 説明 |
| ---- | ---- |
| Snap ID | スナップ対象となるIDを設定します。<br>一致するIDを持った[PickupSnapHandler]のみがスナップできます。[^1] |


## 仕様詳細

- [PickupSnapHandler]によるスナップは、本コンポーネントが付与されているGameObjectと同じ位置・角度へテレポートする形で行われます。本コンポーネントの設置場所にはご注意ください。
- テレポート先の通知は`OnTriggerEnter/Exit`イベントによって行われます。

---

[^1]: ただし`SnapID`が設定されていない場合は、その設定に関わらず全ての[PickupSnapHandler]がスナップできます。



[PickupSnapHandler]: /docs/udon/PickupSnapHandler/

