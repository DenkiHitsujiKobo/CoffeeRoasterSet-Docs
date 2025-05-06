---
title: PickupSnapHandler
parent: "Udonコンポーネント"
nav_order: 9
---

# PickupSnapHandler

Pickupオブジェクトを手放したとき、その置かれた位置を補正するためのコンポーネントです。  
[PickupSnapPoint]と組み合わせて使われます。

## 概要

本コンポーネントの付与されたPickupオブジェクトが、[PickupSnapPoint]の位置へテレポートすることで位置の補正を行います。


## 設定項目

| Settings | 説明 |
| ---- | ---- |
| `Snap ID` | スナップ対象となるIDを設定します。<br>一致するIDを持った[PickupSnapPoint]にのみスナップします。[^1] |
| `Point` | インスタンス起動時からスナップ対象となる[PickupSnapPoint]を設定します。[^2] |


## 仕様詳細
- 本コンポーネントと同時に、以下のコンポーネントが必要です。
  - Collider系コンポーネント
  - VRCPickup
    - RigidBody
  - VRCObjectSync (任意)

---

[^1]: ただし`SnapID`が設定されていない[PickupSnapPoint]には、本コンポーネントの`SnapID`にかかわらずスナップします。
[^2]: Unityの仕様によりインスタンス起動時には`OnTriggerEnter`が反応せず、最初から判定に入っているものがスナップ対象とならないのを回避するためのものです。<br>最初から[PickupSnapPoint]の判定に入っていない場合には設定しないことを推奨します。



[PickupSnapPoint]: /docs/udon/PickupSnapPoint/

