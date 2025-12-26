# 実験方法

## データセット

本実験では、独自に構築した「Japanese Domestic Cat Dataset（JDCD）」を使用した。データセットの概要は以下の通りである。

- **総画像数**：15,000枚
- **品種数**：50品種（日本で人気の品種を中心に選定）
- **収集方法**：SNSからの収集（許諾取得済み）、協力家庭からの提供
- **アノテーション**：バウンディングボックス、品種ラベル、個体ID
- **分割**：訓練セット（10,500枚）、検証セット（1,500枚）、テストセット（3,000枚）

個体識別の評価には、サブセットとして100個体（各個体20枚以上）のデータを使用した。

## 比較手法

以下の既存手法との比較を行った。

- YOLOv8-nano：汎用物体検出モデルのベースライン
- YOLOv8-small：中規模モデル
- EfficientDet-D0：効率的なアーキテクチャを持つ検出モデル
- ResNet-50 + Fine-tuning：品種分類のベースライン

## 評価指標

- **検出**：mAP@0.5, mAP@0.5:0.95, Precision, Recall
- **分類**：Top-1 Accuracy, Top-5 Accuracy, F1-Score
- **識別**：Rank-1 Accuracy, Rank-5 Accuracy, mAP
- **実行性能**：FPS（GPU/CPU/Mobile）、モデルサイズ（MB）、メモリ使用量

## 実験環境

- **学習**：NVIDIA RTX 4090、PyTorch 2.0、CUDA 12.0
- **GPU推論**：NVIDIA RTX 4090
- **CPU推論**：Intel Core i9-13900K
- **モバイル推論**：iPhone 14 Pro（A16 Bionic）、Pixel 7（Google Tensor G2）
