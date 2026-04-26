---
title: "ポケモンGOチート史：海外編 2018〜2021年【iSpoofer・Global++訴訟・COVID・MAD】"
emoji: "⚖️"
type: "tech"
topics: ["pokemongo", "gaming", "history", "spoofing", "security"]
published: true
---

:::message
本記事は研究・歴史的記録を目的としたまとめです。チート行為を推奨するものではありません。
:::

[← シリーズ一覧に戻る](https://zenn.dev/moss1081/articles/pokego-cheat-00-overview)

# 海外編 2018〜2021年：iSpoofer・Global++訴訟・COVID・MAD

## 2018年：3ストライク制と実機スキャン革命

### 「赤い警告」大規模展開（2018年3〜4月）

「修正されたクライアントソフトまたは不正なサードパーティーソフトを使用している可能性を検出した」という赤いメッセージがゲーム起動時に表示されるようになった。iOSのGPSスプーフィングアプリインストール済みユーザーの約90%が受信。

### 3ストライク制ポリシー公式化

| ストライク | 処分 |
|---|---|
| 1回目 | 7日間シャドウBAN（レアポケモン非表示） |
| 2回目 | 30日間アカウント停止 |
| 3回目 | 永久BAN |

悪質な行為は3ストライクなしで即時永久BANも。

### iSpoofer台頭

PokeGo++規制強化を受けてiSpooferがiOS勢の主力ツールへ。ジェイルブレイク不要、テレポート・ジョイスティック・IVチェック・Shinyスキャン・自動ウォーク機能を統合。Free版＋Pro版（$3.99/月）のサブスクモデル。

### CAPTCHAによるスキャナー機能不全

NianticがAPIスキャンアカウントにCAPTCHAを大量送信し始め、RocketMap・Monocleのワーカーアカウントが短時間でBANまたはCAPTCHAループに陥る問題が深刻化。

### MAD（Map-A-Droid）登場 — 実機スキャン革命

実際のAndroid端末をPoGo上でリモートGPSコントロールして動かし、スクリーンショットOCRでスキャンするMADが登場（GitHub: Map-A-Droid/MAD）。正規の端末・正規のアカウントを使うためCAPTCHAを受けにくい。

### RealDeviceMap（RDM）登場

iPhoneを使った実機スキャナーRDMも登場（GitHub: RealDeviceMap/RealDeviceMap）。複数のiPhoneを並列に制御しレイド・ポケモン・ポケストップ情報を収集。

---

## 2019年：Global++提訴とiSpoofer停止

### Niantic、Global++を提訴（2019年6月）

NianticがGlobal++グループを著作権侵害・契約違反等で連邦裁判所に提訴。PokeGo++・Ingress++・Potter++の3アプリが対象。「数十万のサブスクリプション販売」「Patreonで収益化」を根拠に。Global++は提訴直後にウェブサイト・Discord・Twitter・Facebookを閉鎖。

### iSpoofer停止

Nianticの法的圧力を受けてiSpooferが一時停止。「サブスクリプションはクリエイターの状況変化により解除されました」という通知メールがユーザーに送信された。

---

## 2020年：COVID-19がゲームの構造を変える

### Nianticが「公式の静止プレイ」を導入

各国のロックダウンを受けてNianticが緊急対応を実施：

- リモートレイドパス導入（自宅からレイドに参加）
- ポケストップ・ジムのインタラクション距離拡大
- ルアーモジュール延長・孵化距離半減
- GO Battle League（自宅でPvP）拡充

スプーファーサブレディットでは「Nianticが間違ってスプーファーを追いかけてきた。これが公式の解答だ」という反応が多数。

### PGSharp登場（Android向け）

2020年にPGSharpがAndroid向けPoGo改造アプリとしてリリース。Root版（高機能）とNon-root版（簡易版）の両方を提供。テレポート・ジョイスティック・IV確認・エンハンストスロー・捕獲プレビューなどを実装。

### iPogo登場（iOS/Android）

iSpoofer後継としてiPogoが登場。テレポート・ジョイスティック・オートキャッチ・オートスピン・シャイニースキャナー・グローバルレイドリスト・クールダウン追跡を実装。有料VIPプランと無料版を提供。

### MADがRocketMapを完全代替

CAPTCHAと大量アカウントBANでRocketMap・Monocleの維持が困難に。MADのフロントエンドとしてRocketMADが開発される。「Androidファーム」（複数の安価なAndroid端末を並べてスキャン）が新たなコミュニティ標準となる。

---

## 2021年：Global++和解と新AIアンチチート開発開始

### Global++ $500万ドル和解成立（2021年1月）

2019年6月提訴のGlobal++訴訟が和解成立。Global++はNianticに500万ドルの損害賠償を支払い、Nianticゲームのハック作成・販売・サーバーへのアクセスを永久停止に同意。Nianticが訴訟に勝利した初めてのケースとして記録される。

### Niantic新AIアンチチートシステム開発開始

後にNianticが公表した内容によると、新しいアンチチートシステムの開発は2021年初頭から始まっていた。機械学習ベースの行動分析・不正ツールのフィンガープリント検出・イベント中の異常行動監視の強化が含まれる。

### スキャナーの2極化

MAD（Androidファーム）とRDM（iPhoneファーム）が2大スキャナーとして確立。有料Discordコミュニティ（月$5〜$20）のバックエンドも軒並みMADに移行。

---

## ツール変遷（2018〜2021年）

| 時期 | iOS | Android | スキャナー |
|---|---|---|---|
| 2018 | iSpoofer（全盛）| Fake GPS系 | RocketMap→限界/MAD登場 |
| 2019 | iSpoofer（停止）| 各種偽装アプリ | MAD主流へ |
| 2020 | iPogo（台頭）| PGSharp登場 | MAD/RocketMAD |
| 2021 | iPogo（主流）| PGSharp（主流）| MAD+RDM 2強 |

---

[← 海外編 2016〜2017年](https://zenn.dev/moss1081/articles/pokego-cheat-01-global-2016-2017)　|　[次の記事：海外編 2022〜現在 →](https://zenn.dev/moss1081/articles/pokego-cheat-03-global-2022-2026)