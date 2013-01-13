# ホモロジー計算ドリル(4)

特異ホモロジーを使うと任意の位相空間に対してホモロジーが定義できる。その代わり定義から直接計算するのは難しい。

## 特異ホモロジー

以下、$X$を位相空間とする。

### 定義(特異単体)

正整数$k$にたいして、連続写像$\sigma : \varDelta^k \to X$を$X$の特異$k$単体と呼ぶ。

* 潰れていてもよい
* $k > 0$, $0\le j \le k$にたいして、$\varepsilon^j : \varDelta^{k-1} \to \varDelta^{k}$を以下で定める

$$\varepsilon^0(x_1, \dots, x_k) = (0, x_1, \dots, x_k) \\\\
\varepsilon^1(x_1, \dots, x_k) = (x_1, 0, x_2, \dots, x_k) \\\\
\vdots \\\\
\varepsilon^k(x_1, \dots, x_k) = (x_1, \dots, x_k, 0)$$

### 定義(特異鎖加群)

整数$k$にたいして、特異鎖加群$S_k(X)$を特異$k$単体の生成する自由$R$加群とする。

$$ S_k(X) = \bigoplus_{\sigma : \text{特異}k\text{単体}} R\sigma$$

で定める。$k < 0$のときは$S_k(X) = 0$とする

* 自然な対応付けではないが、特異$k$単体は少なくとも潰れた$k+1$単体ともみなせるので、$S_k(X) \subset S_{k+1}(X)$のように単調増大していくことに注意。これも直接の計算を難しくしている。

### 定義(境界準同型)

$R$準同型$\delta_k : S_k(X) \to S_{k-1}(X)$を生成元$\sigma$の像を以下で指定して定義し境界準同型とよぶ。

$$ \sigma \mapsto \sum_{j=0}^k (-1)^j \sigma\circ\varepsilon^j $$

ただし、$k \le 0$の場合は$\delta_k = 0$とする。

* $\delta_{k-1}\circ\delta_k = 0$

### 定義(一般の複体)

$R$加群の列$(T_k)_{k\in\mathbf{Z}}$と$R$準同型の列$(\delta_k : T_k \to T_{k-1})_{k\in\mathbf{Z}}$の組が以下を満たすとき(左)複体とよぶ。

$$\delta_{k-1}\circ\delta_k = 0$$
$$T_k = 0\quad (k < 0)$$

* 特異鎖加群の列と境界準同型の対$S(X) = (S_k(X), \delta_k)$は複体になる

$\DeclareMathOperator{\Ima}{Im}
\DeclareMathOperator{\Ker}{Ker}
$

### 定義(複体のホモロジー)

複体$T = (T_k, \delta_k)$にたいして、$k$次ホモロジー加群$H_k(T)$を以下で定める。

[H_k(T)=\Ker{\delta_k}/\Ima{\delta_{k+1}}]

* 位相空間$X$のの特異複体のホモロジーを特異ホモロジー$H_k(X)$とよぶ

[H_k(X) = H_k(S(X))]

