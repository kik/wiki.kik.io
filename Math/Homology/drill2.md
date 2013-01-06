# ホモロジー計算ドリル(2)

単体的複体の相対ホモロジーも計算をガンガンしてみようと思う。ホモロジーの位相的な応用は相対ホモロジーがないと始まらない。でも、ここではやはり計算に特化して位相的なところにはまだ触れないことにする。

## 単体的複体の相対ホモロジー

### 定義(部分単体的複体)

$V$を頂点とする有限単体的複体$K$にたいして、$K$の部分集合$L$が$K$の部分単体的複体であるとは、$L$も$V$を頂点とする有限単体的複体になっていることをいう。

### 定義(有限単体的複体の対の鎖複体)

$L$を$K$の部分単体的複体とする。これらの対$(K, L)$の$k$次元鎖複体$C_k(K, L)$を
[C_k(K, L) = C_k(K) / C_k(L)]
で定める。

* 包含写像を$i_k : C_k(L) \to C_k(K)$、射影を$j_k : C_k(K) \to C_k(K, L)$と書くことにする。
* 以下は完全系列になる
[0 \xrightarrow{0} C_k(L) \xrightarrow{i_k} C_k(K) \xrightarrow{j_k} C_k(K, L) \xrightarrow{0} 0]

### 定義(対の境界準同型)

対の境界準同型は$R$準同型$\delta_k : C_k(K, L) \to C_{k-1}(K, L)$は$\delta_k : C_k(K) \to C_{k-1}(K)$から誘導される準同型をいう。

* 同じ記号を用いても混乱はしないと思われる

$\DeclareMathOperator{\Ima}{Im}
\DeclareMathOperator{\Ker}{Ker}
$

### 定義(有限単体的複体の対のホモロジー)

対のホモロジー$H_k(K, L)$は対の境界準同型$\delta_k$を用いて
[H_k(K, L) = \Ker{\delta_k} / \Ima{\delta_{k+1}}]
で定義する。

### 定義(連結準同型)

次の図式を可換にする$\Delta_k$を作りたいのだが、鎖複体ではできない。

$$\begin{array}{ccc}
C_k(K, L) & \xrightarrow{\Delta_k?} & C_{k-1}(L) \\\\
j_k\uparrow  & & \downarrow i_{k-1} \\\\
C_k(K) & \xrightarrow[\delta_k]{} & C_{k-1}(K)
\end{array}$$

これをホモロジーにもっていくと$\Delta_k$が作れて、可換なだけでなく完全になる。この$\Delta_k$を連結準同型という。

$$\begin{array}{ccc}
H_k(K, L) & \xrightarrow{\Delta_k} & H_{k-1}(L) \\\\
j_k \uparrow  & & \downarrow i_{k-1}  \\\\
H_k(K) & \xrightarrow[0]{} & H_{k-1}(K)
\end{array}$$

$\Delta_k$は$i_{k-1}^{-1}\circ\delta_k\circ j_k^{-1}$をホモロジーにたいして計算することできちんと定義できる。詳細は適当な本を見るとよい。

### 定義(対の長完全列)

次の完全列を対$(K, L)$のホモロジー長完全列という。

[\dots\xrightarrow{\Delta_{k+1}}H_k(L)\xrightarrow{i_k}H_k(K)\xrightarrow{j_k}H_k(K, L)\xrightarrow{\Delta_k}H_{k-1}(L)\xrightarrow{i_{k-1}}\dots]

### 例(線分と境界の対)

* $V=\\{ v_0, v_1 \\}$
* $K=\\{\langle v_0 \rangle, \langle v_1 \rangle\\} \cup \\{\langle v_0v_1 \rangle \\}$
* $L=\\{\langle v_0 \rangle, \langle v_1 \rangle\\}$
* $H_0(L) = R\langle v_0 \rangle \oplus R\langle v_1 \rangle$, $H_1(L) = 0$
* $H_0(K) = R\langle v_0 \rangle$, $H_1(K) = 0$
* $C_0(K, L) = C_0(K) / C_0(L) = 0$
* $C_1(K, L) = C_1(K) / C_1(L) = R\langle v_0v_1 \rangle$
* $H_0(K, L) = 0$, $H_1(K, L) = R\langle v_0v_1 \rangle$

[H_1(L) = 0 \xrightarrow{0} H_1(K) = 0 \xrightarrow{0} H_1(K, L) = R\langle v_0v_1 \rangle \xrightarrow{\Delta_1} \\\\
H_0(L) = R\langle v_0 \rangle \oplus R\langle v_1 \rangle \xrightarrow{i_0} H_1(K) =  R\langle v_0 \rangle \xrightarrow{0} H_0(K, L) = 0]

* $\Delta_1(\langle v_0v_1 \rangle) = \langle v_1 \rangle - \langle v_0 \rangle$
* $i_0(\langle v_0 \rangle) = \langle v_0 \rangle$
* $i_0(\langle v_1 \rangle) = \langle v_0 \rangle$

* たしかに完全系列になっている
* $\Delta_1$は$\delta_1$が元になっているが、上を完全にするための唯一なものではない。

### 例(線分と境界の一点の対)

