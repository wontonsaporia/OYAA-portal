# OYAA 3DCG講座パスポート
# Figma コンポーネント仕様書

**バージョン：** 1.2  
**対象ファイル：** OYAA_Passport.fig  
**最終更新：** 2026-03-09

---

## 1. Figmaファイル構成

### ページ構成（Figma左サイドバー「Pages」）

| ページ名 | 内容 |
|---------|------|
| `🗺 Core` | カラー・タイポ・コンポーネント定義置き場 |
| `📘 コアシート` | P01表紙・P02-03地図・P04 Tips |
| `📄 各回シート` | S01〜S08 表面・裏面（全16フレーム） |
| `📋 ワークシート` | X01・X02 |
| `🎓 修了証` | C01 |
| `🔬 Sandbox` | 試作・捨て作業置き場 |

---

## 2. フレーム設定

### シートサイズ（基本単位）

```
幅：  95mm → Figmaで 359px（1mm = 3.7795px）
高さ：170mm → Figmaで 643px

※ バインダー穴込みのサイズ。A6（105×148mm）より細長い縦長フォーマット。
※ 印刷入稿時は塗り足し3mm追加が必要（別途対応）
実用上の近似値として 359 × 643px を使用する
```

### フレーム命名規則

```
コアシート：
  コアシート/P01_表紙
  コアシート/P02-03_地図見開き
  コアシート/P04_Tips

各回シート：
  S01/表面
  S01/裏面
  S02/表面
  S02/裏面
  …（S08まで）
```

---

## 3. カラー定義（Figma Styles に登録する）

### プライマリ（第1期：紺）

| スタイル名 | HEX | 用途 |
|-----------|-----|------|
| `P1/Primary` | `#0D2340` | ヘッダー背景・核ブロック・クエストヘッダー |
| `P1/Accent` | `#5FA0E0` | ラベル文字・アクセント |
| `P1/Sub` | `#7AB0D8` | サブテキスト・タグライン |
| `P1/BackHeader` | `#1A3A1A` | 裏面ヘッダー背景 |
| `P1/BackAccent` | `#80C880` | 裏面ヘッダー文字 |

### セカンダリ（第2期：紫）

| スタイル名 | HEX | 用途 |
|-----------|-----|------|
| `P2/Primary` | `#1A0D40` | ヘッダー背景・核ブロック・クエストヘッダー |
| `P2/Accent` | `#A07AE0` | ラベル文字・アクセント |
| `P2/Sub` | `#B090D8` | サブテキスト・タグライン |
| `P2/BackHeader` | `#3A1A10` | 裏面ヘッダー背景 |
| `P2/BackAccent` | `#E09870` | 裏面ヘッダー文字 |

### ニュートラル

| スタイル名 | HEX | 用途 |
|-----------|-----|------|
| `Neutral/PageBG` | `#F0EDE6` | ページ全体の背景色 |
| `Neutral/NavBG` | `#E8E4DC` | ナビバー背景 |
| `Neutral/BG` | `#FAF8F2` | カード背景 |
| `Neutral/Block` | `#FFFFFF` | ブロック背景 |
| `Neutral/Border` | `#E5DFD0` | ブロック枠線 |
| `Neutral/Line` | `#D5CFC0` | メモ罫線 |
| `Neutral/Label` | `#AAAAAA` | ブロックラベル文字 |
| `Neutral/Body` | `#1A1A1A` | 本文テキスト（クエストmain等） |
| `Neutral/Sub` | `#777777` | サブテキスト |
| `Neutral/HoleBG` | `#F0ECE2` | 穴ガター背景 |
| `Neutral/HoleFill` | `#D8D4C8` | 穴の塗り |
| `Neutral/HoleBorder` | `#C8C4B8` | 穴の枠線 |
| `Neutral/GutterBorder` | `#E0DBD0` | 穴ガター枠線 |

### セマンティック

