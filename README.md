
## ■検証内容
以下、三種類のモデルの作成を行いパフォーマンス比較を実施した。
- Kerasのsequantialを利用してシンプルな犬猫分類モデルを構築した。学習データは犬と猫の画像、合計1560枚を使用。
- 学習データを14000枚まで増やし、同モデルのパフォーマンス向上有無の確認を行った。
- 学習済みモデルVGG16を使って転移学習を行うことでより少ない学習データ(160枚)で一定の精度を出せるか確認を行った。

## ■検証結果
1. シンプル構成
- Testスコア81.3％のモデルを作成することができた。14000枚で追加検証を実施、87.4%と更なる精度向上を達成できた。
2. VGG16転移学習モデル
- シンプル構成の約1/10の学習データでほぼ同等のパフォーマンスを得ることができた。学習データを増やすことでOver Fit(過学習)を低減させ、より高い精度の実現が見込まれる。

  ![img](https://github.com/tkshim/Picture/blob/master/keras_performance_hikaku.png)

## ■結論
- 学習データが少ない段階においては、転移学習を利用することが一つのソリューションとなり得る。
- 学習データの収集が進んだ段階においては、スクラッチからモデルを構築した方がより高い精度を実現できるケースもあり、双方を比較検討する余地が残る。
