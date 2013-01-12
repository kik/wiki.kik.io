# 単体的複体の実現

有限単体的複体を$\mathbf{R}^d$の中で考えることをその実現という。こうすると位相を考えることができて、ホモロジー群は同相写像で不変になる。この部分の証明は簡単じゃないので、実現のところだけ考える。

## 単体的複体の実現

### 定義($d$次元標準単体)

以下の$\mathbf{R}^{d+1}$の部分集合$\varDelta^d$を$d$次元標準単体と呼ぶ
[\varDelta^d = \\{ (x_0, x_1, \dots, x_d) \in \mathbf{R}^{d+1} | x_0 + \dots x_d = 1, x_i \ge 0 \\}]

### 定義(有限単体的複体の実現)

$V = \\{ v_0, \dots, v_d \\}$を頂点とする有限単体的複体$K$の実現は、$d$次元標準単体の以下で定める部分集合$|K|$のことをいう
[|K| = \bigcup_{\langle v_{i_0}\dots v_{i_\ell} \rangle \in K} \\{ (x_0, x_1, \dots, x_d) \in \varDelta^d | x_{i_0} + \dots + x_{i_\ell} = 1 \\}]

### 定義(位相空間の有限単体分割)

位相空間$X$が、ある有限単体的複体$K$の実現$|K|$と同相のとき、$K$は$X$の単体分割であるという

### 例(簡単な図形)

* [[単体的複体のホモロジー|Math/Homology/drill1]]の簡単な例はみな簡単な図形に対応している

### 例($d$次元球体 $B^d$)

$d$次元球体$B^d = \\{ (x_1, \dots, x_d) \in \mathbf{R}^d | x_1^2 + \dots + x_d^2 \le 1 \\}$の単体分割は

* $V = \\{ v_1, \dots, v_d \\}$
* $K = \\{ \langle v_1 \rangle, \dots, \langle v_d \rangle \\} \cup \dots \cup \\{ \langle v_1\dots v_d \rangle \\}$
* ホモロジーは1点と同じ
* $H_0(K) = R$
* $k \ne 0$のとき$H_k(K) = 0$
* 素直に計算するのは非常に大変なので、本を見るのがよい。

### 例($d$次元球面 $S^d$)

$d$次元球面$S^d = \\{ (x_0, \dots, x_d) \in \mathbf{R}^d | x_0^2 + \dots + x_d^2 = 1 \\}$の単体分割は

* $V = \\{ v_0, \dots, v_d \\}$
* $K = \\{ \langle v_0 \rangle, \dots, \langle v_d \rangle \\} \cup \dots \cup \\{ \langle v_1\dots v_d \rangle, \dots,  \langle v_0\dots v_{d-1} \rangle \\}$
* ホモロジーを計算するには、$d+1$次元球体との相対ホモロジーを使って
* $L = \\{ \langle v_0 \rangle, \dots, \langle v_d \rangle \\} \cup \dots \cup \\{ \langle v_0\dots v_d \rangle \\}$
* $K$は$L$の部分単体的複体だから

$$ H_{d+1}(K) = 0 \xrightarrow{0} H_{d+1}(L) = 0 \xrightarrow{0} H_{d+1}(L, K) = R \xrightarrow{\cong} \\\\
H_{d}(K) \xrightarrow{0} H_{d}(L) = 0 \xrightarrow{0} H_{d}(L, K) = 0 \xrightarrow{0} \\\\
\vdots \\\\
H_{1}(K) \xrightarrow{0} H_{1}(L) = 0 \xrightarrow{0} H_{1}(L, K) = 0 \xrightarrow{0} \\\\
H_{0}(K) \xrightarrow{\cong} H_{0}(L) = R \xrightarrow{0} H_{d}(L, K) = 0
$$

* $d > 0$の場合は
    * $H_{d}(K) = H_{0}(K) = R$
    * $k \ne 0, d$では$H_k(K) = 0$
* $d = 0$の場合は、２点からなる集合になり
    * $H_{0}(K) = R \oplus R$
    * $k \ne 0$では$H_k(K) = 0$
