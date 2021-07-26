# 概要
- resnet18, EfficientNet-b1のアンサンブル
- 今回は本当にたいしたことしていないので、以下に他の方の参考になったソリューションの抜粋をあげておく。

# 参考になったこと
- 画像をpaddingして、絵画の形を保持する(画像の形にも意味がある場合がある)。
- label smoothing
- Augmentationは画質が変わらないものやドメインにあったものを選択する。
- mixup, cutmix
- 複数モデルのstucking
- classficationモデル(各ラベル出力値をsoftmaxして加重平均を取る)
- いろんなモデルを試してみる
- 事前学習にmaterialsやtechniquesのマルチラベル予測を利用(pretrained=Falseの時に考えるべきか)
