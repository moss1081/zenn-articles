---
title: "ポケモンGOチート史：Androidインジェクション系ツールの歴史【PGSharp・Pokemod・PolygonX】"
emoji: "🤖"
type: "tech"
topics: ["pokemongo", "gaming", "history", "android", "security"]
published: true
---

:::message
本記事は研究・歴史的記録を目的としたまとめです。チート行為を推奨するものではありません。
:::

[← シリーズ一覧に戻る](/articles/pokego-cheat-00-overview)

# Androidインジェクション系ツールの歴史

## 技術アーキテクチャ — 3つの方式

### ① APK改造型（Modified APK）

Nianticの公式APKを逆コンパイル→独自コード注入→再署名・再パッケージ→サイドロード。

- **リスク**：Nianticが署名チェックで「公式と異なる署名」を検出しやすい
- **代表**：PGSharp Non-root版、iPogo（改造APK版）

### ② ランチャー注入型（Root Launcher Injection）

公式APKはPlay Storeから正規インストール→Magisk＋root権限でゲームプロセスに機能を外から注入→署名は正規のまま。

- **利点**：Nianticの署名チェックでは「公式アプリ」に見える
- **代表**：PGSharp Rooted版、Pokemod、Polygon/PolygonX

### ③ Xposed / LSposedフレームワーク型（Hook注入）

LSposedフレームワークをMagisk経由でシステムに常駐→PoGOのJavaクラスをフック→メソッド単位で挙動を書き換え。

- **特徴**：最も深いレベルの介入。Mock Location制限の無効化が可能
- **代表**：Pokemod（内部でLSposed利用）、Smali Patcher

---

## 主要ツール詳細

### PGSharp

**2020年リリース〜現在 | Android専用 | pgsharp.com**

2020年に登場したAndroid向け最大手改造APK。Non-root版とRooted Launcher版の2系統を持つ。

**Non-root版（Standard）：**
公式PoGoを削除してPGSharp APKをインストール。脱獄・root不要で手軽だが、Nianticの署名チェックに引っかかりやすい。

**Rooted Launcher版：**
公式PoGoはPlay Storeから正規インストールのまま。Magiskでroot権限を取得しLauncherがゲームプロセスに注入。「Nianticのサーバーからは公式PoGoが見える」という優位性。2022年頃から主流化。

2025年7月のBANウェーブでPGSharp・PGToolsユーザーが集中的に被弾。

**主な機能：**
テレポート / ジョイスティック / エンハンストスロー / 捕獲プレビュー / IVチェック / オートウォーク / クイックキャッチ

---

### Pokemod

**2021年頃〜現在 | Android（root必須）| pokemod.dev | 月額課金制**

「機能の豊富さ」でAndroid mod界最上位と評される。Magisk＋LSposedフレームワークを前提とし、公式PoGoのJavaメソッドをフックして機能を注入する。

最大の特徴は**vPGP（virtual Pokemon GO Plus）** — GOプラスデバイスをソフトウェアでエミュレートし、物理デバイスなしで高速オートキャッチ・オートスピン・自動再接続を実現。

**主な機能：**
vPGP（GOプラスエミュ） / シャイニースキャン / 完全投げ自動 / インスタントキャッチ / リサーチ報酬表示 / バッグ自動整理 / 卵自動孵化 / GBL個体値表示

---

### Polygon → PolygonX

**〜2022年頃→現在 | Android root必須 | Discord限定配布 | 最高プラン$35**

最上位の「ハードコアボット」として位置づけられるAndroid専用ツール。Discordサーバーでのみ配布されており、Google検索からは意図的に見つかりにくくしている。

旧名Polygonからリブランドし、現PolygonX。**「自動ルート生成・バックグラウンドファーム・ターゲット指定捕獲」**など高度な自動化に特化。

**主な機能：**
ターゲット指定自動捕獲 / 自動ルート生成 / バックグラウンドファーム / シャイニーハント / IVフィルター / レイド自動参加

