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

- `SnapID`
  - IDが設定されている場合、一致するIDを持った[PickupSnapHandler]だけがスナップします。
  - IDが設定されていない場合、すべての[PickupSnapHandler]がスナップします。

## 仕様
- 本コンポーネントと同時に、Trigger設定されたCollider系コンポーネントが必要です。
  - [PickupSnapHandler]が判定に入ると、`OnTriggerEnter`イベントが働いてテレポート先を通知します。
- [PickupSnapHandler]のテレポート先は、本コンポーネントが付与されているGameObjectのTransformと同じ位置です。設置する場所にはご注意ください。


[PickupSnapHandler]: /docs/udon/PickupSnapHandler/

