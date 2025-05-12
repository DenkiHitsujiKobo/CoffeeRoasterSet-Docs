---
title: 使いかた
nav_order: 2
description: "About usage"
permalink: /docs/usage
---

# 使いかた

ここでは本アセットの基本的な使いかたを解説します。


## 0. UnityPackageのインポート

[販売ページ] [Booth item page]から購入・ダウンロードしたUnityPackageを、ご自身のVRChat用ワールドが入ったUnityプロジェクトへインポートしてください。

インポート後、以下のファイル類が`Assets`フォルダ以下に作成されます。

WIP: ここにフォルダパスを書く


## 1. Prefabの配置

`WIP:prefabフォルダへのパスを記入`フォルダより、以下のPrefabをお好きな数だけワールドに設置します。

- [JuteBag]
- [RoasterSet]
- [CoffeeCoolerSet]
- [CoffeeCanister]

設置例

WIP: Prefabが設置してある様子の画像

以上で基本的なセットアップは完了です。  
ワールドをアップロードする、またはUnityエディタ上のClientSimを使って、ギミックが機能することをご確認ください。

---

## 2. 焙煎のやりかた

ワールドに設置したPrefabギミックを使い、コーヒー豆の焙煎を行います。

### 2-1. 豆を焙煎機に入れる

生コーヒー豆の袋([JuteBag])を持ってUseすると、生のコーヒー豆が出てきます。  
これを焙煎機のシリンダー([RoasterPickup])に当てて、豆を注ぎこみます。

WIP: 生の豆を注ぐ画像

豆を入れたのち、シリンダーをスタンドに戻します。

### 2-2. 豆の焙煎

焙煎機の下にあるアルコールランプ([AlcoholLamp])を、持ってUseすると点火します。  
ランプに火が点いた状態で、焙煎機スタンドの下に置いてください。  
生のコーヒー豆が入ったシリンダーが加熱されると、両脇から湯気が出ます。

WIP: 湯気の出ている画像

シリンダーを加熱している状態でハンドルを回すと、コーヒー豆の焙煎が進みます。  

WIP: ハンドルを回している画像

シリンダーの小窓から見える豆の色が、白から茶色へ変わっていれば焙煎は完了です。

WIP: 焙煎完了前後の画像

{: .note}
焙煎にかかる時間は設定で変更することが可能です。  
詳しくはPrefab/[RoasterPickup]とUdonコンポーネント/[HandyRoaster]の説明をご覧ください。

### 2-3. 焙煎した豆を冷やす

シリンダーに入っている豆を冷却器([Colander])へ移し、風を当てて冷やします。

WIP: Colanderへ豆を注いでいる画像

{: .highlight }
現在のところ、実際に豆の温度などを管理する機能は本アセットに実装されていません。  
コーヒー焙煎の過程を楽しむ演出としてご利用ください。

### 2-4. 豆の保管

クーラーで冷やした豆を、缶容器([CoffeeCanister])に移して保存します。

WIP: 缶に入った焙煎豆の画像

以上でコーヒー豆の焙煎は完了です。

---

## 3. 豆を挽く

今後のアップデートで実装予定です。

## 4. コーヒーを淹れる

今後のアップデートで実装予定です。



[Booth item page]: https://cultnhut.booth.pm/

[AlcoholLamp]: /docs/prefabs/AlcoholLamp
[CoffeeCanister]: /docs/prefabs/CoffeeCanister
[CoffeeCoolerSet]: /docs/prefabs/CoffeeCoolerSet
[Colander]: /docs/prefabs/Colander
[JuteBag]: /docs/prefabs/JuteBag
[RoasterPickup]: /docs/prefabs/RosterPickup
[RoasterSet]: /docs/prefabs/RoasterSet

[HandyRoaster]: /docs/udon/HandyRoaster

