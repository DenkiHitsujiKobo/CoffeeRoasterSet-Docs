---
title: RoasterBase
parent: "Prefabs"
nav_order: 8
---

# RoasterBase

コーヒー豆を焙煎する手動焙煎機のスタンド部分です。  
ほかの関連Prefabと一緒に、[RoasterSet]に同梱されています。

<img src="/assets/images/prefabs/RoasterBase.png" width="50%" alt="picture of roaster stand.">


## 使いかた

- ワールドに固定で設置します。
- [RoasterPickup]を近くで手放すと、スタンドの上に乗るように位置を補正します。
- [AlcoholLamp]を近くで手放すと、スタンドの中央になるように位置を補正します。


## 設定項目

以下のコンポーネントが設定できます。  
詳細は各コンポーネントの解説ページをご覧ください。

- RoasterBase/SnapPoint_roaster: [PickupSnapPoint]
- RoasterBase/SnapPoint_lamp: [PickupSnapPoint]



[RoasterSet]: /docs/prefabs/RoasterSet
[RoasterPickup]: /docs/prefabs/RoasterPickup
[AlcoholLamp]: /docs/prefabs/AlcoholLamp
[PickupSnapPoint]: /docs/udon/PickupSnapPoint

