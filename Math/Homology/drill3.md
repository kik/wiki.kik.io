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

### 例($d$次元球面 $S^d$)

$d$次元球面$S^d = \\{ (x_0, \dots, x_d) \in \mathbf{R}^d | x_0^2 + \dots + x_d^2 = 1 \\}$の単体分割は

* $V = \\{ v_0, \dots, v_d \\}$
* $K = \\{ \langle v_0 \rangle, \dots, \langle v_d \rangle \\} \cup \dots \cup \\{ \langle v_1\dots v_d \rangle, \dots,  \langle v_0\dots v_{d-1} \rangle \\}$
