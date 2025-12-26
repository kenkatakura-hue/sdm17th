# 評価

提案手法の評価結果について述べる。

## 評価指標

- 認識精度：mAP@0.5, mAP@0.5:0.95
- 処理速度：FPS（Frames Per Second）
- モデルサイズ：パラメータ数、ファイルサイズ

## 比較手法

YOLOv8-nano、MobileNet-SSD、EfficientDet-D0を比較対象とした。

## 結果

| 手法 | mAP@0.5 | FPS | サイズ |
|------|---------|-----|--------|
| YOLOv8-nano | 82.1% | 45 | 6.3MB |
| MobileNet-SSD | 78.4% | 52 | 8.1MB |
| EfficientDet-D0 | 85.3% | 28 | 15.2MB |
| **NekoNet** | **92.6%** | **48** | **7.8MB** |

NekoNetは全ての比較手法を上回る精度を達成しつつ、処理速度も30FPS以上の要求を満たした。

## 統計的検定

McNemar検定の結果、NekoNetと各比較手法の間に有意差が認められた（p < 0.01）。
