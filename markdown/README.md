# SDM 修士論文 Markdown版

慶應義塾大学大学院 システムデザイン・マネジメント研究科（SDM）向けの修士論文テンプレート（Markdown版）です。

## フォルダ構造

```
chapters_md/
├── README.md                       # このファイル
│
├── frontmatter/                    # 前付け
│   ├── titlepage.md                # 表紙
│   ├── abstract.md                 # 日本語要旨
│   └── abstract-en.md              # 英語要旨
│
├── 1_intro/                        # 第1章：序論
│   ├── 1_1_background.md           # 研究背景
│   ├── 1_2_objective.md            # 研究目的
│   ├── 1_3_novelty.md              # 本研究の新規性
│   └── 1_4_structure.md            # 本論文の構成
│
├── 2_literature/                   # 第2章：先行研究
│   ├── 2_1_domain_a.md             # 深層学習に基づく物体検出
│   ├── 2_2_domain_b.md             # 猫画像認識に関する先行研究
│   ├── 2_3_domain_c.md             # 深層学習モデルの軽量化技術
│   ├── 2_4_positioning.md          # 先行研究の課題と本研究の位置づけ
│   └── 2_5_summary.md              # 本章のまとめ
│
├── 3_preliminary/                  # 第3章：予備調査
│   ├── 3_1_purpose.md              # 調査目的
│   ├── 3_2_method.md               # 調査方法
│   ├── 3_3_result.md               # 調査結果
│   └── 3_4_summary.md              # 本章のまとめ
│
├── 4_proposal/                     # 第4章：提案手法
│   ├── 4_1_overview.md             # 提案手法の概要
│   ├── 4_2_design.md               # 手法の設計
│   ├── 4_3_detail.md               # 手法の詳細
│   └── 4_4_summary.md              # 本章のまとめ
│
├── 5_evaluation/                   # 第5章：評価実験
│   ├── 5_1_purpose.md              # 実験目的
│   ├── 5_2_method.md               # 実験方法
│   ├── 5_3_result.md               # 実験結果
│   ├── 5_4_validation.md           # 検証と妥当性確認
│   └── 5_5_summary.md              # 本章のまとめ
│
├── 6_discussion/                   # 第6章：考察
│   ├── 6_1_findings.md             # 結果の考察
│   ├── 6_2_limitations.md          # 本研究の限界
│   └── 6_3_summary.md              # 本章のまとめ
│
├── 7_conclusion/                   # 第7章：結論
│   ├── 7_1_conclusion.md           # 本研究のまとめ
│   └── 7_2_future.md               # 今後の展望
│
├── backmatter/                     # 後付け
│   └── acknowledgement.md          # 謝辞
│
└── appendices/                     # 付録
    └── appendixA.md                # 付録A：データセット詳細
```

## ファイル数

- 本文：23ファイル
- 前付け：3ファイル
- 後付け：1ファイル
- 付録：1ファイル
- **合計：28ファイル**

## 使い方

1. 各Markdownファイルを編集して内容を更新
2. LaTeXに変換する場合は、対応する.texファイルに内容を反映
