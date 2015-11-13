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

# クイック・スタート・ガイド
当文書は視覚障害者ナビゲーション支援を提供する方々向けに書かれています。
当文書にはiPhoneとiBeaconを用いた屋内ナビゲーションを実現するための**ナビゲーション用地図**の作成方法が書かれています。


## 準備するもの
ナビゲーション用地図の作成にあたり、以下の機器等を事前に準備ください。

0. Mac PC
0. iPhone 6 もしくは、それ以降
0. NavCogアプリ　（[App Store](https://itunes.apple.com/WebObjects/MZStore.woa/wa/viewSoftware?id=1042163426&mt=8)よりダウンロードください）
0. Bluetooh LEビーコン ([補遺](appendix.md#beacon))
0. 対象フロアマップ画像 (optional)
0. フィート目盛のある巻尺、粘着テープ


## ナビゲーション用地図作成の概要
NavCogアプリはビーコンからのBluetooth信号を利用してユーザの位置を推定します。
以下の手順で、簡単にナビゲーション用地図を作成することができます。

1.	対象エリアおよび案内ルートを決定する([Sec. 2](map.md))
2.	ルート周辺にビーコンを配置する([Sec. 3](beacon.md))
3.	位置推定のための **基準測定**([*1](#footnote1)) データを収集する ([Sec. 3](beacon.md#fingerprinting))
4.	ナビゲーション用地図データをエクスポートする ([Sec. 2](map.md#export_map))
5.	ナビゲーション用地図をテストする ([Sec. 4](test.md))
6.	ナビゲーション用地図を登録・公開する ([Sec. 4](test.md#submit_map))
7.	対象エリアで視覚障害者にNavCogアプリを使ってもらう([Sec. 5](navcog.md))

# 目次

1. はじめに (当文書)
2. [ナビゲーション用地図の作成](map.md)
3. [ビーコン設置と基準測定](beacon.md)
4. [ナビゲーション用地図のテスト](test.md)
5. [NavCogユーザー・ガイド](navcog.md)
6. [補遺](appendix.md)

<a name="footnote1">*1</a>: 正確な位置を把握した上でビーコン信号強度を計測すること
