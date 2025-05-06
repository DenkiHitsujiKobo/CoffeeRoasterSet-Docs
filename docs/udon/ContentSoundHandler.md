---
title: ContentSoundHandler
parent: "Udonコンポーネント"
nav_order: 2
---

# ContentSoundHandler

中身の種類に対応した音源の再生を行うコンポーネントです。  


## 機能

- [ContentHandler]コンポーネントに紐づけられて使用されます。
- [ContentHandler]からイベントを介して呼び出され、その中身の種類に応じた効果音を再生します。


## 設定項目

| Components | 説明 |
| ---- | ---- |
| `Audio` | 音源の再生に使うためのAudioSourceを設定します。 |

| Sound | 説明 |
| ---- | ---- |
| `Raw Beans` | 生の豆が入れられた際の効果音(AudioClip)を設定します。 |
| `Roasted Beans` | 焙煎豆が入れられた際の効果音(AudioClip)を設定します。 |
| `Coffee Powder` | コーヒー粉が入れられた際の効果音(AudioClip)を設定します。 |
| `Coffee Liquid` | 液体コーヒーが入れられた際の効果音(AudioClip)を設定します。 |
| `Water` | 水が入れられた際の効果音(AudioClip)を設定します。 |

| Options | 説明 |
| ---- | ---- |
| `Volume` | 再生時の音量を設定します。 |


## 仕様詳細
- 音源の再生は`AudioSource::PlayOneShot(...)`で行われます。
  - 音源が重複して再生される仕様のため、設定する音源は尺の短いものを推奨します。
- 現実に起こる現象としては、お湯と水では容器へ注いだ際の音が異なりますが、現時点ではお湯のみを想定して`WATER`に一本化しています。



[ContentHandler]: /docs/udon/ContentHandler

