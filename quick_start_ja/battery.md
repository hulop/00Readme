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


# 電池駆動型ビーコンを使用する際の注意事項 
Bluetoothビーコンは一般的に電池またはUSB電源を使用します。 
電池駆動型ビーコンは設置の柔軟性が高いことで多くの場所に採用されています。
しかし長期間(２ヶ月以上)の設置を行う場合、電池の残量に気を使う必要があります。
電池維持コストを最小限にするための以下の情報を参考にしてください。

## 電池容量
一般的な3V電源を使用するビーコンの電池の種類および容量は以下のようになります。容量が大きいほど電池寿命が長くなります。

| 電池の種類 | 容量 |
|---------------------|---------|
| 1 x CR2477 (リチウム)| 1000mAh |
| 2 x 単三 (アルカリ)   | 2000mAh - 2700mAh (製造メーカーに依存) |
| 2 x 単三 (リチウム)    | 3000mAh | 

単三リチウム電池を使用するビーコンはCR2477電池を使用するビーコンと比べて３倍の電池寿命をもつことになります

寒い環境においてはアルカリ電池よりリチウム電池の使用が適しています。

## ビーコン設定と電池寿命
電池の寿命は送信間隔と電波出力設定に大きく依存します。

送信間隔100msの場合の電池消費は送信間隔200msの場合の約２倍です。
電波出力を大きくすることも電池を多く消費することになります。

送信間隔の値はビーコン精度にとって重要でありユーザー体験にも影響を与えます。
ビーコンベンダーに最適な設定条件を問い合わせてください。

## 電池残量の確認方法
* LED表示
 * 電池残量を表示するためのLEDを装備し、電池残量が基準レベル以下になるとLED表示が切り替わるビーコンがあります。詳細はビーコン販売元に問い合わせてください。
* ビーコン管理ツール
 * 専用のソフトウェアを使用して電池残量を確認できるビーコンがあります。詳細はビーコン販売元に問い合わせてください。 
* 電圧計
 * 上記の方法で電池残量確認ができない場合はビーコンから電池を取り出して電圧を測定する必要があります。
* RSSIレベル測定  
 * 電池を取り出すのが極めて困難な場合は汎用のビーコンチェックツール、例えばBeacon Ranging (https://itunes.apple.com/jp/app/beacon-ranging/id734155067) 等を使用してビーコンのRSSIレベルを測定することで電池寿命の尽きたビーコン(通常単三電池で0.7V以下)を確認をすることができます。ただし、この方法で異常が検出されるのはすでに手遅れ状態なので、電池寿命が尽きる前の電池交換をお勧めします。

## いつ電池を交換すべきか?
ビーコンがまだ動いていたとしても、以下の電池切れ電圧以下になったら電池交換を行うことをお勧めします。

| 電池の種類 | 電池切れ電圧 |
|--------|------|
| CR2477 | 2.0V |
| 単三電池 | 1.0V |

電池切れ状態でアルカリ電池を放置すると液漏れの恐れがあります。