---

### PGTools

**2022年頃〜現在 | pgtools.net | Android（root推奨）**

「スプーフィング」より「自動化」に重きを置いたハイブリッドツール。**自動グラント（GOロケット団）狩りモード**が最大の特徴で、ロケット団を自動で見つけ・バトル・シャドウポケモンを回収するサイクルを無人で回せる。

2025年7月のBANウェーブではPGSharpと並んでPGToolsユーザーが集中的に被弾。

**主な機能：**
自動グラント狩り / オートウォーク / クールダウンタイマー / 自動インベントリ整理 / レイドアシスト

---

### Shungo

**2023年頃〜現在 | Android root必須**

**「シャンドー（Shiny＋Hundo＝色違い＆個体値100%）」**の自動スナイピングに特化した超攻撃的なAndroid mod。世界中のシャンドー座標フィードを自動で受信→即座テレポート→捕獲→次の座標へというサイクルを全自動で繰り返す。

不自然な動きになりやすく検出率が高い。「最近BANが急増した」という報告が2024年頃から増加。

---

## 技術変遷タイムライン

| 時期 | 主な変化 |
|---|---|
| 〜2017年 | Android標準の「モック位置情報」＋GPS Joystickが主流。Nianticが「モック位置情報アプリのインストール検出」を開始 |
| 2018〜2019年 | SafetyNet強化でroot端末を検出しBANするように。Magisk＋Magisk Hideでroot隠蔽が標準化。Smali Patcherが登場 |
| 2020年 | PGSharp登場（APK改造型）。Non-root版でも動作する手軽さで爆発的普及 |
| 2021年〜 | Pokemodが登場。LSposedフレームワークを利用したフック注入型の洗練された実装。vPGP機能が革新的と評価 |
| 2022年 | PolygonXがDiscord限定コミュニティで拡大。PGSharp Rooted（Launcher注入型）が登場 |
| 2023年 | GoogleがSafetyNetを**Play Integrity API**に移行。新しいbypass（MagiskのZygisk DenyList＋Play Integrity Fix）が開発される |
| 2024年〜 | 「Magisk＋Zygisk＋LSposed＋Play Integrity Fix＋DenyList」という構成が標準に |
| 2025年7月〜 | PGSharp・PGTools対象の大規模BANウェーブ。PokemodやPolygonXは比較的被害が少なかったとされる |

---

## ツール比較（2026年時点）

| ツール | Root | BANリスク | 主な用途 | 価格 |
|---|---|---|---|---|
| PGSharp Non-root | 不要 | 高 | スプーフ全般 | 無料/月額 |
| PGSharp Rooted | 必須 | 中 | スプーフ全般 | 無料/月額 |
| Pokemod | 必須 | 中 | 自動化・効率化 | 月額課金 |
| PolygonX | 必須 | 中〜高 | ボット・自動化 | 最高$35 |
| PGTools | 推奨 | 高（BAN後） | 農業・自動化 | 月額 |
| Shungo | 必須 | 非常に高 | シャンドースナイプ | 不明 |
| iPogo Android | 不要 | 高 | スプーフ全般 | 無料/VIP |

---

## iOS vs Android — チートの方向性の根本的な違い

| 項目 | iOS | Android |
|---|---|---|
| 基本アーキテクチャ | ウォールドガーデン・コード注入困難 | オープン・システム改変可能 |
| 主な手法 | GPS偽装（外部デバイス・PC経由） | APK改造 / Root注入 / フック注入 |
| Error 12問題 | iOSのLocation API制限で頻発 | AndroidはGPS APIが異なり基本発生しない |
| 機能の深さ | GPS偽装が中心 | 自動化・ボット・UV検出・完全投げなど多様 |

---

[← 日本編 2022〜現在](/articles/pokego-cheat-06-japan-2022-2026)　|　[次の記事：iOS脱獄系 →](/articles/pokego-cheat-08-ios-jailbreak)