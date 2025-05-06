---
title: PickupSnapPoint
parent: "Udonコンポーネント"
nav_order: 10
---

# PickupSnapPoint

Pickupオブジェクトを手放したとき、その置かれた位置を補正するためのコンポーネントです。  
[PickupSnapHandler]と組み合わせて使われます。

## 概要

[PickupSnapHandler]の付与されたPickupオブジェクトが、本コンポーネントの位置へテレポートすることで位置の補正を行います。

例えば本コンポーネントを収納棚の要所に設定することで、おおよその位置でオブジェクトを手放してもきれいに整列させる、といった使いかたが可能です。

## 設定項目

| Settings | 説明 |
| ---- | ---- |
| `Snap ID` | スナップ対象となるIDを設定します。<br>一致するIDを持った[PickupSnapHandler]のみがスナップできます。<br>ただし`SnapID`が設定されていない場合には、全ての[PickupShapHandler]がスナップします。 |

## 仕様詳細

- 本コンポーネントと同時に以下のコンポーネントが必要です。
  - Collider系コンポーネント(Trigger設定オン)
- [PickupSnapHandler]がCollider判定に入ると、`OnTriggerEnter`イベントが働くことでテレポート先を通知します。
- [PickupSnapHandler]のテレポート先は、本コンポーネントが付与されているGameObjectのTransformと同じ位置です。設置する場所にはご注意ください。



[PickupSnapHandler]: /docs/udon/PickupSnapHandler/