| スタイル名 | HEX | 用途 |
|-----------|-----|------|
| `Semantic/OK/BG` | `#F4FFF4` | コツブロック背景 |
| `Semantic/OK/Border` | `#A8DCA8` | コツブロック枠線 |
| `Semantic/OK/Label` | `#2A7A2A` | コツラベル文字 |
| `Semantic/NG/BG` | `#FFF8F0` | 詰まりブロック背景 |
| `Semantic/NG/Border` | `#F0C080` | 詰まりブロック枠線 |
| `Semantic/NG/Label` | `#B05000` | 詰まりラベル文字 |
| `Semantic/KW/BG` | `#FFFBE6` | キーワードタグ背景 |
| `Semantic/KW/Border` | `#E8CC50` | キーワードタグ枠線 |
| `Semantic/KW/Text` | `#6A4E00` | キーワードタグ文字 |
| `Semantic/Result/BG` | `#FFFBE6` | 成果物ブロック背景 |
| `Semantic/Result/Text` | `#4A3800` | 成果物テキスト |
| `Semantic/Result/Sub` | `#8A7040` | 成果物サブテキスト |
| `Semantic/HL/BG` | `#FFF3E0` | ハイライトアイコン背景 |
| `Semantic/HL/Border` | `#F0B840` | ハイライトアイコン枠線 |
| `Semantic/Quest/IconBG` | `#F0F4FF` | クエストアイコン背景 |
| `Semantic/Quest/IconBorder` | `#C8D8F8` | クエストアイコン枠線 |
| `Semantic/Badge/BG` | `#FFF3E0` | バッジ背景 |
| `Semantic/Badge/Text` | `#A06000` | バッジ文字 |
| `Semantic/Next/Title` | `#FFD060` | 次回予告タイトル文字 |

### 地図専用（Map）

地図見開き（P02–03）専用カラー。古地図テーマで統一。各回シートには使用しない。

#### 背景

| スタイル名 | HEX | 用途 |
|-----------|-----|------|
| `Map/Paper/L1` | `#F2E8D0` | 左ページ背景グラデーション（明） |
| `Map/Paper/L2` | `#E8D8B8` | 左ページ背景グラデーション（中） |
| `Map/Paper/L3` | `#D8C8A0` | 左ページ背景グラデーション（暗） |
| `Map/Paper/R1` | `#EDE0C4` | 右ページ背景グラデーション（明） |
| `Map/Paper/R2` | `#E0CFA8` | 右ページ背景グラデーション（中） |
| `Map/Paper/R3` | `#CFC090` | 右ページ背景グラデーション（暗） |

#### ノード・道

| スタイル名 | HEX | 用途 |
|-----------|-----|------|
| `Map/Node/P1BG` | `#3A2A14` | 章1ノード背景（ドーナツ村・暗茶） |
| `Map/Node/P1Accent` | `#C8A060` | 章1ノードアクセント・枠線（ゴールド） |
| `Map/Node/P2BG` | `#0A2A18` | 章2ノード背景（キャラメイク平原・深緑） |
| `Map/Node/P2Accent` | `#60B080` | 章2ノードアクセント・枠線（緑） |
| `Map/Node/P3BG` | `#0A2030` | 章3ノード背景（デザイン湿地・深青緑） |
| `Map/Node/P3Accent` | `#50A0B0` | 章3ノードアクセント・枠線（青緑） |
| `Map/Node/P4BG` | `#2A1A30` | 章4ノード背景（シーンメイク魔境・暗紫） |
| `Map/Node/P4Accent` | `#9A70C0` | 章4ノードアクセント・枠線（紫） |
| `Map/Node/GoalBG` | `#3A1A08` | 章5ノード背景（ドーナツ村🏆・深茶） |
| `Map/Node/GoalAccent` | `#D4880A` | 章5ノードアクセント（琥珀・グロー付き） |
| `Map/Node/Text` | `#F5EAD0` | ノード内テキスト（クリーム白） |
| `Map/Road/Ch1` | `#7A5A28` | 章1の道（茶） |
| `Map/Road/Cross` | `#8A6A30` | ページまたぎの道（明茶） |
| `Map/Road/Ch2` | `#3A7A50` | 章2の道（緑） |
| `Map/Road/Ch3` | `#2A6070` | 章3の道（青緑） |
| `Map/Road/Ch4` | `#5A3A78` | 章4の道（暗紫） |
| `Map/Label/P1` | `#5A3A10` | 第1期エリアラベル文字 |
| `Map/Label/P2` | `#3A1A60` | 第2期エリアラベル文字 |
| `Map/Label/Start` | `#7A4A10` | STARTラベル文字 |
| `Map/Label/Goal` | `#C47808` | GOALラベル文字 |

---

## 4. タイポグラフィ定義（Figma Text Styles に登録する）

使用フォント：**Noto Sans JP**（日本語）、**Space Mono**（英数字・ラベル）

