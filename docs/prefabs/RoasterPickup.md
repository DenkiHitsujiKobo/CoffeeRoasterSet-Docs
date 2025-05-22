---
title: RoasterPickup
parent: "Prefabs"
nav_order: 9
---

# RoasterPickup

コーヒー豆を焙煎する手動焙煎機のシリンダー部分です。  
ほかの関連Prefabと一緒に、[RoasterSet]に同梱されています。

<img src="{{site.baseurl}}/assets/images/prefabs/RoasterPickup.png" width="50%" alt="picture of roaster cylinder.">


## 使いかた

- Pickupオブジェクトです。
- 中身が入っているときにUseすると、中身がパーティクルとして出てきます。
  - 再度UseすることでパーティクルのON/OFFを切り替えます。
  - 中身が入っていない場合、パーティクルは出せません。
- ほかの容器にパーティクルを当てることで、保持している中身を渡すことができます。
- ほかの容器からパーティクルを当てられると、その中身を受け取ります。
  - 初期設定で受け取れるのは、生の豆と焙煎豆の2種類です。
  - 中身を受け取るときに、その種類に応じた効果音が再生されます。
- [RoasterBase]の近くで手放すと、スタンドの上に乗るように位置が補正されます。
- [AlcoholLamp]で加熱しながらハンドルを回すことでコーヒー豆の焙煎ができます。
  - 生の豆が加熱されている間は、シリンダーの両脇から湯気が出ます。
  - ハンドルをピックアップしている間だけ焙煎が進み、設定された時間が経つと焙煎が完了します。


## 設定項目

以下のコンポーネントが設定できます。  
詳細は各コンポーネントの解説ページをご覧ください。

- RoasterPickup/System: [HandyRoaster]
  - [ContentHandler]も参照のこと
- RoasterPickup/System/AudioHandler: [ContentSoundHandler]



[RoasterSet]: /docs/prefabs/RoasterSet
[RoasterBase]: /docs/prefabs/RoasterBase
[AlcoholLamp]: /docs/prefabs/AlcoholLamp
[HandyRoaster]: /docs/udon/HandyRoaster
[ContentHandler]: /docs/udon/ContentHandler
[ContentSoundHandler]: /docs/udon/ContentSoundHandler

