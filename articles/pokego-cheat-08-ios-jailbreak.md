---
title: "ポケモンGOチート史：iOS脱獄系チートの歴史【Cydia・JBツール変遷・署名方式の進化】"
emoji: "🔓"
type: "tech"
topics: ["pokemongo", "gaming", "history", "ios", "jailbreak"]
published: false
---

:::message
本記事は研究・歴史的記録を目的としたまとめです。チート行為を推奨するものではありません。
:::

[← シリーズ一覧に戻る](/articles/pokego-cheat-00-overview)

# iOS脱獄系チートの歴史

## iOSが「ウォールドガーデン」である理由

Appleはコード署名を厳格化しており、iOSは全アプリの起動前にAppleの証明書チェーンで署名を検証する。脱獄（Jailbreak）とは「このチェックを無効化してroot権限でカーネルを書き換える」行為だ。

AndroidがRoot＋Magiskでシステム改変できるのに対し、iOSは脱獄なしにゲームプロセスへの深いコード注入が困難。これがiOS側のチートが「GPS偽装（外部デバイス・PC経由）」という方向に進化した根本的な理由となった。

---

## iOS脱獄ツール年表（PoGoチートに関係した主要JBのみ）

| 時期 | JBツール | 対応iOS | タイプ | PoGoへの影響 |
|---|---|---|---|---|
| 2015〜2016年 | Pangu（iOS 9.x）/ TaiG（iOS 8.x） | iOS 8〜9 | Untethered | PoGOリリース時期。CydiaからLocationFaker・PokeGo++ JB版が即座に登場 |
| 2017年 | Yalu（iOS 10.x）/ Electra（iOS 11.x） | iOS 10〜11 | Semi-untethered | 再起動のたびにJB再適用が必要に。NianticがJB検出を実装→PokePatch/Masterbaで回避 |
| 2018〜2019年 | unc0ver（iOS 11〜12）/ checkra1n（iOS 12〜13） | iOS 11〜13 | Semi-untethered / Semi-tethered | checkra1nはBoot ROMエクスプロイト（checkm8）でiPhone X以下限定。ソフトウェア更新で修正不可 |
| 2020〜2021年 | unc0ver（iOS 13〜14）/ Taurine（iOS 14.x） | iOS 13〜14 | Semi-untethered | SX-PokeGoが登場。「最高のJB向けPoGoチートtweak」として評価される |
| 2022〜2023年 | Dopamine（iOS 15〜16.6.1）/ Palera1n（iOS 15〜17.x） | iOS 15〜16 | Semi-untethered | 現行世代の主要JBツール。「JBのためにiPhone X世代を専用機として使う」文化が確立 |
| 2024〜現在 | iOS 17〜18 / iPhone 12以降: 公開JBなし | — | — | iOS 18でExclaves・SPTM・TXMが組み合わさり脆弱性発見が大幅困難化 |

:::message alert
2026年3月時点で、iOS 17以降・iPhone 12以降の公開JBは存在しない。
:::

---

## JBのタイプとPoGoへの実用的な影響

脱獄にはいくつかのタイプがある。Untethered（永続型）はかつての標準だったが、iOS 9以降実質的に存在しない。現在主流のSemi-untetheredは再起動後にJBアプリを開いて再適用が必要。

PoGoプレイヤーにとってこれは非常に不便で：
- 毎朝JBアプリを開いて再適用が必要
- バッテリー切れ・強制再起動でJBが消え「素のiPhone」に戻る
- 電源OFF前に必ずJB状態を確認しなければならない

これが「JB機は鞄の中で絶対電源を切らない」という運用文化を生んだ。

---

## 脱獄専用PoGoチートTweak

### MobileSubstrate / Substitute / ElleKit（注入フレームワーク）

JB Tweakの注入を担うフレームワーク。

| フレームワーク | 時期 | 採用JB |
|---|---|---|
| MobileSubstrate | 旧世代 | Cydia系全般 |
| Substitute | 中間世代 | Chimera / Sileo系 |
| ElleKit | 現在の標準 | Dopamine環境 |

**注入フロー：**
JB後にSileo/CydiaでTweakをインストール → Dylibが配置される → 次回のPoGo起動時にElleKitがDylibをPoGoプロセスのメモリ空間にmapする → DylibがNiantic製クラスをhookして挙動を書き換える

---

### LocationFaker（Cydia Tweak）

**2016年〜 | JB必須 | 実質引退**

JB系GPS偽装tweakの原点。iOSのCoreLocation.frameworkのメソッドをhookし、CLLocationManagerの返す座標をすり替える。システムワイドな偽装のためPoGo以外の全アプリのGPSも偽装される。単体では「テレポートして止まる」機能のみ。PokeGo++（ジョイスティック移動）と組み合わせて使うのが2016年当時の標準構成だった。

---

### Masterball / PokePatch（JB検出回避Tweak）

**2016〜2019年頃 | cokepokes.github.io**

PoGoが実装したJB検出コードを回避するための専用tweak。チート機能は持たない「JB隠蔽専用ツール」。PoGoをJB端末で正常起動させるために必須だった。

