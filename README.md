# IshiiSan_Relativity_Egison
『一般相対性理論を一歩一歩数式で理解する』読書ノート  

# 変更履歴
19/06/11　一休み中  
19/05/05　「第3章　テンソルと直線座標のテンソル場」  
　　　　　　「第4章　特殊相対性理論」読書中  
19/04/13　「第2章　物理の準備」読書中  
19/04/04　「第1章　数学の準備」読書中  

# ゴール
- 法則7.10　アインシュタインの重力場方程式  
　　G_i_j = (8πG/c^4)T_i_j  
を理解（導出？）する  

# Egison
Egisonで計算しながら読書を進める。  
Egisonは数式処理ができる。また、テンソルも扱える。  

# Jupyter良いかも
- 分数とか行列とかをきれいに表示してくれる。  
- 入れ方は<a href="https://github.com/egison/egison_kernel" target="_blank">公式</a>を参照してください。  
「Jupyter's CodeMirror directory」とは、`> jupyter notebook`を叩くフォルダです。  
- Windowsだと動かなかった。Linux(VirtualBox使用)で動いた。  

# 第1章　数学の準備
## 1 ベクトル積
## 2 微分の公式
## 3 3次元の座標変換
## 4 スカラー場、ベクトル場のイメージ
## 5 勾配
## 6 発散
## 7 回転
## 8 勾配、発散、回転の公式
- Egisonで  
公式1.21「rot grad f(**x**) = **0**」  
公式1.22「div rot **A**(**x**) = 0」  
を計算した。  
```egison
> (load "sample\\math\\geometry\\vector-analysis.egi")
> (rot (grad f))
[| [| 0 0 0 |] [| 0 0 0 |] [| 0 0 0 |] |]
> (div (rot A))
0
```

## 9 ポテンシャル
## 10 スカラー場の線積分
## 11 ベクトル場の線積分
## 12 曲面の面積
## 13 ベクトル場の面積分
## 14 逆2乗法則についての計算
## 15 波動方程式
## 16 ポアソン方程式
## 17 変分法
## 18 アインシュタインの縮約記法

# 第2章　物理の準備
## 1 ニュートンの重力場方程式
## 2 応力テンソル
- う～ん……
- 応力テンソルは、連続体内部に定義した微小面積に作用する  
単位面積あたりの力　で定義される。（Wikipediaより）  
- 応力テンソルは、3次元デカルト座標の下では、3*3行列で表される。  

## 3 流体の基礎方程式
## 4 クーロンの法則の書き換え
- クーロンの法則  
- アンペールの法則  
- ファラデーの法則  
  - ローレンツ力  

を、マックスウェルの方程式にまとめる。  
div**E**(**x**, t) = ρ(**x**, t)/ε_0  
rot**E**(**x**, t) + ∂**B**(**x**, t)/∂t = **0**  
div**B**(**x**, t) = 0  
rot**B**(**x**, t) - ε_0 * μ_0 * ∂**E**(**x**, t)/∂t = μ_0 * **i**  

## 5 静電場のエネルギー
## 6 アンペールの法則の書き換え
## 7 ファラデーの電磁誘導の法則の書き換え
> ローレンツ力は、動いている電荷に対して垂直な方向に力がかかります。  
> それでは、動いている電荷と同じ速度を持つ観測者からは、どう見えるでしょうか？  
> 同じ速度を持っている観測者にとって、電荷は静止しているように見えます。  
> ですから、観測者が同じ物理法則を適用するとすれば、  
> ローレンツ力は生じないはずです。これは矛盾です。  
> あとで見るように特殊相対論は、この矛盾をクリアに解決してくれます。  

## 8 電磁波
## 9 静磁場エネルギー
## 10 マックスウェルの応力テンソル
## 11 マックスウェルの方程式をポテンシャルで書き換え

# 第3章　テンソルと直線座標のテンソル場
さっぱりだ～  
後から戻ってくる感じかな  

# 第4章　特殊相対性理論
```idris
・ローレンツ変換をやる
・ミンコフスキー空間をやる
・力学をやる
・電磁場をやる
```

## 1 方程式の共変性
## 2 特殊相対論の課題
## 3 ローレンツ変換とダランベルシアン
## 4 ローレンツ変換の導出
## 5 ローレンツ収縮の対等性
## 6 一般の速度のローレンツ変換
## 7 ミンコフスキー空間
## 8 速度・加速度の変換則
## 9 速度の4元化
## 10 固有時
## 11 4元加速度、4元力
## 12 力学的なエネルギー・運動量テンソル
## 13 マックスウェルの方程式の4元化
## 14 ローレンツ力の共変性
> 慣性系S'がSに対してx方向に速度Vで動いているとし（電荷も）、
> Sではz軸方向に磁場**B**があり、電場はないものとします。  
> このとき、S'に対して静止している電荷q（>0）は、  
> S、S'から見てどのように見えるでしょうか。  

Sから見ると、F_x = 0、F_y = -qVB、F_z = 0　です。  

S'の電磁場で、B_zが出てくる成分は、  
E'_y = -γVB、　B'_z = γB　です。  

電荷に働く力F'をS'で見ると、**F**' = q(**E**' + **0** × **B**')　なので、  
F'_x = 0、　F'_y = -γqVB、　F'_z = 0  
となります。  

速度VがS'の電場にあらわれるわけですね。  

## 15 電磁場のエネルギー・運動量テンソル

# 第5章　曲線座標のテンソル場

# 第6章　曲率

# 第7章　一般相対性理論