* $V=\\{ v_0, v_1 \\}$
* $K=\\{\langle v_0 \rangle, \langle v_1 \rangle\\} \cup \\{\langle v_0v_1 \rangle \\}$
* $L=\\{\langle v_0 \rangle\\}$
* $H_0(L) = R\langle v_0 \rangle$, $H_1(L) = 0$
* $H_0(K) = R\langle v_0 \rangle$, $H_1(K) = 0$
* $C_0(K, L) = C_0(K) / C_0(L) = R\langle v_1 \rangle$
* $C_1(K, L) = C_1(K) / C_1(L) = R\langle v_0v_1 \rangle$
* $(K, L)$について
    * $\delta_1(\langle v_0v_1 \rangle) = \langle v_1 \rangle$
    * $\Ima \delta_1 = C_0(K, L)$
    * $\Ker \delta_1 = 0$
* $H_0(K, L) = 0$, $H_1(K, L) = 0$

[H_1(L) = 0 \xrightarrow{0} H_1(K) = 0 \xrightarrow{0} H_1(K, L) = 0 \xrightarrow{0} \\\\
H_0(L) = R\langle v_0 \rangle \xrightarrow{i_0} H_0(K) =  R\langle v_0 \rangle \xrightarrow{0} H_0(K, L) = 0]

* $i_0(\langle v_0 \rangle) = \langle v_0 \rangle$

### 例(線分と内点の対)

* $V=\\{ v_0, v_1, v_2 \\}$
* $K=\\{\langle v_0 \rangle, \langle v_1 \rangle, \langle v_2 \rangle\\} \cup \\{\langle v_0v_1 \rangle, \langle v_1v_2 \rangle \\}$
* $L=\\{\langle v_1 \rangle\\}$
* $H_0(L) = R\langle v_0 \rangle$, $H_1(L) = 0$
* $H_0(K) = R\langle v_0 \rangle$, $H_1(K) = 0$
* これらの間の$i_k$は同型なので、実際には計算しなくても上の例と同じことが分かる

* $C_0(K, L) = C_0(K) / C_0(L) = R\langle v_0 \rangle \oplus R\langle v_2 \rangle$
* $C_1(K, L) = C_1(K) / C_1(L) = R\langle v_0v_1 \rangle \oplus R\langle v_1v_2 \rangle$
* $(K, L)$について
    * $\delta_1(\langle v_0v_1 \rangle) = -\langle v_0 \rangle$
    * $\delta_1(\langle v_1v_2 \rangle) = \langle v_2 \rangle$
    * $\Ima \delta_1 = C_0(K, L)$
    * $\Ker \delta_1 = 0$
* $H_0(K, L) = 0$, $H_1(K, L) = 0$

[H_1(L) = 0 \xrightarrow{0} H_1(K) = 0 \xrightarrow{0} H_1(K, L) = 0 \xrightarrow{0} \\\\
H_0(L) = R\langle v_0 \rangle \xrightarrow{i_0} H_0(K) =  R\langle v_0 \rangle \xrightarrow{0} H_0(K, L) = 0]

* $i_0(\langle v_0 \rangle) = \langle v_0 \rangle$

### 例(三角形と境界の対)

* $V = \\{ v_0, v_1, v_2 \\}$
* $K = \\{ \langle v_0 \rangle,  \langle v_1 \rangle,  \langle v_2 \rangle \\} \cup \\{  \langle v_0v_1 \rangle, \langle v_1v_2 \rangle, \langle v_0v_2 \rangle \\} \cup \\{ \langle v_0v_1v_2 \rangle \\}$
* $L = \\{ \langle v_0 \rangle,  \langle v_1 \rangle,  \langle v_2 \rangle \\} \cup \\{  \langle v_0v_1 \rangle, \langle v_1v_2 \rangle, \langle v_0v_2 \rangle \\}$
* $H_0(L) = R\langle v_0 \rangle$, $H_1(L) = R(\langle v_0v_1 \rangle + \langle v_1v_2 \rangle - \langle v_0v_2 \rangle)$, $H_2(L) = 0$
* $H_0(K) = R\langle v_0 \rangle$, $H_1(K) = 0$, $H_2(K) = 0$
* 同型と$0$があるので計算しなくてもわりと分かりそうだが、計算したほうが簡単

* $C_0(K, L) = 0$
* $C_1(K, L) = 0$
* $C_2(K, L) = R\langle v_0v_1v_2 \rangle$
* $H_0(K, L) = 0$
* $H_1(K, L) = 0$
* $H_2(K, L) = R\langle v_0v_1v_2 \rangle$

[H_2(L) = 0 \xrightarrow{0} H_2(K) = 0 \xrightarrow{0} H_2(K, L) = R\langle v_0v_1v_2 \rangle \xrightarrow{\Delta_2} \\\\
H_1(L) = R(\langle v_0v_1 \rangle + \langle v_1v_2 \rangle - \langle v_0v_2 \rangle) \xrightarrow{0} H_1(K) = 0 \xrightarrow{0} H_1(K, L) = 0 \xrightarrow{0} \\\\
H_0(L) = R\langle v_0 \rangle \xrightarrow{i_0} H_0(K) =  R\langle v_0 \rangle \xrightarrow{0} H_0(K, L) = 0]

* $\Delta_1(\langle v_0v_1v_2 \rangle) = \langle v_0v_1 \rangle + \langle v_1v_2 \rangle - \langle v_0v_2 \rangle$
* $i_0(\langle v_0 \rangle) = \langle v_0 \rangle$
