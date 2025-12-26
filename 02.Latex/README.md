# 博士論文 LaTeX テンプレート

慶應義塾大学大学院 システムデザイン・マネジメント研究科（SDM）向けの博士論文テンプレートです。

## コンパイル方法

Overleafを使用する場合は、XeLaTeXでコンパイルしてください。

```
Menu → Compiler → XeLaTeX
```

## フォルダ構造

```
thesis/
├── main.tex                    # メインファイル（これをコンパイル）
├── refs.tex                    # 参考文献
├── README.md                   # このファイル
│
├── frontmatter/                # 前付け
│   ├── titlepage.tex           # 表紙
│   ├── abstract.tex            # 日本語要旨
│   └── abstract-en.tex         # 英語要旨（Abstract）
│
├── chapters/                   # 本文
│   ├── 0_intro/                # 序章
│   │   ├── 0_1_problem.tex     # 問題意識
│   │   ├── 0_2_objectives.tex  # 本研究の目的
│   │   └── 0_3_structure.tex   # 本論文の構成
│   │
│   ├── 1_slr/                  # 第1章（体系的文献レビュー）
│   │   ├── 1_1_purpose.tex     # 目的
│   │   ├── 1_2_method.tex      # 方法
│   │   ├── 1_3_result.tex      # 結果
│   │   ├── 1_4_findings.tex    # 発見
│   │   └── 1_5_summary.tex     # 本章のまとめ
│   │
│   ├── 2_mtl/                  # 第2章（設計と評価）
│   │   ├── 2_1_methodology.tex # 研究方法論
│   │   ├── 2_2_bma.tex         # ビジネス分析
│   │   ├── 2_3_1_strs.tex      # 利害関係者要求（StRS）
│   │   ├── 2_3_2_syrs.tex      # システム要求（SyRS）
│   │   ├── 2_4_ad.tex          # アーキテクチャ設計
│   │   ├── 2_5_dd.tex          # 詳細設計
│   │   ├── 2_6_impl.tex        # 実装
│   │   ├── 2_7_eval.tex        # 評価
│   │   └── 2_8_summary.tex     # 本章のまとめ
│   │
│   ├── 3_discussion/           # 第3章（総合考察）
│   │   ├── 3_1_summary.tex     # 研究成果の要約
│   │   ├── 3_2_academic.tex    # 学術的貢献
│   │   ├── 3_3_practical.tex   # 実務的貢献
│   │   ├── 3_4_limitations.tex # 限界
│   │   └── 3_5_future.tex      # 将来研究
│   │
│   └── conclusion.tex          # 結論
│
├── backmatter/                 # 後付け
│   └── acknowledgement.tex     # 謝辞
│
└── appendices/                 # 付録
    ├── appendixA.tex           # 付録A
    ├── appendixB.tex           # 付録B
    └── appendixC.tex           # 付録C
```

## 各ファイルの役割

### main.tex
論文全体の構造を定義するメインファイル。パッケージの読み込み、章立て、\input コマンドによる各ファイルの読み込みを行う。

### frontmatter/
- **titlepage.tex**: 表紙（論文題目、所属、氏名、指導教員、提出年月）
- **abstract.tex**: 日本語要旨（SDM形式の枠線付きフォーマット）
- **abstract-en.tex**: 英語要旨（SDM形式の枠線付きフォーマット）

### chapters/
本文を章・節ごとに分割して管理。ファイル名の数字はmain.texでの読み込み順序に対応。

### backmatter/
- **acknowledgement.tex**: 謝辞

### appendices/
付録資料。必要に応じて追加・削除可能。

## 編集のヒント

1. **各章を独立して編集**: chaptersフォルダ内のファイルを個別に編集することで、コンフリクトを避けやすくなります。

2. **図表の追加**: figuresフォルダを作成し、`\includegraphics{figures/xxx.pdf}` で読み込むことを推奨します。

3. **参考文献**: refs.texを直接編集するか、BibTeXを使用する場合は別途.bibファイルを作成してください。

## 注意事項

- 日本語フォントはIPAexMincho/IPAexGothicを使用しています
- Overleaf以外の環境では、フォント設定の変更が必要な場合があります
