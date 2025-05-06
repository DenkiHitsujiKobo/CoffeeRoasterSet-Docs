---
title: AlcoholLamp
parent: "Prefabs"
nav_order: 1
---

# AlcoholLamp

コーヒー豆の焙煎に使う、加熱用のアルコールランプです。


## 使いかた

- Pickupオブジェクトです。Useすることで点火/消火の切り替えができます。
- 点火した状態で[RoasterPickup]の下に置くと、シリンダーの中に入っている豆を加熱します。
- [RoasterBase]の下で手離すと、適切な位置にスナップします。


## 設定項目

以下のコンポーネントが設定できます。  
詳細は各コンポーネントの解説ページをご覧ください。

- AlcoholLamp: [PickupSnapHandler]
- AlcoholLamp/System: [HeatSource]



[RoasterPickup]: /docs/prefabs/RoasterSet/RoasterPickup
[RoasterBase]: /docs/prefabs/RoasterSet/RoasterBase
[PickupSnapHandler]: /docs/udon/PickupSnapHandler/
[HeatSource]: /docs/udon/HeatSource