| スタイル名 | フォント | ウェイト | サイズ | 行間 | 用途 |
|-----------|--------|---------|------|------|------|
| `Title/H1` | Noto Sans JP | Black 900 | 20px | 120% | カードタイトル |
| `Title/Tagline` | Noto Sans JP | Regular | 10px | 140% | タグライン |
| `Label/Mono` | Space Mono | Regular | 10px | 100% | Chapter番号・日付 |
| `Label/Block` | Noto Sans JP | Bold | 9px | 100% | ブロックラベル（uppercase） |
| `Body/Main` | Noto Sans JP | Medium | 12px | 160% | 本文・クエストmain |
| `Body/Sub` | Noto Sans JP | Regular | 10.5px | 140% | サブテキスト |
| `Body/Core` | Noto Sans JP | Bold | 14px | 165% | 核テキスト |
| `Body/NextTitle` | Noto Sans JP | Bold | 13px | 130% | 次回予告タイトル |
| `Tag/KW` | Noto Sans JP | Bold | 11px | 100% | キーワードタグ |
| `Tag/Badge` | Noto Sans JP | Bold | 9px | 100% | 技術ハイライトバッジ |
| `Note/Stamp` | Space Mono | Regular | 8px | 100% | スタンプ枠テキスト |

---

## 5. コンポーネント一覧

以下のコンポーネントを `🗺 Core` ページに作成する。  
命名は `ComponentName/Variant` の形式。

---

### C-01：CardHeader（カードヘッダー）

**サイズ：** 幅 359px × 高さ 64px  
**バリアント：** `Period=P1`、`Period=P2`

| レイヤー名 | 種類 | 内容 |
|-----------|------|------|
| `Background` | Rectangle | 幅359×高64。塗り：`P1/Primary` or `P2/Primary` |
| `ChapterLabel` | Text | 「Chapter 01」。スタイル：`Label/Mono`。色：`P1/Accent` |
| `DateLabel` | Text | 「4 / 5」。スタイル：`Label/Mono`。色：`P1/Accent`。右寄せ |
| `Title` | Text | 回タイトル。スタイル：`Title/H1`。色：White |
| `Tagline` | Text | サブタイトル。スタイル：`Title/Tagline`。色：`P1/Sub` |

---

### C-02：BackHeader（裏面ヘッダー）

**サイズ：** 幅 359px × 高さ 36px  
**バリアント：** `Period=P1`、`Period=P2`

| レイヤー名 | 種類 | 内容 |
|-----------|------|------|
| `Background` | Rectangle | 塗り：`P1/BackHeader` or `P2/BackHeader` |
| `ChapterLabel` | Text | 「Chapter 01 — 記録」。スタイル：`Label/Mono`。色：`P1/BackAccent` |
| `DateLabel` | Text | 日付。スタイル：`Label/Mono`。色：`P1/BackAccent`。右寄せ |

---

### C-03：KeywordBlock（キーワードブロック）

**サイズ：** 幅 335px × 高さ Auto  
**レイアウト：** Auto layout（縦）、パディング 6px 8px、Gap 4px

| レイヤー名 | 種類 | 内容 |
|-----------|------|------|
| `Wrapper` | Frame | 塗り：`Neutral/Block`。枠線：`Neutral/Border` 1px。角丸 4px |
| `Label` | Text | 「🔑 キーワード」。スタイル：`Label/Block` |
| `TagRow` | Frame | Auto layout（横）。Wrap。Gap 4px |

**子コンポーネント：KeywordTag**

| レイヤー名 | 種類 | 内容 |
|-----------|------|------|
| `Background` | Rectangle | 塗り：`Semantic/KW/BG`。枠線：`Semantic/KW/Border` 1px。角丸 20px |
| `Text` | Text | キーワード文字。スタイル：`Tag/KW`。色：`Semantic/KW/Text` |

---

### C-04：QuestBlock（クエストブロック）

**サイズ：** 幅 335px × 高さ Auto  
**レイアウト：** Auto layout（縦）、Gap 0px

| レイヤー名 | 種類 | 内容 |
|-----------|------|------|
| `QuestHeader` | Frame | 高さ 28px。Auto layout（横）。塗り：`P1/Primary`。パディング 5px 9px |
| `QuestHeader/Label` | Text | 「⚔️ 今日のクエスト」。スタイル：`Label/Block`。色：`P1/Accent` |
| `QuestHeader/StepCount` | Text | 「4 steps」。スタイル：`Note/Stamp`。色：`P1/Sub`。右寄せ |
| `StepList` | Frame | Auto layout（縦）。塗り White。パディング 7px 9px。Gap 5px |

