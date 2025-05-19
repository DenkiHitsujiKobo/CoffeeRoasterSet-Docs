---
title: 使いかた
nav_order: 2
description: "About usage"
permalink: /docs/usage
---

# 使いかた

ここでは本アセットの基本的な使いかたを解説します。


## 0. UnityPackageのインポート

<a href="https://cultnhut.booth.pm/items/6861803" target="_blank" rel="noopener noreferrer">販売ページ</a>から購入・ダウンロードしたUnityPackageを、ご自身のVRChat用ワールドが入ったUnityプロジェクトへインポートしてください。

インポート後、以下のファイル類が`Assets`フォルダ以下に作成されます。

WIP: ここにフォルダパスを書く


## 1. Prefabの配置

`WIP:prefabフォルダへのパスを記入`フォルダより、以下のPrefabをお好きな数だけワールドに設置します。

- [JuteBag]
- [RoasterSet]
- [CoffeeCoolerSet]
- [CoffeeCanister]

設置例  
<img src="/assets/images/usage/usage01.png" width="80%" alt="picture on Unity editor">

以上で基本的なセットアップは完了です。  
ワールドをアップロードする、またはUnityエディタ上のClientSimを使って、ギミックが機能することをご確認ください。

---

## 2. 焙煎のやりかた

ワールドに設置したPrefabギミックを使い、コーヒー豆の焙煎を行います。

### 2-1. 豆を焙煎機に入れる

生コーヒー豆の袋([JuteBag])を持ってUseすると、生のコーヒー豆が出てきます。  
これを焙煎機のシリンダー([RoasterPickup])に当てて、豆を注ぎこみます。

<img src="/assets/images/usage/usage02.png" width="80%" alt="picture on vrchat, player is pouring raw beans into the roaster.">

豆を入れたのち、シリンダーをスタンドに戻します。

### 2-2. 豆の焙煎

焙煎機の下にあるアルコールランプ([AlcoholLamp])を、持ってUseすると点火します。  
ランプに火が点いた状態で、焙煎機スタンドの下に置いてください。  
シリンダーが加熱されていれば、両脇から湯気が出ます。

<img src="/assets/images/usage/usage03.png" width="80%" alt="picture on vrchat, the roaster with rising smoke.">

シリンダーを加熱している状態でハンドルを回すと、コーヒー豆の焙煎が進みます。  

<img src="/assets/images/usage/usage04.png" width="80%" alt="picture on vrchat, player is turning the roaster.">

シリンダーの小窓から見える豆の色が、白から茶色へ変わっていれば焙煎は完了です。

<img src="/assets/images/usage/usage05.png" width="80%" alt="picture on vrchat, the roaster before roasting and after.">

{: .note}
焙煎の所要時間は設定で変更することが可能です。  
詳しくはPrefab/[RoasterPickup]とUdonコンポーネント/[HandyRoaster]の説明をご覧ください。

### 2-3. 焙煎した豆を冷やす

シリンダーに入っている豆を冷却器([Colander])へ移し、風を当てて冷やします。

<img src="/assets/images/usage/usage06.png" width="80%" alt="picture on vrchat, player is pouring roasted beans into the colander.">

{: .highlight }
現在のところ、実際に豆の温度などを管理する機能はギミック内に実装されていません。  
コーヒー焙煎の過程を楽しむ演出としてご利用ください。

### 2-4. 豆の保管

クーラーで冷やした豆を、缶容器([CoffeeCanister])に移して保存します。

<img src="/assets/images/usage/usage07.png" width="80%" alt="picture on vrchat, player is pouring roasted beans into the canister.">

以上でコーヒー豆の焙煎は完了です。

---

## 3. 豆を挽く

今後のアップデートで実装予定です。

## 4. コーヒーを淹れる

今後のアップデートで実装予定です。



[AlcoholLamp]: /docs/prefabs/AlcoholLamp
[CoffeeCanister]: /docs/prefabs/CoffeeCanister
[CoffeeCoolerSet]: /docs/prefabs/CoffeeCoolerSet
[Colander]: /docs/prefabs/Colander
[JuteBag]: /docs/prefabs/JuteBag
[RoasterPickup]: /docs/prefabs/RoasterPickup
[RoasterSet]: /docs/prefabs/RoasterSet

[HandyRoaster]: /docs/udon/HandyRoaster

