課題１
実装するための設計としては、以下を考えました。

1. まず、1-004-2.jpg の右端上の画像(本実装の test.png)を取得する。
2. test.png と 1-004-1.jpg を用いてテンプレートマッチングのアルゴリズムの SSD(Sum of Absolute Difference) を用いて、test.png をどれだけのベクトル量を平行移動させると、1-004-1.jpg とよく一致するかを計算する。
3. 手順 2 で求めた移動させるべき移動量に従って、変換行列を求める。
4. 1-004-2.jpg を変換行列を使って平行移動させた画像と 1-004-1.jpg を重ね合わせると、求めるべきパノラマ画像(ans.png)を取得できる。

プログラムの説明に関しては、ソースコードにコメントを記載していますので、そちらを参照して下さい。

課題２
実装方法を思いつかなかったので、実装していません。
実装するための設計としては、以下を考えました。

1. 2-004-2.jpg 回転している傾きを計算して、元にもどす。
2. 課題１と同様にテンプレートマッチングを行い、2-004-2.jpg をどれだけ平行移動させると、2-004-1.jpg と重なりパノラマ画像を生成できるかを計算する。

この 1 を実装するにあたり、考えたことが 1 つあります。それは、画像の家と草のエッジから 2-004-2.jpg の画像が 2-004-1.jpg と比較してどれだけ回転しているかを求める方法です。この手法では、この画像でしか対応できない汎用性の低い設計となってしまうので行き詰まりました。

参考
https://github.com/dilmnqvovpnmlib/MultimediaSignalAnalysis/tree/master/lecture_3