**子コンポーネント：QuestStep**  
**バリアント：** `Highlight=False`、`Highlight=True`

| レイヤー名 | 種類 | 内容 |
|-----------|------|------|
| `Wrapper` | Frame | Auto layout（横）。Gap 7px。下ボーダー：`Neutral/Border` 1px dashed |
| `Icon` | Frame | 20×20px。角丸 3px。塗り：`Neutral/Block`（通常）or `Semantic/HL/BG`（HL）。枠線 1.5px |
| `Icon/Emoji` | Text | アイコン絵文字 |
| `Content` | Frame | Auto layout（縦）。Gap 2px。flex-grow |
| `Content/Main` | Text | ステップ名。スタイル：`Body/Main` |
| `Content/Sub` | Text | 補足説明。スタイル：`Body/Sub`。色：`Neutral/Sub` |
| `Content/Badge` | Frame | 表示/非表示（Highlightバリアント時のみ表示）。塗り：`Semantic/Badge/BG`。枠線：`Semantic/HL/Border` |
| `Content/Badge/Text` | Text | 「⚡ 技術ハイライト」。スタイル：`Tag/Badge`。色：`Semantic/Badge/Text` |

---

### C-05：TipsRow（コツ/詰まりブロック）

**サイズ：** 幅 335px × 高さ Auto  
**レイアウト：** Auto layout（横）。Gap 5px

| レイヤー名 | 種類 | 内容 |
|-----------|------|------|
| `OKBlock` | Frame | flex-grow。Auto layout（縦）。角丸 4px。塗り：`Semantic/OK/BG`。枠線：`Semantic/OK/Border` |
| `OKBlock/Label` | Text | 「✅ コツ」。スタイル：`Label/Block`。色：`Semantic/OK/Label` |
| `OKBlock/Items` | Frame | Auto layout（縦）。Gap 2px |
| `NGBlock` | Frame | flex-grow。構成はOKBlockと同様。色は`Semantic/NG/*` |

**子コンポーネント：TipItem**

| レイヤー名 | 種類 | 内容 |
|-----------|------|------|
| `Bullet` | Text | 「·」。色：`Neutral/Label` |
| `Text` | Text | Tip本文。スタイル：`Body/Sub`。色：`Neutral/Body` |

---

### C-06：ResultBlock（成果物ブロック）

**サイズ：** 幅 335px × 高さ Auto  
**レイアウト：** Auto layout（横）。Gap 7px。パディング 7px 9px

| レイヤー名 | 種類 | 内容 |
|-----------|------|------|
| `Background` | Rectangle | 塗り：`Semantic/Result/BG`。枠線：`Semantic/KW/Border` 1px。角丸 4px |
| `Icon` | Text | 🏆（18px） |
| `Content` | Frame | Auto layout（縦）。Gap 1px |
| `Content/Title` | Text | 成果物名。スタイル：`Body/Main`。色：`Semantic/KW/Text` |
| `Content/Sub` | Text | 補足。スタイル：`Body/Sub`。色：`Semantic/Badge/Text` |

---

### C-07：CoreBlock（核ブロック・裏面）

**サイズ：** 幅 335px × 高さ Auto  
**バリアント：** `Period=P1`、`Period=P2`

| レイヤー名 | 種類 | 内容 |
|-----------|------|------|
| `Background` | Rectangle | 塗り：`P1/Primary`。角丸 4px |
| `Label` | Text | 「💡 今日のまとめ」。スタイル：`Label/Block`。色：`P1/Accent` |
| `CoreText` | Text | まとめ文。スタイル：`Body/Core`。色：White |

---

### C-08：CheckBlock（今日できたこと）

**サイズ：** 幅 335px × 高さ Auto

| レイヤー名 | 種類 | 内容 |
|-----------|------|------|
| `Wrapper` | Frame | 塗り：`Neutral/Block`。枠線：`Neutral/Border`。角丸 4px |
| `Label` | Text | 「○ 今日できたこと」。スタイル：`Label/Block` |
| `ItemList` | Frame | Auto layout（縦）。Gap 5px |

**子コンポーネント：CheckItem**  
**バリアント：** `Period=P1`、`Period=P2`

