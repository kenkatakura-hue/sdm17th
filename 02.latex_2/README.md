# SDM 修士論文 LaTeX テンプレート v4

慶應義塾大学大学院 システムデザイン・マネジメント研究科（SDM）向けの修士論文LaTeXテンプレートです。

## 特徴

- ✅ SDM提出要件に準拠（表紙・要旨フォーマット）
- ✅ PDFプロパティ自動設定（KOARA提出対応）
- ✅ **[1]形式の参考文献引用**（クリックでジャンプ）
- ✅ 4階層の見出しスタイル対応
- ✅ XeLaTeX対応（日本語フォント）

---

## SDM提出要件と検証結果

本テンプレートは、SDMの3つの公式ドキュメントに基づいて設計されています。

### 検証対象ドキュメント
1. **HowtoPDF.pdf** - PDF作成要領（協生館修士論文）
2. **shuron_check_list.pdf** - 修士論文提出前自己点検リスト
3. **MastersThesis_sample.docx** - 修士論文サンプル

### 達成状況サマリー

| カテゴリ | 合計 | ✅ 対応済 | ⚠️ 後処理 |
|----------|------|----------|-----------|
| PDF要件 | 4 | 3 | 1 |
| 自己点検リスト | 9 | 9 | 0 |
| Wordサンプル | 13 | 13 | 0 |
| **合計** | **26** | **25 (96%)** | **1 (4%)** |

### 1. PDF作成要件（HowtoPDF.pdf）

| 要求 | 対応状況 | 備考 |
|------|----------|------|
| PDFは「最適化」されたファイル | ⚠️ 後処理 | 提出前にAdobe Acrobatで最適化が必要 |
| 暗号化（パスワード設定）を行わない | ✅ OK | LaTeX出力は暗号化なし |
| PDFプロパティにタイトルを入力 | ✅ OK | `\hypersetup{pdftitle=...}`で設定 |
| PDFプロパティに作成者を入力 | ✅ OK | `\hypersetup{pdfauthor=...}`で設定 |

### 2. 自己点検リスト（shuron_check_list.pdf）

| 要求 | 対応状況 |
|------|----------|
| 日本語表紙あり | ✅ OK |
| 日本語要旨あり | ✅ OK |
| 英語要旨あり | ✅ OK |
| 表紙が所定のフォーマット | ✅ OK |
| 修了年度が正しい | ✅ OK |
| 提出年月が正しい | ✅ OK |
| 専攻名「システムデザイン・マネジメント専攻」 | ✅ OK |
| 日本語要旨のキーワードは日本語 | ✅ OK |
| 英語要旨のキーワードは英語 | ✅ OK |

### 3. Wordサンプル準拠（MastersThesis_sample.docx）

| 要求 | 対応状況 |
|------|----------|
| 表紙レイアウト（修士論文/年度の左右配置） | ✅ OK |
| 日本語要旨（SDM表形式） | ✅ OK |
| 英語要旨（SDM表形式） | ✅ OK |
| 目次 | ✅ OK |
| 図目次 | ✅ OK |
| 表目次 | ✅ OK |
| 見出し1：章（第1章 タイトル） | ✅ OK |
| 見出し2：節（1.1 タイトル） | ✅ OK |
| 見出し3：項（1.1.1 タイトル） | ✅ OK |
| 見出し4：小項（(1) タイトル） | ✅ OK |
| [1]形式の参考文献引用 | ✅ OK |
| クリックで参考文献にジャンプ | ✅ OK |
| 謝辞 | ✅ OK |

---

## ⚠️ 提出前の必須作業

### PDF最適化（KOARA提出要件）

LaTeXで出力したPDFは、提出前に以下の処理が必要です：

1. **Adobe Acrobatで開く**（KIC共用PCで利用可能）
2. **ファイル → その他の形式で保存 → 最適化されたPDF**
3. **プロパティを確認**
   - タイトル：論文タイトル
   - 作成者：慶應義塾大学大学院システムデザイン・マネジメント研究科

---

## フォルダ構造

```
thesis_template/
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
│   ├── 2_literature/               # 第2章：先行研究
│   ├── 3_preliminary/              # 第3章：予備調査
│   ├── 4_proposal/                 # 第4章：提案手法
│   ├── 5_evaluation/               # 第5章：評価実験
│   ├── 6_discussion/               # 第6章：考察
│   └── 7_conclusion/               # 第7章：結論
│
├── backmatter/                     # 後付け
│   └── acknowledgement.tex         # 謝辞
│
└── appendices/                     # 付録
    └── appendixA.tex               # 付録A
```

---

## 見出しスタイル

| レベル | LaTeXコマンド | 出力例 |
|--------|--------------|--------|
| 見出し1 | `\chapter{序論}` | 第1章 序論 |
| 見出し2 | `\section{研究の背景}` | 1.1 研究の背景 |
| 見出し3 | `\subsection{社会受容性}` | 1.1.1 社会受容性 |
| 見出し4 | `\subsubsection{期待と不安}` | (1) 期待と不安 |

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
MobileNet\cite{Howard2017}は、計算量を大幅に削減した。
既存手法\cite{Howard2017, Tan2019}と比較した。
```

### 出力イメージ

> MobileNet[4]は、計算量を大幅に削減した。

**[4]をクリック → 参考文献にジャンプ！**

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
| 表紙が所定フォーマット（修士論文/年度が左右配置） | □ |
| 日本語要旨・英語要旨あり（SDM表形式） | □ |
| 専攻名「システムデザイン・マネジメント専攻」 | □ |
| 修了年度が正しい（2025年3月提出→2024年度） | □ |
| 目次・図目次・表目次あり | □ |
| PDFプロパティ（タイトル・作成者）設定済み | □ |
| キーワードが日本語/英語で正しい | □ |
| 参考文献が[1]形式でジャンプ可能 | □ |
| **PDF最適化済み（Adobe Acrobat）** | □ |

---

## 更新履歴

| バージョン | 日付 | 内容 |
|------------|------|------|
| v1 | - | 初版（enumerate形式） |
| v2 | - | DSR構成に変更 |
| v3 | 2025-12 | bibitem形式、PDFプロパティ追加 |
| **v4** | 2025-12 | 図目次・表目次追加、見出しスタイル4階層対応、SDM要求検証追加 |
