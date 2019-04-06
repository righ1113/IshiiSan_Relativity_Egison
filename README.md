# IshiiSan_Relativity_Egison
『一般相対性理論を一歩一歩数式で理解する』読書ノート  

# 変更履歴
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


# 第2章　物理の準備

# 第3章　テンソルと直線座標のテンソル場

# 第4章　特殊相対性理論

# 第5章　曲線座標のテンソル場

# 第6章　曲率

# 第7章　一般相対性理論




