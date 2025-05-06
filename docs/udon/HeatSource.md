---
title: HeatSource
parent: "Udonコンポーネント"
nav_order: 5
---

# HeatSource

コーヒーの焙煎工程で使う熱源となるコンポーネントです。   
加熱対象の[IHeatableContentHandler]へイベントを飛ばします。

## 概要

[INoneSyncPickupEntity]を継承しています。[NoneSyncPickupProxy]を介してUseされることで点火/消火の切り替えができます。


## 設定項目

| Components | 説明 |
| ---- | ---- |
| `Animator` | 状態に応じた見た目の制御を行うためのアニメーターを設定します。 |

| Settings | 説明 |
| ---- | ---- |
| `Handlers` | インスタンス起動時から判定に入っている[IHeatableContentHandler]を設定します。[^1] |


## 仕様詳細
- 本コンポーネントと同時に以下のコンポーネントが必要です。
  - Collider系コンポーネント(Trigger設定オン)
- [IHeatableContentHandler]がCollider判定に入ると、`OnTriggerEnter`イベントが働くことで加熱対象を判断します。

---

[^1]: Unityの仕様によりインスタンス起動時には`OnTriggerEnter`が反応せず、最初から判定に入っているものが加熱対象とならないのを回避するためのものです。<br>最初から[IHeatableContentHandler]が判定に入っていない場合には設定しないことを推奨します。



[INoneSyncPickupEntity]: /docs/udon/INoneSyncPickupEntity
[NoneSyncPickupProxy]: /docs/udon/NoneSyncPickupProxy
[IHeatableContentHandler]: /docs/udon/IHeatableContentHandler

