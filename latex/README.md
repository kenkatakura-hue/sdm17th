# SDM 修士論文 LaTeX テンプレート

慶應義塾大学大学院 システムデザイン・マネジメント研究科（SDM）向けの修士論文テンプレートです。

## コンパイル方法

Overleafを使用する場合は、XeLaTeXでコンパイルしてください。

```
Menu → Compiler → XeLaTeX
```

## フォルダ構造

```
latex/
├── main.tex                        # メインファイル（これをコンパイル）
├── refs.tex                        # 参考文献
├── README.md                       # このファイル
│
├── frontmatter/                    # 前付け
│   ├── titlepage.tex               # 表紙
│   ├── abstract.tex                # 日本語要旨
│   └── abstract-en.tex             # 英語要旨
│
├── chapters/                       # 本文
│   ├── 1_intro/                    # 第1章：序論
│   │   ├── 1_1_background.tex      # 研究背景
│   │   ├── 1_2_objective.tex       # 研究目的
│   │   ├── 1_3_novelty.tex         # 本研究の新規性
│   │   └── 1_4_structure.tex       # 本論文の構成
│   │
│   ├── 2_literature/               # 第2章：先行研究
│   │   ├── 2_1_domain_a.tex        # 領域Aの先行研究
│   │   ├── 2_2_domain_b.tex        # 領域Bの先行研究
│   │   ├── 2_3_domain_c.tex        # 領域Cの先行研究
│   │   ├── 2_4_positioning.tex     # 先行研究の課題と本研究の位置づけ
│   │   └── 2_5_summary.tex         # 本章のまとめ
│   │
│   ├── 3_preliminary/              # 第3章：予備調査
│   │   ├── 3_1_purpose.tex         # 調査目的
│   │   ├── 3_2_method.tex          # 調査方法
│   │   ├── 3_3_result.tex          # 調査結果
│   │   └── 3_4_summary.tex         # 本章のまとめ
│   │
│   ├── 4_proposal/                 # 第4章：提案手法
│   │   ├── 4_1_overview.tex        # 提案手法の概要
│   │   ├── 4_2_design.tex          # 手法の設計
│   │   ├── 4_3_detail.tex          # 手法の詳細
│   │   └── 4_4_summary.tex         # 本章のまとめ
│   │
│   ├── 5_evaluation/               # 第5章：評価実験
│   │   ├── 5_1_purpose.tex         # 実験目的
│   │   ├── 5_2_method.tex          # 実験方法
│   │   ├── 5_3_result.tex          # 実験結果
│   │   ├── 5_4_validation.tex      # 検証と妥当性確認
│   │   └── 5_5_summary.tex         # 本章のまとめ
│   │
│   ├── 6_discussion/               # 第6章：考察
│   │   ├── 6_1_findings.tex        # 結果の考察
│   │   ├── 6_2_limitations.tex     # 本研究の限界
│   │   └── 6_3_summary.tex         # 本章のまとめ
│   │
│   └── 7_conclusion/               # 第7章：結論
│       ├── 7_1_conclusion.tex      # 本研究のまとめ
│       └── 7_2_future.tex          # 今後の展望
│
├── backmatter/                     # 後付け
│   └── acknowledgement.tex         # 謝辞
│
└── appendices/                     # 付録
    └── appendixA.tex               # 付録A
```

## 章構成の設計思想

本テンプレートは、SDM修士論文（佐竹, 2019; 真鍋, 2019）の構造をメタ化し、Design Science Research（DSR）およびシステムズエンジニアリングの流れに沿った標準的な章構成としています。

| 章 | 内容 | 対応するDSRフェーズ |
|---|------|-------------------|
| 1 | 序論 | Problem Identification |
| 2 | 先行研究 | Literature Review |
| 3 | 予備調査 | Exploratory Study |
| 4 | 提案手法 | Design & Development |
| 5 | 評価実験 | Demonstration & Evaluation |
| 6 | 考察 | Discussion |
| 7 | 結論 | Communication |

## 編集のヒント

1. **各章を独立して編集**：chaptersフォルダ内のファイルを個別に編集することで、管理しやすくなります。

2. **図表の追加**：figuresフォルダを作成し、`\includegraphics{figures/xxx.pdf}` で読み込むことを推奨します。

3. **参考文献**：refs.texを直接編集するか、BibTeXを使用する場合は別途.bibファイルを作成してください。

## カスタマイズ

### 章構成の変更

main.texの `\input` コマンドを編集することで、章の追加・削除が可能です。

### 品種分類研究以外への適用

サンプルコンテンツ（猫画像認識）は架空の研究テーマです。各.texファイルの内容をご自身の研究に合わせて書き換えてください。

## 注意事項

- 日本語フォントはIPAexMincho/IPAexGothicを使用しています
- Overleaf以外の環境では、フォント設定の変更が必要な場合があります
