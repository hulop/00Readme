<!--
The MIT License (MIT)

Copyright (c) 2014, 2015 IBM Corporation
Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
-->


# 補遺


## <a name="transition"></a>ノードの遷移

**遷移**とは、ナビゲーション用地図上のノードからノードへの遷移を意味します。
**遷移**は、階段、エレベーター、入り口の二重扉など、視覚障害ユーザが構造物を容易に理解でき、案内がなくても問題なく移動できるような場所に利用します。（特にビーコンの信号が届きにくい構造の場所での利用を推奨します）

ユーザが構造物に沿って向かうべき先の情報を遷移元のノードに記述しておく必要があります。（エレベーターで何階を選択すべきなのか、いくつ扉を開ければよいのか、など）

また、エッジ情報に`最大knnDist`、`最小knnDist`の値を、 ノード情報に`対象knn距離`と `位置`の値を、それぞれ設定しておく必要があります。


### <a name="knnDist"></a>knn距離

遷移ノードを利用する場合は、最大knn距離と最小knn距離を遷移直後のエッジに登録する必要があります。

最大knn距離と最小knn距離に設定すべき値は、[精度評価](beacon.md#acc_eval)の結果ファイルに出力されます。
オンライン地図エディタで、それらの値をエッジに入力してください。


## ビーコンのタイプ

ビーコンにはいくつかのタイプがあります。例えば、バッテリー型、USB電源型、防水型、LED照明埋め込み型、など。

タイプ | 利点 | 欠点
---|---|---
バッテリー|最も普及しているタイプ、値段も高くない|バッテリーの交換が必要
USB電源|メンテナンスが不要|電源タップが必要、高価
防水|屋外に設置可能|通常バッテリー型、高価
LED照明埋め込み|メンテナンスが不要|ソケットが必要、高価

##BLEビーコンのプロトコル

2015年10月時点でBLEビーコンのプロトコルは以下の三種類があります。現時点で、NavCogはiBeaconのみをサポートしています。

* [iBeacon (Apple)](https://developer.apple.com/ibeacon/)
* [EddyStone (Google)](https://developers.google.com/beacons/?hl=en)
* [AltBeacon (Radius Network)](http://altbeacon.org)
