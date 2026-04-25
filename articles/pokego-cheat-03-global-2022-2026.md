---
title: "ポケモンGOチート史：海外編 2022〜現在【新AIアンチチート・Scopely買収・ハードウェア化】"
emoji: "🤖"
type: "tech"
topics: ["pokemongo", "gaming", "history", "spoofing", "security"]
published: false
---

:::message
本記事は研究・歴史的記録を目的としたまとめです。チート行為を推奨するものではありません。
:::

[← シリーズ一覧に戻る](/articles/pokego-cheat-00-overview)

# 海外編 2022〜現在：新AIアンチチート・Scopely買収・ハードウェア化

## 2022年：新AIアンチチート本格展開

### Niantic新AIアンチチートシステム正式発表（2022年6月）

「より高速・高精度にチートを特定し、正規プレイヤーへの誤検知を削減」と発表。全Nianticゲームに統合・常時適用する設計（以前は波状のBANウェーブ方式）に移行。

### GO Fest 2022 各都市開催 → 毎イベント後にBANウェーブ

Berlin（7/1〜3）・Seattle（7/22〜24）・Sapporo（8/5〜7）・Finale（8/27）と国際イベントが続くたびにBANウェーブが発動。「イベント中は安全に見えてもデータを収集されている」という認識がコミュニティに定着。

### iPogo / PGSharpが2大ツールとして確立

- **iPogo（iOS/Android）**：iSpoofer後継の最有力ツール。テレポート・ジョイスティック・オートキャッチ・シャイニースキャン・グローバルレイドリスト
- **PGSharp（Android）**：Non-root版・Rooted Launcher版の2系統。エンハンストスローが人気

### iTools BT（Bluetoothハードウェア）台頭

ThinkSkySoft製の物理Bluetoothデバイス（$73〜100）。iPhoneにBluetooth接続しシステムレベルでGPSを偽装するため、ゲームアプリのコードを改変しない。「最も安全な手法」としてr/pokemongospoofingで推奨された。

---

## 2023年：リモートレイドネーフとError 12問題

### リモートレイドパス大幅値上げ＋1日5回制限（2023年4月6日）

単体195コイン（旧100コイン）・3パック525コイン（旧300コイン）に値上げ。1日5回制限を導入。r/pokemongoに空前の反発。「これはスプーフィングを正当化する」という意見が多数。

### Fast Catch誤BANウェーブ（2023年11月15日）

「Fast Catch（速捕獲）」テクニックがBANの誤検知を引き起こすバグが発生。チートしていない多数の正規プレイヤーが突然BANされた。NianticがFast Catchのバグが原因と公式認定し翌日に修正。

### PC連携型Bluetoothスプーファー（iAnyGo / AnyTo）の台頭

PCにインストールしたソフトからスマートフォンにBluetooth接続で位置情報を送り込む新方式。iAnyGo（Tenorshare製）・AnyTo（iMyFone製）が代表例。月額課金モデル（$9.95〜）。「改造アプリ不要・脱獄不要・公式PoGoそのまま」として急速に普及。

### 「Error 12」がソフトスプーファーの最大の壁に

NianticのGPS検証強化により、改造アプリ系スプーファー（iPogo/PGSharp）を使うと「Failed to Detect Location (12)」エラーが頻発。Appleがも位置情報APIに監視機構を実装したことで、従来の偽装が機能しにくくなった。

---

## 2024年：史上最大規模の誤BAN事件

### 史上最大規模の誤BANウェーブ（2024年10月26日）

ギガンタマックスバトルイベント開始直後、主にAndroid端末のユーザー数千人が突然30日BANを受ける。チートしていない正規プレイヤーが多数含まれており「電車や車で移動しながらプレイしていただけ」という報告が殺到。Nianticが正式に誤りを認め取り消し処理を実施。

### 「マイクロGPSドリフト」exploitの横行と取り締まり

GPSをON/OFFする等の操作で位置情報を意図的にずらし、リモートレイドパスを使わずに通常パスでレイドに参加するテクニック。Niantic Community ManagerがDiscordで「ToS違反・検出・BAN対象」と明言。

---

## 2025年：Scopely買収と新世代BANウェーブ

### Niantic→Scopely売却（2025年3月12日）

ScopelyがNianticのゲーム事業（Pokemon GO・Pikmin Bloom・Monster Hunter Now）を35億ドルで買収。Scopelyはサウジアラビアの政府系ファンド（PIF）傘下。2024年のPoGo収益は10億ドル超・月間アクティブユーザー2000万人以上。

### PGSharp / PGTools 大規模BANウェーブ（2025年7月）

ゲームアップデート後にPGSharpおよびPGToolsユーザーを標的とした大規模BANを実施。数千件の7日ストライク〜30日停止が報告される。

### 日本・韓国・アジア圏大規模BANウェーブ（2025年11月）

日本・韓国を中心に突然のBANウェーブ。正規プレイヤーも多数被弾。「IngressとPoGOが連携した位置情報・行動履歴の遡及チェックシステム」が原因と推定される。

### スプーフィング手法の「ハードウェア化」

AppleのiOS位置情報API監視機構強化により、従来の改造アプリが実用性低下。代わりにBluetoothハードウェア系（iTools BT / iAnyGo Bluetooth）が主流化。スプーフィングの「民主化」から「有料化・複雑化」への逆行が起きている。

---

## 2026年現在の状況

| カテゴリ | 主要ツール | リスク |
|---|---|---|
| iOS スプーフ | iAnyGo BT / iTools BT | 低〜中 |
| iOS スプーフ（改造アプリ） | iPogo | 高 |
| Android スプーフ | PGSharp Rooted | 中 |
| Android 自動化 | Pokemod / PolygonX | 中〜高 |
| スキャナー | MAD + RDM | 中 |
| 日本マッピング | みんポケ / GO FRIEND | 低（合法） |

---

[← 海外編 2018〜2021年](/articles/pokego-cheat-02-global-2018-2021)　|　[次の記事：日本編 2016〜2017年 →](/articles/pokego-cheat-04-japan-2016-2017)