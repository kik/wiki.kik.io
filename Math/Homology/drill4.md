# ホモロジー計算ドリル(4)

特異ホモロジーを使うと任意の位相空間に対してホモロジーが定義できる。その代わり定義から直接計算するのは難しい。

## 特異ホモロジー

以下、$X$を位相空間とする。

### 定義(特異単体)

正整数$k$にたいして、連続関数$\sigma : \varDelta^k \to X$を$X$の特異$k$単体と呼ぶ。

* 潰れていてもよい
* $0\le j \le k$にたいして、$\varepsilon^j : \varDelta^{k-1} \to \varDelta^{k}$を以下で定める

$$\varepsilon^0(x_1, \dots, x_k) = (0, x_1, \dots, x_k) \\\\
\varepsilon^1(x_1, \dots, x_k) = (x_1, 0, x_2, \dots, x_k) \\\\
\vdots \\\\
\varepsilon^k(x_1, \dots, x_k) = (x_1, \dots, x_k, 0)$$

### 定義(特異鎖加群)

整数$k$にたいして、特異鎖加群$S_k(X)$を特異$k$単体の生成する自由$R$加群とする。

$$ S_k(X) = \bigoplus_{\sigma : \text{特異}k\text{単体}} R\sigma$$

で定める。$k < 0$のときは$S_k(X) = 0$とする
