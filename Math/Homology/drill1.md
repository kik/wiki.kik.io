# ホモロジー計算ドリル(1)

ホモロジーの計算がガンガンできるようになるためのドリルなので、無駄に計算ばかりする予定。本によって内容の順序が大幅に変わるのだけれども、計算を重視して並べたい予定。

## 単体的複体のホモロジー

$\mathbf{R}^d$の部分集合として単体的複体を定義することもできるけど、純粋に組み合わせ論的に書いたほうが向き付けとか考えなくていいし計算練習だけなら何も問題ないと思う。あと有限じゃない場合も考えなくてもいいと思われる。坪井先生の講義からもってくたのを一行で書くことにする。

### 定義(有限単体的複体)
 
有限全順序集合$V$を頂点とする有限単体的複体とは、$V$の部分集合で空でないものからなる族$K$で、任意の$S\in K$の空でない部分集合が$K$の元であることをいう。

* $k$を整数として、$\sigma\in K$が$\\#\sigma = k+1$を満たすとき、$\sigma$を$K$の$k$単体という。
* $k$単体$\sigma$は単調増大する組$(v_0, \dots, v_k)$を使って、$\sigma=\\{ v_0, \dots, v_k \\}$と一意にあらわせるので、これを$\langle v_0\dots v_k\rangle$と書く。
* $k$を$\langle v_0\dots v_k\rangle$の次元という。
* $K$の元の次元の最大値を$K$の次元といい、$\dim{K}$と書く

以下、$R$を環とする。

### 定義(有限単体的複体の鎖複体)

$K$が有限単体的複体のとき、その$k$次元鎖複体$C_k(K)$とは、$K$の$k$単体全体の生成する自由$R$加群のことをいう。
[C_k(K) = \bigoplus_{\\#\sigma = k+1} R\sigma]

### 定義(境界準同型)

$R$準同型$\delta_k : C_k(K)\to C_{k-1}(K)$を生成元$\langle v_0\dots v_k\rangle$の像を以下で指定して定義し境界準同型とよぶ。
[\langle v_0 \rangle\mapsto 0 \ \ (k = 0)]
[\langle v_0\dots v_k\rangle\mapsto \sum_{i=0}^k(-1)^i\langle v_0\dots\check{v_i}\dots v_k\rangle \ \ (k > 0)]

$\DeclareMathOperator{\Ima}{Im}
\DeclareMathOperator{\Ker}{Ker}
$

### 定義(有限単体的複体のホモロジー)

$K$の$k$次ホモロジー$H_k(K)$を以下で定める
[H_k(K)=\Ker{\delta_k}/\Ima{\delta_{k+1}}]

### 例(1点のみからなる場合)

* $V = \\{ v_0 \\}$
* $K = \\{ \langle v_0 \rangle \\}$
* $C_0(K) = R\langle v_0 \rangle$。$k\ne 0$のとき$C_k(K) = 0$
* $\delta_k = 0$
* $\Ima \delta_1 = 0$
* $\Ker \delta_0 = C_0(K)$
* $H_0(K) = R\langle v_0 \rangle$。$k\ne 0$のとき$H_k(K) = 0$

### 例($n+1$点のみからなる場合)

* $V = \\{ v_0, \dots, v_n \\}$
* $K = \\{ \langle v_0 \rangle, \dots, \langle v_n \rangle \\}$
* $C_0(K) = R\langle v_0 \rangle \oplus \dots \oplus R\langle v_n \rangle$
* $k\ne 0$のとき$C_k(K) = 0$
* $\delta_k = 0$
* $\Ima \delta_1 = 0$
* $\Ker \delta_0 = C_0(K)$
* $H_0(K) = R\langle v_0 \rangle \oplus \dots \oplus R\langle v_n \rangle$
* $k\ne 0$のとき$H_k(K) = 0$

### 例(線分のみからなる場合)

* $V = \\{ v_0, v_1 \\}$
* $K = \\{ \langle v_0 \rangle, \langle v_1 \rangle\\} \cup \\{\langle v_0v_1 \rangle\\}$
* $C_0(K) = R\langle v_0 \rangle \oplus R\langle v_1 \rangle$
* $C_1(K) = R\langle v_0v_1 \rangle$
* $k\ne 0, 1$のとき$C_k(K) = 0$
* $\delta_1(\langle v_0v_1 \rangle) = \langle v_1 \rangle - \langle v_0 \rangle$
* $\Ker \delta_0 = C_0(K)$
* $\Ima \delta_1 = R(\langle v_1 \rangle - \langle v_0 \rangle)$
* $\Ker \delta_1 = \\{ x \langle v_0v_1 \rangle | x\langle v_1 \rangle - x\langle v_0 \rangle = 0 \\} = \\{ x \langle v_0v_1 \rangle | x = 0 \\} = 0$
* $\Ima \delta_2 = 0$
* $H_0(K) = (R\langle v_0 \rangle \oplus R\langle v_1 \rangle) / R(\langle v_1 \rangle - \langle v_0 \rangle) = R\langle v_0 \rangle$
* $H_1(K) = 0 / 0 = 0$
* $k\ne 0, 1$のとき$H_k(K) = 0$
* 1点の場合と同じ

### 例($n$本の線分がまっすぐ繋がっている場合)

* $V = \\{ v_0, \dots, v_n \\}$
* $K = \\{ \langle v_0 \rangle, \dots, \langle v_n \rangle \\} \cup \\{ \langle v_0v_1 \rangle, \dots, \langle v_{n-1}v_n \rangle\\}$
* $C_0(K) = R\langle v_0 \rangle \oplus \dots \oplus R\langle v_n \rangle$
* $C_1(K) = R\langle v_0v_1 \rangle \oplus \dots \oplus R\langle v_{n-1}v_n \rangle$
* $\delta_1(\langle v_0v_1 \rangle) = \langle v_1 \rangle - \langle v_0 \rangle$
*  ...
* $\delta_1(\langle v_{n-1}v_n \rangle) = \langle v_n \rangle - \langle v_{n-1} \rangle$
* $\Ker \delta_0 = C_0(K)$
* $\Ima \delta_1 = R(\langle v_1 \rangle - \langle v_0 \rangle) + \dots + R(\langle v_n \rangle - \langle v_{n-1} \rangle)$
* $\Ker \delta_1 = \\{ x_1 \langle v_0v_1 \rangle + \dots + x_n \langle v_{n-1}v_n \rangle | (x_1\langle v_1 \rangle - x_1\langle v_0 \rangle) + \dots + (x_n\langle v_n \rangle - x_n\langle v_{n-1} \rangle) = 0 \\}$
    * 条件の部分は
    * $-x1 = 0$
    * $x2-x1 = 0$
    * ...
    * $x_n-x_{n-1} = 0$
    * $x_n = 0$
    * なので係数は全部$0$
* $\Ker \delta_1 = 0$
* $\Ima \delta_2 = 0$
* $H_0(K) = (R\langle v_0 \rangle \oplus \dots \oplus R\langle v_n \rangle) / (R(\langle v_1 \rangle - \langle v_0 \rangle) + \dots + R(\langle v_n \rangle - \langle v_{n-1} \rangle)) = R\langle v_0 \rangle$
* $H_1(K) = 0 / 0 = 0$
* $k\ne 0, 1$のとき$H_k(K) = 0$
* 1点の場合と同じ
