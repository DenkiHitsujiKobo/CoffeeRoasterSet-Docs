---
title: Colander
parent: "Prefabs"
nav_order: 5
---

# Colander

焙煎したコーヒー豆を冷やすための、冷却器に乗せる金属ザルです。


## 使いかた

- Pickupオブジェクトです。UseすることでパーティクルのON/OFFを切り替えます。
- ほかの容器からパーティクルを当てられると、その中身を受け取ります。
  - 中身を受け取るときに、その種類に応じた効果音が再生されます。
  - 初期設定で受け入れるのは焙煎豆のみです。
- ほかの容器オブジェクトにパーティクルを当てることで、保持している中身を渡すことができます。
- [CoffeeCooler]の近くで手放すと、真上に乗るように位置が補正されます。


## 設定項目

以下のコンポーネントが設定できます。  
詳細は各コンポーネントの解説ページをご覧ください。

- Colander/System: [ContentHandler]
- Colander/System/AudioHandler: [ContentSoundHandler]



[CoffeeCooler]: /docs/prefabs/CoffeeCooler
[ContentHandler]: /docs/udon/ContentHandler
[ContentSoundHandler]: /docs/udon/ContentSoundHandler

