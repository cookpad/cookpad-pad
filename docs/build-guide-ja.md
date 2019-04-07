# Cookpad Pad ビルドガイド

## パーツリスト

![](https://raw.githubusercontent.com/cookpad/cookpad-pad/master/docs/images/bg-items.jpg)

名称 | 数量
-- | --
基板 | 1
スイッチプレート | 1
ボトムプレート | 1
Pro Micro | 1
ダイオード（1N4148） | 6
タクトスイッチ | 1
スペーサー（M2 5mm） | 4
ねじ（M2 4mm） | 8
キースイッチ | 6
キーキャップ | 6

## ファームウェア

Cookpad Pad のファームウェアは、まだ QMK 本体に含まれていません。フォークしたリポジトリをつかってください。手順は下記の通りです。

```
$ git clone git@github.com:qmk/qmk_firmware.git
$ git remote add takai git@github.com:takai/qmk_firmware.git
$ git fetch takai
$ git checkout -t takai/cookpad-pad
```

ファームウェアのビルドと書き込みは、下記コマンドになります。

```
$ make cookpad_pad:default:avrdude
```

## 組み立て手順

### ダイオードのはんだ付け

ダイオードの足を曲げて取り付け、はんだ付けをします。ダイオードは表面から取り付け、裏面からはんだ付けをします。ダイオードには極性がありますので、方向に注意してください。黒い帯がある方向がカソードです。この帯が左を向くように取り付けをします。

![](https://raw.githubusercontent.com/cookpad/cookpad-pad/master/docs/images/bg-step1-1.jpg)

このとき、写真のようにマスキングテープでダイオードを固定すると、裏返したときにも位置がずれたりすることがなく、はんだ付け作業をしやすくなります。

![](https://raw.githubusercontent.com/cookpad/cookpad-pad/master/docs/images/bg-step1-2.jpg)

はんだ付けがおわったら、ニッパーで余分な足を切ります。この段階でテスターで取り付け方向が間違っていないかを確認することをおすすめします。

![](https://raw.githubusercontent.com/cookpad/cookpad-pad/master/docs/images/bg-step1-3.jpg)

### ピンヘッダのはんだ付け

Pro Micro の袋からピンヘッダを取り出し、裏面にピンヘッダを取り付け、表面からはんだ付けをします。

![](https://raw.githubusercontent.com/cookpad/cookpad-pad/master/docs/images/bg-step2-1.jpg)

写真のようにブレッドボードを利用すると簡単にはんだ付けができます。しかし、はんだの高熱でブレッドボードが溶ける可能性があるため、推奨されるやり方ではないとのことです。

![](https://raw.githubusercontent.com/cookpad/cookpad-pad/master/docs/images/bg-step2-2.jpg)

### Pro Microの取り付け

先ほど取り付けたピンヘッダにプロマイクロを配置し、そこからはみ出した余分なピンヘッダのピンをニッパーで切り落します。

![](https://raw.githubusercontent.com/cookpad/cookpad-pad/master/docs/images/bg-step3-1.jpg)

次に、 Pro Micro をはんだ付けします。

### リセットスイッチのはんだ付け

リセットスイッチを裏面に取り付け、表面からはんだ付けをします。

![](https://raw.githubusercontent.com/cookpad/cookpad-pad/master/docs/images/bg-step4.jpg)

### スペーサーの取り付け

スペーサーを4ヶ所に取り付け、ねじで固定します。このねじは後から締め直すのが難しいので、しっかりと締めるようにしてください。

![](https://raw.githubusercontent.com/cookpad/cookpad-pad/master/docs/images/bg-step5-1.jpg)

![](https://raw.githubusercontent.com/cookpad/cookpad-pad/master/docs/images/bg-step5-2.jpg)


### キースイッチのはんだ付け

スイッチプレートの保護紙をはがし、キースイッチをプレートに固定します。無理に力を加えるとプレートが割れてしまうため、十分に注意をしながら作業をしてください。

![](https://raw.githubusercontent.com/cookpad/cookpad-pad/master/docs/images/bg-step6-1.jpg)

キースイッチが固定できたら、スイッチプレートを基板の表側から取り付けます。このときに曲がった足があると、うまく取り付けることができなくなってしまいますので、取り付け前に確認をしてください。

![](https://raw.githubusercontent.com/cookpad/cookpad-pad/master/docs/images/bg-step6-2.jpg)

その後、全てのキースイッチをはんだ付けします。

![](https://raw.githubusercontent.com/cookpad/cookpad-pad/master/docs/images/bg-step6-3.jpg)

### ボトムプレートの取り付け

ボトムプレートを取り付け、ねじで固定します。

![](https://raw.githubusercontent.com/cookpad/cookpad-pad/master/docs/images/bg-step7-1.jpg)

その後、クッションゴムを取り付けてください。

![](https://raw.githubusercontent.com/cookpad/cookpad-pad/master/docs/images/bg-step7-2.jpg)

### キーキャップの取り付け

キーキャップを付ければ完成です。

![](https://raw.githubusercontent.com/cookpad/cookpad-pad/master/docs/images/bg-step8.jpg)
