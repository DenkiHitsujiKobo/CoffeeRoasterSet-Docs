---
title: HandyRoasterHandle
parent: "Udonコンポーネント"
nav_order: 4
---

# HandyRoasterHandle

手動焙煎機の回転ハンドル部分に関わる機能を持つコンポーネントです。  
[HandyRoaster]と紐づけて使います。

```mermaid
flowchart LR
    accTitle: class relationship
    accDescr: HandyRoasterHandle inherits UdonSharpBehaviour, and depends to HandyRoaster.

    handle("<u>**HandyRoasterHandle**</u>")
    behaviour("UdonsharpBehaviour")
    roaster(["HandyRoaster"])

    behaviour -->|継承| handle
    roaster <-.->|依存| handle
```

### 関連コンポーネント

- [HandyRoaster]

---


## 機能について

- 本コンポーネントと同時に以下のコンポーネントが必要です。
  - VRCPickup
    - RigidBody
  - VRCObjectSync
- ピックアップされると、紐づいている[HandyRoaster]へハンドルが掴まれていることを知らせます。
- ハンドルを手放すと、後述の設定によって決められたスナップ位置へテレポートされます。
  - ハンドルのピックアップ判定をもとの位置に戻すための機能です。
- 紐づいている[HandyRoaster]が中身を保持している場合、本コンポーネントの移動速度に応じて効果音を再生します。
  - 焙煎に伴って豆が転がる音を再現するための機能です。
  - 音を鳴らすのは生の豆または焙煎豆が入っている場合のみです。それ以外の場合は音を再生しません。


## 設定項目

| Components | 説明 |
| ---- | ---- |
| Roaster | 連携したい[HandyRoaster]を紐づけます。 |
| Snap | ハンドルが手放されたときのスナップ先となるGameObjectを設定します。 |
| Audio | 焙煎機の中で豆が転がる効果音を再生するためのAudioSourceを設定します。[^1] |

| Settings | 説明 |
| ---- | ---- |
| Velocity | ハンドルが移動していると判断する速度の閾値 (double型 単位:m/s) を設定します。 |


## 仕様詳細

- 本コンポーネントがピックアップされている間、[HandyRoaster]のピックアップ判定は無効化されます。
  - VRCObjectSyncを入れ子にしたとき、ハンドルの戻る位置がズレる現象を緩和するための機能です。
- ハンドルの位置を見失った場合、紐づけた[HandyRoaster]をピックアップすることで本来の位置へ戻ってきます。
- 焙煎機の3Dモデルを回転させる機能は、別途Aim Constraintでハンドルに追従させる想定で設計されています。

---

### 注釈

[^1]: 設定するAudioSourceは別オブジェクトに付与することを推奨します。



[HandyRoaster]: /docs/udon/HandyRoaster

