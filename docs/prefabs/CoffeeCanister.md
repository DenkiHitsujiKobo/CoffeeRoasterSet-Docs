---
title: CoffeeCanister
parent: "Prefabs"
nav_order: 2
---

# CoffeeCanister

コーヒー豆を保存する缶容器です。


## 使いかた

- Pickupオブジェクトです。
- 中身が入っているときにUseすると、中身がパーティクルとして出てきます。
  - 再度UseすることでパーティクルのON/OFFを切り替えます。
  - 中身が入っていない場合、パーティクルは出せません。
- ほかの容器にパーティクルを当てることで、保持している中身を渡すことができます。
- ほかの容器からパーティクルを当てられると、その中身を受け取ります。
  - 初期設定で受け取れるのは、生の豆と焙煎豆の2種類です。
  - 中身を受け取るときに、その種類に応じた効果音が再生されます。


## 設定項目

以下のコンポーネントが設定できます。  
詳細は各コンポーネントの解説ページをご覧ください。

- CoffeeCanister/System: [ContentHandler]
- CoffeeCanister/System/AudioHandler: [ContentSoundHandler]


## バリエーション

以下の設定バリエーションが、Prefab Variantとしてあらかじめ用意されています。

- `Roasterprefabs/Canister_variation/`
  - `Canister_Eraser.prefab`: 渡された中身を消去するゴミ箱として機能します。
  - `Canister_InfRawBeans.prefab`: 生の豆を無限に出し入れできます。
  - `Canister_InfRoastedBeans.prefab`: 焙煎豆を無限に出し入れできます。



[ContentHandler]: /docs/udon/ContentHandler
[ContentSoundHandler]: /docs/udon/ContentSoundHandler

