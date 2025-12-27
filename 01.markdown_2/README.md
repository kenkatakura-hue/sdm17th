# SDM 修士論文 Markdown版 v3

LaTeXテンプレートv3に対応するMarkdown版です。

## 使い方

```
1. Markdownで執筆・編集
2. Claudeに「LaTeXに変換して」と依頼
3. Overleafにアップロード
4. PDF出力
```

## フォルダ構造

```
thesis_md_v3/
├── README.md
├── refs.md                     # 参考文献リスト
│
├── frontmatter/
│   ├── titlepage.md            # 表紙
│   ├── abstract.md             # 日本語要旨
│   └── abstract-en.md          # 英語要旨
│
├── 1_intro/
│   ├── 1_1_background.md       # 研究背景
│   ├── 1_2_objective.md        # 研究目的・RQ
│   ├── 1_3_novelty.md          # 新規性
│   └── 1_4_structure.md        # 論文構成
│
├── 2_literature/
│   ├── 2_1_domain_a.md         # 深層学習・物体検出
│   ├── 2_2_domain_b.md         # 猫画像認識
│   ├── 2_3_domain_c.md         # 軽量化技術
│   ├── 2_4_positioning.md      # 研究の位置づけ
│   └── 2_5_summary.md          # まとめ
│
├── 3_preliminary/
│   ├── 3_1_purpose.md          # 調査目的
│   ├── 3_2_method.md           # 調査方法
│   ├── 3_3_result.md           # 調査結果
│   └── 3_4_summary.md          # まとめ
│
├── 4_proposal/
│   ├── 4_1_overview.md         # 概要・ミッション要求
│   ├── 4_2_design.md           # 設計
│   ├── 4_3_detail.md           # 詳細
│   └── 4_4_summary.md          # まとめ
│
├── 5_evaluation/
│   ├── 5_1_purpose.md          # 実験目的
│   ├── 5_2_method.md           # 実験方法
│   ├── 5_3_result.md           # 実験結果
│   ├── 5_4_validation.md       # 検証・妥当性確認
│   └── 5_5_summary.md          # まとめ
│
├── 6_discussion/
│   ├── 6_1_findings.md         # 考察
│   ├── 6_2_limitations.md      # 限界
│   └── 6_3_summary.md          # まとめ
│
├── 7_conclusion/
│   ├── 7_1_conclusion.md       # 結論
│   └── 7_2_future.md           # 今後の展望
│
├── backmatter/
│   └── acknowledgement.md      # 謝辞
│
└── appendices/
    └── appendixA.md            # 付録A
```

## 参考文献の書き方

### 本文中での引用

```markdown
MobileNet[4]は、計算量を大幅に削減した。

既存手法[4][5]と比較した。
```

### refs.md

```markdown
[1] Redmon, J., et al. (2016). You Only Look Once...
[2] Jocher, G., et al. (2023). Ultralytics YOLOv8...
```

## ファイル数

- 本文: 23ファイル
- 前付け: 3ファイル
- 後付け: 1ファイル
- 付録: 1ファイル
- 参考文献: 1ファイル
- **合計: 29ファイル**
