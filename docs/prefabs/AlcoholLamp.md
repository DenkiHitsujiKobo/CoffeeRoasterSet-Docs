---
title: AlcoholLamp
parent: "Prefabs"
nav_order: 1
---

# AlcoholLamp

コーヒー豆の焙煎に使う加熱用のアルコールランプです。  
ほかの関連Prefabと一緒に、[RoasterSet]に同梱されています。

<img src="{{site.baseurl}}/assets/images/prefabs/AlcoholLamp.png" width="30%" alt="picture of alcohol lamp.">


## 使いかた

- Pickupオブジェクトです。
- Useすることでランプが点火します。
  - 再度Useすることで点火/消火を切り替えます。
- 点火した状態で[RoasterPickup]の下に置くと、シリンダーの中に入っている生の豆を加熱します。
- [RoasterBase]の下で手離すと、適切な位置に補正されます。


## 設定項目

以下のコンポーネントが設定できます。  
詳細は各コンポーネントの解説ページをご覧ください。

- AlcoholLamp: [PickupSnapHandler]
- AlcoholLamp/System: [HeatSource]



[RoasterSet]: /docs/prefabs/RoasterSet
[RoasterPickup]: /docs/prefabs/RoasterPickup
[RoasterBase]: /docs/prefabs/RoasterBase
[PickupSnapHandler]: /docs/udon/PickupSnapHandler/
[HeatSource]: /docs/udon/HeatSource

