---
title: HandyRoaster
parent: "Udonコンポーネント"
nav_order: 3
---

# HandyRoaster

手動焙煎機のメイン機能を持つコンポーネントです。  
[HandyRoasterHandle]および[HeatSource]と連携して使います。

```mermaid
flowchart LR
    accTitle: class relationship
    accDescr: HandyRoaster inherits IHeatableContentHandler, and depends to HandyRoasterHandle and HeatSource.

    roaster("<u>**HandyRoaster**</u>")
    %% handler("ContentHandler")
    %% sound(["ContentSoundHandler"])
    heatable("IHeatableContentHandler")
    heat(["HeatSource"])
    handle(["HandyRoasterHandle"])

    %% handler -->|継承| heatable
    %% handler -.->|依存| sound
    heatable -->|継承| roaster
    heatable <-.->|依存| heat
    roaster <-.->|依存| handle
```

### 関連コンポーネント

- [IHeatableContentHandler]
  - [ContentHandler]
  - [ContentSoundHandler]
- [HeatSource]
- [HandyRoasterHandle]

---

## 機能について

継承元スクリプトの機能を引き継いでいるため、関係する機能をあわせて記載しています。

### [ContentHandler]と共通する機能

- 本コンポーネントと同時に以下のコンポーネントが必要です。
  - Collider系コンポーネント
  - RigidBody (`Use Gravity`オフ、`Is Kinematic`オン)
- [NoneSyncPickupProxy]を介してUseされると、中身をパーティクルとして出すことができます。
  - 再度UseすることでパーティクルのON/OFFを切り替えます。
  - 中身が入っていない場合、パーティクルは出せません。
- ほかのContentHandlerにパーティクルを当てることで、保持している中身を渡すことができます。
- ほかのContentHandlerからパーティクルを当てられると、その中身を受け取ります。
  - 受け取れる中身の種類や挙動は、後述の設定によって決まります。
  - 中身を受け取るときに、その種類に応じた効果音が[ContentSoundHandler]によって再生されます。

### [IHeatableContentHandler]と共通する機能

- 点火している[HeatSource]のCollider判定へ入ると、加熱されていることを知らせるイベントを受け取ります。
  - 判定に入ってから点火する場合・点火してから判定に入る場合のいずれでも反応します。

### 本コンポーネント特有の機能

- 中身が生の豆である場合、かつ加熱されている間は焙煎が行えます。
  - 焙煎できる状態になると、効果音と煙エフェクトが動作します。
- 本コンポーネントに紐づいた[HandyRoasterHandle]をピックアップすると豆の焙煎が進みます。
  - 焙煎が進むのはハンドルがピックアップされている間のみです。
  - 途中でハンドルを手放すと、焙煎の進行度も途中で止まります。
- 後述の設定によって決められた時間が経過すると焙煎が完了し、中身が生の豆から焙煎豆へ変化します。
  - 中身の量は、焙煎の前後でそのまま引き継がれます。



## 設定項目

共通の設定については[ContentHandler]の説明も合わせてご参照ください。

| Components | 説明 |
| ---- | ---- |
| Pop Audio | 焙煎でコーヒー豆が弾ける効果音を再生するためのAudioSourceを設定します。[^1] [^2] |
| Effects | 焙煎にともなう煙エフェクトを出すためのParticleSystemを設定します。 |

| Settings | 説明 |
| ---- | ---- |
| Roast Time | コーヒー豆の焙煎にかかる時間 (float型 単位:秒) を設定します。 |


## 仕様詳細

各継承元スクリプトの仕様詳細も合わせてご参照ください。

- 効果音の再生は`AudioSource::Play()`で行われます。

---

### 注釈

[^1]: AudioSourceは別オブジェクトに付与されていても構いません。
[^2]: 再生したい音源(AudioClip)は、該当のAudioSource側で設定してください。



[IHeatableContentHandler]: /docs/udon/IHeatableContentHandler
[ContentHandler]: /docs/udon/ConentHandler
[NoneSyncPickupProxy]: /docs/udon/NoneSyncPickupProxy
[ContentSoundHandler]: /docs/udon/ContentSoundHandler
[HeatSource]: /docs/udon/HeatSource
[HandyRoasterHandle]: /docs/udon/HandyRoasterHandle

