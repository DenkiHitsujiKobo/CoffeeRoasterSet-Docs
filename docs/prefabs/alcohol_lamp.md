---
title: AlcoholLamp
parent: "Prefabs"
nav_order: 1
---

# AlcoholLamp

コーヒー豆の焙煎に使う、加熱用のアルコールランプです。

## 使いかた

- Pickupオブジェクトです。Useすることで点火・消火の切り替えができます。
- 点火した状態でRoasterPickupの下に置くと、中に入っている豆を加熱します。
- RoasterBaseの下で手離すと、適切な位置にスナップします。

## 設定項目

- [PickupSnapHandler]
  - `SnapID`: 一致しないIDを持つPickupSnapPointには位置スナップしません。

詳細は各Udonコンポーネントの解説を参照ください。


[PickupSnapHandler]: /docs/udon/PickupSnapHandler/