| レイヤー名 | 種類 | 内容 |
|-----------|------|------|
| `Circle` | Ellipse | 13×13px。枠線 1.5px：`P1/Primary`（P1）or `P2/Primary`（P2）。塗りなし |
| `Text` | Text | チェック項目文。スタイル：`Body/Sub`。色：`Neutral/Body` |

> **※ 画像挿入予定のスペース**  
> CheckBlockとStampBlockは、後からアイコン・イラストを挿入する前提。  
> Figmaでは `Icon` レイヤーを空のFrameとして確保しておく。

---

### C-09：StampBlock（スタンプ欄）

**サイズ：** 幅 335px × 高さ Auto

| レイヤー名 | 種類 | 内容 |
|-----------|------|------|
| `Wrapper` | Frame | 塗り：`Neutral/Block`。枠線：`Neutral/Border`。角丸 4px |
| `Label` | Text | 「🔖 スタンプ」。スタイル：`Label/Block` |
| `StampBox` | Frame | 46×46px。枠線 1.5px dashed：`Neutral/Label`。角丸 4px。中央揃え |
| `StampBox/Placeholder` | Text | 「STAMP」。スタイル：`Note/Stamp`。色：`Neutral/Label` |

---

### C-10：MemoBlock（メモ欄）

**サイズ：** 幅 335px × 高さ Auto（flex-grow で余白を吸収）

| レイヤー名 | 種類 | 内容 |
|-----------|------|------|
| `Wrapper` | Frame | 塗り：`Neutral/Block`。枠線：`Neutral/Border`。角丸 4px。flex-grow |
| `Label` | Text | 「📝 MEMO」。スタイル：`Label/Block` |
| `Lines` | Frame | Auto layout（縦）。Gap 9px |
| `Lines/Line（×4）` | Rectangle | 幅 100%。高さ 1px。塗り：`Neutral/Line` |

---

### C-11：NextBlock（次回予告）

**サイズ：** 幅 335px × 高さ Auto  
**バリアント：** `Period=P1`、`Period=P2`

| レイヤー名 | 種類 | 内容 |
|-----------|------|------|
| `Background` | Rectangle | 塗り：`P1/Primary`。角丸 4px |
| `Label` | Text | 「📌 次回予告」。スタイル：`Label/Block`。色：`P1/Accent` |
| `NextTitle` | Text | 次回タイトル。スタイル：`Body/NextTitle`。色：`Semantic/Next/Title` |
| `NextDesc` | Text | 次回説明。スタイル：`Body/Sub`。色：`Neutral/Label` |

---

## 6. 各回シートのフレーム組み立て手順

### 表面フレーム構成

```
S01/表面（359×643px）
├── HoleGutter（幅22px・左端、丸穴×3）← 表面は左側
├── CardHeader（C-01）
└── Body（Auto layout 縦、Gap 8px、Padding 10px 12px）
    ├── KeywordBlock（C-03）
    ├── QuestBlock（C-04）
    ├── TipsRow（C-05）
    └── ResultBlock（C-06）
```

### 裏面フレーム構成

```
S01/裏面（359×643px）
├── HoleGutter（幅22px・右端、丸穴×3）← 裏面は右側
├── BackHeader（C-02）
└── Body（Auto layout 縦、Gap 8px、Padding 10px 12px）
    ├── CoreBlock（C-07）
    ├── CheckBlock（C-08）
    ├── StampBlock（C-09）
    ├── MemoBlock（C-10）← flex-grow
    └── NextBlock（C-11）
```

> **HoleGutter：** 幅22px・背景 `Neutral/HoleBG`・境界線1px `Neutral/GutterBorder`。丸穴（直径10px・塗り `Neutral/HoleFill`・枠線 `Neutral/HoleBorder`）を**縦2個均等配置**（2穴確定）。表面では左端（`border-right`）、裏面では右端（`border-left`）に配置。

---

## 6b. 地図見開きフレーム構成（P02–03）

地図はSVGで実装。Figmaでは718×643pxの単一フレームとして管理する。

