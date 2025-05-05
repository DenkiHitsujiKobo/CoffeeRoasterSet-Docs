---
title: PickupSnapHandler
parent: "Udonコンポーネント"
nav_order: 9
---

# PickupSnapHandler

Pickupオブジェクトを手放したとき、その置かれた位置を補正するためのクラスです。  
[PickupSnapPoint]と組み合わせて使われます。

## 概要

本コンポーネントの付与されたPickupオブジェクトが、[PickupSnapPoint]の位置へテレポートすることで位置の補正を行います。

## 設定項目

- `SnapID`
  - 一致するIDを持った[PickupSnapPoint]にのみスナップします。
  - `SnapID`が設定されていない[PickupSnapPoint]には、本コンポーネントの`SnapID`にかかわらずスナップします。

## 仕様
- 本コンポーネントと同時に、以下のコンポーネントが必要です。
  - VRCPickup
  - Collider系コンポーネント
  - RigidBody
  - VRCObjectSync (任意)



[PickupSnapPoint]: /docs/udon/PickupSnapPoint/

