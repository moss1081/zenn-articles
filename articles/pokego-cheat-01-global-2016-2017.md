---
title: "ポケモンGOチート史：海外編 2016〜2017年【誕生期とシャドウBAN】"
emoji: "🌍"
type: "tech"
topics: ["pokemongo", "gaming", "history", "spoofing", "security"]
published: true
---

:::message
本記事は研究・歴史的記録を目的としたまとめです。チート行為を推奨するものではありません。
:::

[← シリーズ一覧に戻る](/articles/pokego-cheat-00-overview)

# 海外編 2016〜2017年：誕生期とシャドウBAN

## 2016年：無法地帯の誕生

### リリース直後からAPIリバースエンジニアリング開始

2016年7月6日のリリース翌日から、GitHubでAPIのリバースエンジニアリングが始まった。tejado/pgoapi（Python）がProtobufスキーマを解析し、AeonLucid/POGOProtosが中央リポジトリとして機能した。

### PokeVision（2016年7月中旻）

5日で2700万ユーザーを獲得した地図サービス。「3ステップバグ」の代替として爆発的に普及したが、7月31日にNiantic CEO発言を受けて閉鎖。

### PokemonGo-Map（AHAAAAAAA/PokemonGo-Map）

2週間で960万ビュー・44,000クローン・160コントリビューターを記録したオープンソースのスキャナー。後のRocketMapの原型となった。

### Necrobot（C#・無料）

時速5万XPを叩き出した自動化ボット。自動捕獲・進化・転送機能を実装。2016年8月18日の第1回大規模BANウェーブを受けてGitHubからソース削除。

### Unknown6暗号化とTeam Unknown6

2016年8月上旬にNianticがAPI通信に暗号化（Unknown6）を実装。r/pokemongodevを起点にTeam Unknown6が3.5日で解読し、pogodevorg/TU6としてGitHubに公開した。

### GPSスプーフィングの方法（2016年当時）

- **Android**：開発者オプション「モック位置情報」で設定可能（比較的簡単）
- **iOS**：HackRFハードウェア（約$300）が必要で参入障壁が高かった

### Soft BAN概念の確立

8月18日の大規模BANウェーブでSoft BAN（約20時間、ポケモンが逃げ続ける）という段階的BAN概念が確立された。

---

## 2017年：シャドウBANとPokeGo++

### RocketMap・Monocleが事実上の標準スキャナーに

- **RocketMap**（GitHub: RocketMap/RocketMap）：PokemonGo-Mapの後継。多機能・高拡張性でコミュニティの標準スキャナーに
- **Monocle**（GitHub: Noctem/Monocle）：asyncio・スポーンポイント学習・CAPTCHA自動解決を実装

### シャドウBANの登場（2017年5月下旬）

レアポケモンが自分には見えなくなるシャドウBANが登場。Kotakuが報道し、r/TheSilphRoadが解析。検出手法として①インストールアプリスキャン②機械学習ベースの行動分析が採用されたとされる。

### PokeGo++（Global++）

iOS向けオールインワンModとして登場。ジェイルブレイク不要で動作し、TutuApp経由で配布。ジョイスティック・テレポート・完全投げ・IVチェック機能を統合。後に2021年の$500万ドル訴訟和解の対象となる。

### GOフェスト シカゴ大失敗（2017年7月22日）

QRコード突破・ネット障害が重なり大混乱。スプーファーが遠隔参加し、Nianticの杜撰な運営が露呈した。

### レイドバトル実装（2017年6月29日）

レイドバトルの実装がスプーフィングの新たな動機となった。世界中の伝説レイド座標を共有するDiscordサーバーが急増。

---

## 主要ツール一覧（2016〜2017年）

| ツール | 種別 | 対象 | 状態 |
|---|---|---|---|
| PokeVision | スキャナー | ブラウザ | 2016年7月閉鎖 |
| PokemonGo-Map | スキャナー | PC | RocketMapに発展 |
| Necrobot | ボット | PC/Android | 2016年8月BAN後削除 |
| RocketMap | スキャナー | PC | 2020年頃に衰退 |
| Monocle | スキャナー | PC | 2020年頃に衰退 |
| PokeGo++ | スプーフ | iOS/Android | 2019年訴訟で終了 |
| GPS Joystick | スプーフ | Android | 一部継続 |
| LocationFaker | スプーフ | iOS（JB） | 現在も存在 |

---

[次の記事：海外編 2018〜2021年 →](/articles/pokego-cheat-02-global-2018-2021)