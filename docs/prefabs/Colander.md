---
title: Colander
parent: "Prefabs"
nav_order: 5
---

# Colander

焙煎したコーヒー豆を冷やすための、冷却器に乗せる金属ザルです。  
他の関連Prefabと一緒に、[CoffeeCoolerSet]に同梱されています。

<img src="/assets/images/prefabs/Colander.png" width="50%" alt="picture of colander.">


## 使いかた

- Pickupオブジェクトです。
- 中身が入っているときにUseすると、中身がパーティクルとして出てきます。
  - 再度UseすることでパーティクルのON/OFFを切り替えます。
  - 中身が入っていない場合、パーティクルは出せません。
- ほかの容器にパーティクルを当てることで、保持している中身を渡すことができます。
- ほかの容器からパーティクルを当てられると、その中身を受け取ります。
  - 初期設定で受け取れるのは焙煎豆のみです。
  - 中身を受け取るときに、その種類に応じた効果音が再生されます。
- [CoffeeCooler]の近くで手放すと、真上に乗るように位置が補正されます。

{: .highlight }
現在のところ、実際に豆の温度などを管理する機能はギミック内に実装されていません。  
コーヒー焙煎の過程を楽しむ演出としてご利用ください。


## 設定項目

以下のコンポーネントが設定できます。  
詳細は各コンポーネントの解説ページをご覧ください。

- Colander/System: [ContentHandler]
- Colander/System/AudioHandler: [ContentSoundHandler]



[CoffeeCoolerSet]: /docs/prefabs/CoffeeCoolerSet
[CoffeeCooler]: /docs/prefabs/CoffeeCooler
[ContentHandler]: /docs/udon/ContentHandler
[ContentSoundHandler]: /docs/udon/ContentSoundHandler

