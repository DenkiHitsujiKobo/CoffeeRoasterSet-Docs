---
title: RoasterPickup
parent: "Prefabs"
nav_order: 9
---

# RoasterPickup

コーヒー豆を焙煎する、手動焙煎機のシリンダー部分です。


## 使いかた

- Pickupオブジェクトです。UseすることでパーティクルのON/OFFを切り替えます。
- ほかの容器からパーティクルを当てられると、その中身を受け取ります。
  - 中身を受け取るときに、その種類に応じた効果音が再生されます。
  - 初期設定で受け入れるのは生の豆と焙煎豆の2種類です。
- ほかの容器オブジェクトにパーティクルを当てることで、保持している中身を渡すことができます。
- [RoasterBase]の近くで手放すと、スタンドの上に乗るように位置が補正されます。
- [AlcoholLamp]で加熱しながらハンドルを回すことでコーヒー豆の焙煎ができます。
  - ハンドルを握っている間だけ焙煎が進み、設定された時間が経つと焙煎が完了します。


## 設定項目

以下のコンポーネントが設定できます。  
詳細は各コンポーネントの解説ページをご覧ください。

- RoasterPickup/System: [HandyRoaster]
  - [ContentHandler]も参照のこと
- RoasterPickup/System/AudioHandler: [ContentSoundHandler]



[RoasterBase]: /docs/prefabs/RoasterBase
[AlcoholLamp]: /docs/prefabs/AlcoholLamp
[HandyRoaster]: /docs/udon/HandyRoaster
[ContentHandler]: /docs/udon/ContentHandler
[ContentSoundHandler]: /docs/udon/ContentSoundHandler

