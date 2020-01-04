Python を用いての実装を行い、以下の問に対して回答せよ

１ : アトリビュートを確認する

クラス TestClass を作成し、その中にいくつかの変数、関数を定義して dir を用いてそのクラスに存在しているアトリビュートのリストを表記するプログラムを実装せよ

2 : type および isinstance を用いて型の違いを調べる

クラス AClass に対して、下記の変数が存在する際に

a = 1
b = 1.0
c = "1"

それぞれの型を type を用いて表示する関数 printType を実装せよ

3 : プロパティの復習

指定した値の 2 乗の数値を取り扱うクラス Sqr を実装せよ。

コンストラクタ**init**(self, x)では引数として x を受け取り、自身持つアトリビュート\_x に代入を行う。

プロパティとして下記関数の定義を行う。

・def setX(self) : \_x の値を返す
・def getX(self, x) : \_x の値を更新する
・def setSqrX(self) : \_x の 2 乗の値を返す

4 : 型の取り扱い

上記 Sqr の**init**および setX 関数に関して、引数として代入されてきた値が数値でなかった場合、\_x に対して None(何も存在しないことを示す値)を代入するプログラムを実装せよ

5 : 例外処理を行う

線形補間を行う関数 lerp を定義して正しく動いた場合と、例外の発生した場合の動作を検証せよ。

この関数では引数として開始値 a、終了値 b、a と b の補間値 t を定義する。

パラメータ t の動作範囲は 0 から 1 の値で制限されており、この関数は計算結果とメッセージを返すものとする（Python 関数は複数の返り値を指定した場合、タプルで計算結果を返す）

t = 0 の場合は a を返し、メッセージには None を返す。
t = 1 の場合は b を返し、メッセージには None を返す。
t > 0 かつ t < 1 の場合は a から b に t だけ移動した分の値を返し、メッセージには None を返す。
また、なんらかの例外が発生して正しく計算できなかった場合は-1 を返し、それに応じたエラーメッセージを添えて返す。

想定する例外処理として、下記の判定を行う。

・a、b ないしは t に対して、数値以外の値が入ってきた場合は例外を発生させる
・t が 0 から 1 の範囲にない場合は raise を用いて例外を発生させる