---

### PokeGo++ JB版（Cydia / unlimapps）

**2016〜2019年 | Cydia source: beta.unlimapps.com | MobileSubstrate**

Global++グループが開発した脱獄向けTweak版PokeGo++。MobileSubstrateが公式PoGoプロセスに注入し、UI上にジョイスティックを追加。2019年6月のGlobal++訴訟で全版同時終了。

**主な機能：**
ジョイスティック / テレポート / 完全投げ / IVチェック / 公式PoGoに直接注入

---

### SX-PokeGo（Cydia / Sileo Tweak）

**2021年〜現在 | repo.sx-pokego.xyz | Dopamine/Palera1n対応 | BANリスクあり**

現代JB環境向けの代表的なPoGoチートTweak。単純なGPS偽装を超えた「ライトボット」に近い存在。NianticがSX-PokeGoのJB検出回避バイパスを特定してストライクを出した事例がある。

**主な機能：**
ホットスポットリストからテレポート / オートウォーク（ルート設定）/ オートキャッチ（全/色違い/特定種）/ オートスピン / 完全投げ / ※GPXルート非対応

---

### SpooferPro JB版（SpooferX / Cydia Tweak）

**2022年頃〜現在 | unc0ver・checkra1n・Dopamine対応**

非JB版（IPA配布）のSpooferProの脱獄専用Tweakビルド。JB環境で直接公式PoGoに注入するため証明書失効の問題がなく安定性が高い。KernBypassがバンドルされJB隠蔽に対応。

**主な機能：**
IVプレビュー（エンカウント時）/ スロー変更投げツール / オートウォーク / GPXルート完全対応 / 近傍スポーンライブフィード

---

### iPogo JB版（Sileo/Zebra Tweak）

**Dopamine・Palera1n対応 | ipogo.app/repo/ | ElleKit使用**

iPogo（iOS/Android向け多機能スプーフMod）の脱獄専用Tweakバージョン。ElleKitが注入フレームワークとして機能。JB版のメリットは証明書失効なし・再署名不要・安定動作。ただし「JBしたiPhoneでNianticがPoGoを起動させない」問題を回避するためのHide JB（RootHide・ShadowJB等）が別途必要。

---

## 署名・サイドロード手法の進化（JBなし系）

| 手法 | 時期 | 有効期限 | 特徴 |
|---|---|---|---|
| Enterprise証明書（OTA）| 2016〜現在 | Appleが任意に失効 | Safariからタップだけで完了。最も簡単だが一括失効リスク |
| Cydia Impactor | 2016〜2021年頃 | 7日（無料）/ 1年（$99）| PC＋Apple IDでIPAに署名。2021年頃から動作不安定に |
| AltStore / AltServer | 2019年〜現在 | 7日（自動更新）| PCにAltServerを常駐させ同一Wi-Fi経由で自動再署名 |
| Sideloadly | 2020年〜現在 | 7日（無料）/ 1年（$99）| Cydia ImpactorのUI改善版。iPogo公式推奨 |
| Signulous | 2020年頃〜現在 | 1年（理論上）| 年$20の有料署名プラットフォーム。iPogo公式パートナー |

---

## 2026年現在のiOS JB系チートの現状

**iOS 17以降・iPhone 12以降：公開JBは存在しない。**

iOS 16.7.x以下（Dopamine対応）、またはiPhone X以下のcheckm8デバイス（Palera1n対応）のみJB可能。

**「PoGo専用JB機」文化：**
中古市場でiPhone 6S / 7 / 8 / SE(1st) / X がJB目的で買われる。iOS 16以下で止め、Dopamine＋SX-PokeGo / SpooferPro tweak＋iPogo JB版を入れた「専用機」として運用。

---

## iOS チート方式の最終比較（2026年時点）

| 手法 | JB必要 | 安全性 | 機能の深さ | 手軽さ | 継続コスト |
|---|---|---|---|---|---|
| JB＋SX-PokeGo | 必須 | 中 | ★★★★★ | 低 | 無料 |
| JB＋SpooferPro tweak | 必須 | 中 | ★★★★☆ | 低 | 無料〜有料 |
| iPogo＋Signulous | 不要 | 中 | ★★★★☆ | 中 | $20/年 |
| SpooferX＋Sideloadly | 不要 | 中 | ★★★☆☆ | 中 | 無料 |
| iAnyGo Bluetooth | 不要 | 高 | ★☆☆☆☆ | 高 | $9.95〜/月 |
| iTools BT（物理HW）| 不要 | 高 | ★★☆☆☆ | 高 | $73〜一回 |

JB系は「機能の深さ」では群を抜くが「手軽さ」「継続性」「iOS対応範囲」の点で大きな制約がある。新しいiPhoneユーザーにとってJBベースのPoGoチートはほぼ非現実的な選択肢となっている。

---

[← Androidインジェクション系](/articles/pokego-cheat-07-android)　|　[シリーズ一覧に戻る →](/articles/pokego-cheat-00-overview)