```
コアシート/P02-03_地図見開き（718×643px）
├── Background（左ページ）  ← Map/Paper/L1〜L3 ラジアルグラデーション
├── Background（右ページ）  ← Map/Paper/R1〜R3 ラジアルグラデーション
├── CrosshatchTexture       ← 薄いクロスハッチパターン
├── ContourDecorations      ← 等高線風の薄い円（装飾）
├── PageDivider             ← x=359 の破線（断ち切り目安）
├── AreaLabels              ← 5章エリア名（下記参照）
├── Roads（道）
│   ├── 01→02（Map/Road/Ch1）
│   ├── 02→03（Map/Road/Cross  ← ページまたぎ・章1→章2）
│   ├── 03→04（Map/Road/Ch2→Ch3、L字折れ）
│   ├── 04→05（Map/Road/Cross  ← ページまたぎ・章3→章4）
│   ├── 05→06（Map/Road/Ch4、L字折れ）
│   ├── 06→07（Map/Road/Ch4）
│   └── 07→08（Map/Road/Ch4→Ch5）
├── Nodes（ノード × 8）
│   ├── Node01–02  ← 章1「ドーナツ村」：Map/Node/P1BG・Map/Node/P1Accent
│   ├── Node03     ← 章2「キャラメイク平原」：Map/Node/P2BG・Map/Node/P2Accent
│   ├── Node04–05  ← 章3「デザイン湿地」：Map/Node/P3BG・Map/Node/P3Accent
│   ├── Node06–07  ← 章4「シーンメイク魔境」：Map/Node/P4BG・Map/Node/P4Accent
│   └── Node08     ← 章5「ドーナツ村🏆」：Map/Node/GoalBG・Map/Node/GoalAccent（グロー付き・円環演出）
├── StartLabel / GoalLabel
└── Legend（凡例）
```

### エリア構成（5章・確定）

| 章 | ノード | エリア名 | カラーキー |
|----|--------|---------|-----------|
| 1 | S01–02 | ドーナツ村 | P1（茶金） |
| 2 | S03 | キャラメイク平原 | P2（緑系） |
| 3 | S04–05 | デザイン湿地 | P3（青緑系） |
| 4 | S06–07 | シーンメイク魔境 | P4（紫系） |
| 5 | S08 | ドーナツ村 🏆 | Goal（琥珀・グロー） |

> S08は章1「ドーナツ村」と同名。地図上でS01-02の近くに配置し、旅が円環で閉じる構造を視覚的に表現する。

### ノード仕様

| 項目 | 値 |
|------|-----|
| サイズ | 114×60px |
| 角丸 | 8px |
| 番号テキスト | Space Mono・9px・Bold・各期Accent色 |
| タイトルテキスト | Noto Sans JP・10px・Bold・`Map/Node/Text` |
| 日付テキスト | Space Mono・8px・各期Accent色 |
| スタンプ枠 | 34×23px・角丸3px・破線枠・各期Accent色（opacity 0.5） |

### ノード座標（基準値）

| No. | cx | cy | ページ |
|-----|----|----|--------|
| 01 | 95 | 118 | 左 |
| 02 | 272 | 95 | 左 |
| 03 | 468 | 108 | 右 |
| 04 | 590 | 295 | 右 |
| 05 | 262 | 310 | 左 |
| 06 | 88 | 478 | 左 |
| 07 | 278 | 505 | 左→右境界付近 |
| 08 | 490 | 520 | 右 |

---

## 7. Figma作業の推奨順序

1. **Stylesを登録する**（§3カラー・§4タイポ）
   - Neutral / P1 / P2 / Semantic / Map の順に登録
2. **Coreページにコンポーネントを作る**（C-01から順番に）
3. **S01の表面・裏面を組む**（動作確認）
4. **S01を複製してS02〜S08を作る**（テキスト差し替えのみ）
5. **コアシートフレームを作る**
   - P01表紙（359×643px）
   - P02-03地図見開き（718×643px・SVG埋め込み or ベクター再現）
   - P04 Tips（359×643px）

---

## 8. 未対応（別途作業）

- **K01知識シート**のワイヤーフレーム・Figmaフレーム定義（優先度高）
- **X01ちびキャラ発想シート**のワイヤーフレーム・Figmaフレーム定義（優先度高）
- **X02オリカデザインシート**のワイヤーフレーム・Figmaフレーム定義（優先度高）
- **バインダー穴仕様の確定**（穴径・穴間隔の実寸確認）
- **スタンプ枠サイズの確定**（実物スタンプ合わせ）
- **地図の章3・章4ノードカラーの最終調整**（上記は仮値）
- 修了証（C01）の判型・デザイン・定義（優先度低）
- 塗り足し・トンボの入稿設定
- イラストの配置ガイドライン（自作予定）
- Tips・ルールページの内容（授業パワポ完成後に検証）
