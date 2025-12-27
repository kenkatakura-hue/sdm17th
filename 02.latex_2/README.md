# SDM 修士論文 LaTeX テンプレート v3

慶應義塾大学大学院 システムデザイン・マネジメント研究科（SDM）向けの修士論文LaTeXテンプレートです。

## 特徴

- ✅ SDM提出要件に準拠（表紙・要旨フォーマット）
- ✅ PDFプロパティ自動設定（KOARA提出対応）
- ✅ **[1]形式の参考文献引用**（クリックでジャンプ）
- ✅ Design Science Research（DSR）構成
- ✅ XeLaTeX対応（日本語フォント）

---

## フォルダ構造

```
thesis_v2_new/
├── main.tex                        # メインファイル
├── refs.tex                        # 参考文献（bibitem形式）
│
├── frontmatter/                    # 前付け
│   ├── titlepage.tex               # 表紙
│   ├── abstract.tex                # 日本語要旨
│   └── abstract-en.tex             # 英語要旨
│
├── chapters/                       # 本文
│   ├── 1_intro/                    # 第1章：序論
│   │   ├── 1_1_background.tex      # 研究背景
│   │   ├── 1_2_objective.tex       # 研究目的・RQ
│   │   ├── 1_3_novelty.tex         # 新規性
│   │   └── 1_4_structure.tex       # 論文構成
│   │
│   ├── 2_literature/               # 第2章：先行研究
│   │   ├── 2_1_domain_a.tex        # 領域A
│   │   ├── 2_2_domain_b.tex        # 領域B
│   │   ├── 2_3_domain_c.tex        # 領域C
│   │   ├── 2_4_positioning.tex     # 研究の位置づけ
│   │   └── 2_5_summary.tex         # まとめ
│   │
│   ├── 3_preliminary/              # 第3章：予備調査
│   │   ├── 3_1_purpose.tex         # 調査目的
│   │   ├── 3_2_method.tex          # 調査方法
│   │   ├── 3_3_result.tex          # 調査結果
│   │   └── 3_4_summary.tex         # まとめ
│   │
│   ├── 4_proposal/                 # 第4章：提案手法
│   │   ├── 4_1_overview.tex        # 概要・ミッション要求
│   │   ├── 4_2_design.tex          # 設計（ステイクホルダー・システム要求）
│   │   ├── 4_3_detail.tex          # 詳細
│   │   └── 4_4_summary.tex         # まとめ
│   │
│   ├── 5_evaluation/               # 第5章：評価実験
│   │   ├── 5_1_purpose.tex         # 実験目的
│   │   ├── 5_2_method.tex          # 実験方法
│   │   ├── 5_3_result.tex          # 実験結果
│   │   ├── 5_4_validation.tex      # 検証・妥当性確認
│   │   └── 5_5_summary.tex         # まとめ
│   │
│   ├── 6_discussion/               # 第6章：考察
│   │   ├── 6_1_findings.tex        # 考察
│   │   ├── 6_2_limitations.tex     # 限界
│   │   └── 6_3_summary.tex         # まとめ
│   │
│   └── 7_conclusion/               # 第7章：結論
│       ├── 7_1_conclusion.tex      # 結論
│       └── 7_2_future.tex          # 今後の展望
│
├── backmatter/                     # 後付け
│   └── acknowledgement.tex         # 謝辞
│
└── appendices/                     # 付録
    └── appendixA.tex               # 付録A
```

---

## 参考文献の書き方

### refs.tex（参考文献リスト）

```latex
\begin{thebibliography}{99}

\bibitem{Howard2017}
Howard, A. G., et al. (2017). MobileNets: Efficient Convolutional Neural Networks for Mobile Vision Applications. \textit{arXiv:1704.04861}.

\bibitem{Tan2019}
Tan, M., \& Le, Q. V. (2019). EfficientNet: Rethinking Model Scaling for Convolutional Neural Networks. \textit{ICML 2019}.

\end{thebibliography}
```

### 本文中での引用

```latex
% 単一引用
MobileNet\cite{Howard2017}は、計算量を大幅に削減した。

% 複数引用
既存手法\cite{Howard2017, Tan2019}と比較した。
```

### 出力イメージ

> MobileNet[4]は、計算量を大幅に削減した。

**[4]をクリック → 参考文献にジャンプ！**

---

## PDFプロパティ設定

main.texの`\hypersetup`を編集してください：

```latex
\hypersetup{
    pdftitle={あなたの論文タイトル},
    pdfauthor={慶應義塾大学大学院システムデザイン・マネジメント研究科},
    ...
}
```

これにより、KOARA提出要件のPDFメタデータが自動設定されます。

---

## 使い方

### 1. Overleafにアップロード

1. zipファイルをOverleafにアップロード
2. Menu → Compiler → **XeLaTeX** を選択
3. Recompile

### 2. 編集の流れ

```
Markdownで下書き
    ↓
Claudeに「LaTeXに変換して」
    ↓
該当の.texファイルを更新
    ↓
Overleafでコンパイル
```

### 3. カスタマイズ

| 変更箇所 | ファイル |
|----------|----------|
| タイトル・氏名 | frontmatter/titlepage.tex |
| 要旨 | frontmatter/abstract.tex, abstract-en.tex |
| 本文 | chapters/各章/ |
| 参考文献 | refs.tex |
| PDFプロパティ | main.tex（hypersetup） |

---

## 提出前チェックリスト

| 項目 | 確認 |
|------|------|
| 表紙が所定フォーマット | □ |
| 日本語要旨・英語要旨あり | □ |
| 専攻名「システムデザイン・マネジメント専攻」 | □ |
| 修了年度が正しい（2025年3月→2024年度） | □ |
| PDFプロパティ（タイトル・作成者）設定済み | □ |
| キーワードが日本語/英語で正しい | □ |
| 参考文献が[1]形式でジャンプ可能 | □ |

---

## 更新履歴

| バージョン | 日付 | 内容 |
|------------|------|------|
| v1 | - | 初版（enumerate形式） |
| v2 | - | DSR構成に変更 |
| **v3** | 2024-12 | bibitem形式に変更、PDFプロパティ追加 |
