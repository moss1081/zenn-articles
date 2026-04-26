---
title: "ポケモンGOチート10年史【全体概観】2016〜2026"
emoji: "🗺️"
type: "tech"
topics: ["pokemongo", "gaming", "history", "spoofing", "security"]
published: true
---

:::message
本記事は研究・歴史的記録を目的としたまとめです。チート行為を推奨するものではありません。掲載情報はReddit・GitHub・海外/日本語ゲームメディア等の公開情報に基づいています。
:::

# ポケモンGOチート10年史（2016〜2026）

2016年7月にポケモンGOがリリースされた瞬間から、チートツールとNianticの攻防が始まった。本シリーズは2016年から2026年現在までの約10年間にわたる「チートの歴史」を、海外・日本の両視点から体系的に記録したものである。

## シリーズ構成

| 記事 | 内容 |
|---|---|
| 本記事（全体概観） | 10年間の流れと主要転換点の俯瞰 |
| [海外編 2016〜2017年](/articles/pokego-cheat-01-global-2016-2017) | 誕生期・PokeVision・Necrobot・Unknown6 |
| [海外編 2018〜2021年](/articles/pokego-cheat-02-global-2018-2021) | iSpoofer・Global++訴訟・COVID・MAD登場 |
| [海外編 2022〜現在](/articles/pokego-cheat-03-global-2022-2026) | 新AIアンチチート・Scopely買収・ハードウェア化 |
| [日本編 2016〜2017年](/articles/pokego-cheat-04-japan-2016-2017) | ピゴサ・マジゴー・日本固有エコシステム |
| [日本編 2018〜2021年](/articles/pokego-cheat-05-japan-2018-2021) | iSpoofer普及・マジゴー消滅・COVID |
| [日本編 2022〜現在](/articles/pokego-cheat-06-japan-2022-2026) | GOフェスト大阪・Scopely売却・アジアBAN |
| [Androidインジェクション系](/articles/pokego-cheat-07-android) | PGSharp・Pokemod・PolygonX・技術解説 |
| [iOS脱獄系](/articles/pokego-cheat-08-ios-jailbreak) | Cydia・JBツール変遷・署名方式の進化 |

---

## 10年間の大きな流れ

### 第1期（2016〜2017年）：「無法地帯」
リリース直後からAPIリバースエンジニアリングが始まり、PokeVision・PokemonGo-Map・Necrobotが爆発的に普及。Nianticは対策として「Unknown6暗号化」「シャドウBAN」「PokeVision強制閉鎖」を実施したが、チートコミュニティの成長速度に追いつけなかった時期。

### 第2期（2018〜2021年）：「法的対抗と技術進化」
CAPTCHAによりAPIスキャナーが機能不全に陥り、「実機スキャン（MAD/RDM）」という革命的な技術転換が起きた。NianticはGlobal++を提訴し2021年に$500万ドルの和解を勝ち取るが、iSpoofer→iPogo/PGSharpというツールの世代交代も起きた。COVID-19がリモートレイドパスを生み、ゲームと現実の境界が変わった。

### 第3期（2022〜現在）：「AIと法の時代」
新AIアンチチートが常時稼働方式になり、GO Fest直後のBANウェーブが定例化。iOS側はError 12問題でソフトウェア改造が困難になりBluetoothハードウェアスプーファーが台頭。2025年3月にはScopelyが$35億でNianticのゲーム事業を買収し、新たな局面へ。

---

## ツール変遷サマリー

| 時期 | iOS主力 | Android主力 | スキャナー |
|---|---|---|---|
| 2016 | HackRF / TutuApp | Fake GPS / Necrobot | PokeVision → PokemonGo-Map |
| 2017 | TutuApp + PokeGo++ | GPS Joystick | RocketMap / Monocle |
| 2018 | iSpoofer | Fake GPS系 | MAD / RDM 登場 |
| 2019 | iSpoofer（停止へ） | 各種偽装アプリ | MAD主流 |
| 2020 | iPogo | PGSharp | MAD + クラウドソーシング |
| 2021〜2022 | iPogo | PGSharp | MAD + RDM 2強 |
| 2023〜2024 | iAnyGo Bluetooth | PGSharp（BAN多発） | 手動型（日本） |
| 2025〜現在 | Bluetooth系 | PGSharp（限定的） | MAD + 手動型 |

---

## 訴訟・法的重要事項

| 時期 | 内容 |
|---|---|
| **2016年** | Niantic、Bossland GmbH（ドイツ）を提訴 |
| **2017年** | Bossland訴訟で約$900万ドルの損害賠償判決が確定（被告欠席）。Nianticが法廷で勝利した最初の大型ケース |
| **2019年6月** | Niantic、Global++を著作権侵害等で提訴（PokeGo++・Ingress++・Potter++） |
| **2021年1月** | Global++ $500万ドル和解成立。永久停止に合意 |
| **2025年3月12日** | Scopely（サウジPIF傘下）がNianticのゲーム事業を$35億で買収 |

:::message
Bossland訴訟（2017年）はGlobal++訴訟（2021年）より先に確立された法的前例。「チートツールの商業的販売はNianticの著作権・契約違反にあたる」という判断がここで初めて確立された。
:::

---

## 座標配信エコシステム — Pokedex100に代表されるDiscordスキャナーネットワーク

### Pokedex100とは

2016年11月に創設された世界最大級のポケモンGO座標配信Discordサーバー。**50万人以上**のメンバーを抱え、30カ国以上のリアルタイム座標を無料・有料で配信している。

### なぜ捕獲前にIVがわかるのか

ポケモンGOのサーバーはクライアント端末に「このエリアにいるポケモン」の情報を送信する際、個体値（IV）・CP・技・消滅タイムスタンプを含めて送信している。MAD・RDMはこの通信データを傍受（MITM）して取得するため、**捕獲しなくても100IVかどうかが事前にわかる**。

### 技術スタック

スキャナー（MAD/RDM）
↓ ポケモン出現データ取得
データベース（MySQL）
↓ Webhook（HTTP POST）
フィルタリング（PokeAlarm / Poracle / WhMgr）
↓ 条件に合致したポケモンのみ
Discord（Pokedex100等）
↓ リアルタイム座標通知
ユーザー（スプーフィングツールでテレポート→捕獲）

### 主要な座標配信サービス

| サービス | 規模 | 特徴 |
|---|---|---|
| **Pokedex100** | 50万人超 | 最大規模・30カ国対応・無料あり |
| **PokeXperience** | 大規模 | 有料特化・月額制・種族別チャンネル |
| **PokeSniper** | 8万人超 | 専用ウェブサイトとDiscord連携 |

---

## 情報源

- **GitHub**：tejado/pgoapi, AeonLucid/POGOProtos, AHAAAAAAA/PokemonGo-Map, Map-A-Droid/MAD, RealDeviceMap/RealDeviceMap
- **Reddit**：r/pokemongo, r/pokemongodev, r/pokemongobotting, r/TheSilphRoad, r/pokemongospoofing
- **日本**：5ch（krsw.5ch.net）, みんポケ（9db.jp）, AUTOMATON, 4Gamer, ITmedia