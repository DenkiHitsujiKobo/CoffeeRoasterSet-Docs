---
title: PickupSnapPoint
parent: "Udonコンポーネント"
nav_order: 10
---

# PickupSnapPoint

Pickupオブジェクトを手放したとき、その置かれた位置を補正するためのコンポーネントです。  
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
- [PickupSnapHandler]がCollider判定に入るとテレポート先を知らせます。
  - その状態でPickupオブジェクトが手放されると、テレポート先へ移動します。


## 設定項目

| Settings | 説明 |
| ---- | ---- |
| Snap ID | スナップ対象となるIDを設定します。<br>一致するIDを持った[PickupSnapHandler]のみがスナップできます。<br>ただし`SnapID`が設定されていない場合には、全ての[PickupSnapHandler]がスナップします。 |


## 仕様詳細

- [PickupSnapHandler]のテレポート先は、本コンポーネントが付与されているGameObjectのTransformと同じ位置です。設置する場所にはご注意ください。



[PickupSnapHandler]: /docs/udon/PickupSnapHandler/

