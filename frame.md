<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script> <script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

# Matriz de rigidez Pórtico plano

<p style="text-align: justify;">Pórticos são elementos estruturais arbitrariamente orientados no plano, em que sua modelagem físico-matemática são considerados rotações, translações verticais e translações horizontais.

A matriz de compatibilidade cinemática **B** para o pórtico será a combinação das matrizes **B** da [viga (eq. 15)](https://wmpjrufg.github.io/ANALISEMATRICIAL/beam.html) e da [treliça (eq. 14)](https://wmpjrufg.github.io/ANALISEMATRICIAL/truss.html):
<p style="text-align: justify;"> </p>

$$(1) \ \ \  [B] = \left \{ \begin{matrix} \frac{-1}{L} & \frac{-y}{L^3}(12x - 6L) &  \frac{-y}{L^2}(6x - 4L) & \frac{-1}{L} & -\frac{-y}{L^3}(12x - 6L) & \frac{-y}{L^2}(6x - 2L)\end{matrix}\right \}$$<br/>

A matriz de constituição **C** equivalente ao módulo de elasticidade **E**.
Substituindo a eq. 1  e **C** na [eq. 7 da dedução geral do MEF](https://wmpjrufg.github.io/ANALISEMATRICIAL/LIBRARY_MATRIX_ELEMENTS.html) é possível obter a matriz de rigidez **K**:
<p style="text-align: justify;"> </p>
$$(2) \ \ \     K = \int_{0}^{L}\left \{ \begin{matrix} \frac{-1}{L} & \frac{-y}{L^3}(12x - 6L) &  \frac{-y}{L^2}(6x - 4L) & \frac{-1}{L} & -\frac{-y}{L^3}(12x - 6L) & \frac{-y}{L^2}(6x - 2L)\end{matrix}\right \}^t \\ E \ \\left \{ \begin{matrix} \frac{-1}{L} & \frac{-y}{L^3}(12x - 6L) &  \frac{-y}{L^2}(6x - 4L) & \frac{-1}{L} & -\frac{-y}{L^3}(12x - 6L) & \frac{-y}{L^2}(6x - 2L)\end{matrix}\right \} \ dx \ ^2 \ ^3$$<br/>

$$^2 \ \  I_z = \int\int_{A}^{}y^2 \ dA$$<br/>

$$^3$$ Sendo a área constante, e a variação ocorrendo apenas no eixo x: $$dV = A \ dx$$<br/>

<p style="text-align: justify;">Resolvendo a integral da eq. 2, obtém-se a matriz de rigidez expressa pela eq. 3.</p>
$$(3) \ \ \     K =\begin{bmatrix}C_1 & 0 & 0& -C_1& 0& 0\\ 0 & 12C_2 & 6C_2L& 0& -12C_2& 6C_2L\\ 0 & 6C_2L& 4C_2L^2& 0& -6C_2L& 2C_2L^2\\-C_1 & 0 & 0& C_1& 0& 0\\ 0 & -12C_2 & -6C_2L& 0& 12C_2& -6C_2L\\ 0 & 6C_2L& 2C_2L^2& 0& -6C_2L& 4C_2L^2 \end{bmatrix}$$<br/>

<p style="text-align: justify;"> Onde: </p>

$$C_1 = \frac{AE}{L} \ \ e \ \ C_2 = \frac{EI}{L^3}$$

Sendo $${f} = [K]{d}$$:
$$(4) \ \ \     \begin{Bmatrix}f'_{1x} \\ f'_{1y}\\ m'_{1} \\ f'_{2x} \\ f'_{2y} \\ m'_{2} \end{Bmatrix} = \begin{bmatrix}C_1 & 0 & 0& -C_1& 0& 0\\ 0 & 12C_2 & 6C_2L& 0& -12C_2& 6C_2L\\ 0 & 6C_2L& 4C_2L^2& 0& -6C_2L& 2C_2L^2\\-C_1 & 0 & 0& C_1& 0& 0\\ 0 & -12C_2 & -6C_2L& 0& 12C_2& -6C_2L\\ 0 & 6C_2L& 2C_2L^2& 0& -6C_2L& 4C_2L^2 \end{bmatrix}\begin{Bmatrix}u'_1\\\nu'_1 \\ \phi'_1\\ u'_2\\\nu'_2 \\ \phi'_2 \end{Bmatrix}$$<br/>

# Matriz de rigidez Pórtico arbitrariamente orientado no plano

<p style="text-align: justify;">Sendo a relação entre os graus de liberdade de um elemento orientado no plano com eixos locais x'-y' e os graus de liberdade orientados nos eixos globais x-y expresso pela eq. 1.</p>
$$(1) \ \ \     \begin{Bmatrix}\nu'_1 \\ \phi'_1\\ \nu'_2 \\ \phi'_2 \end{Bmatrix} = \begin{bmatrix}-S & C & 0& 0& 0& 0\\ 0 & 0 & 1& 0& 0& 0\\ 0 & 0 & 0& -S& C& 0\\ 0 & 0 & 0& 0& 0& 1 \end{bmatrix}\begin{Bmatrix}u_1\\\nu_1 \\ \phi_1\\ u_2\\\nu_2 \\ \phi_2 \end{Bmatrix}$$<br/>

<p style="text-align: justify;"> Onde a matriz de transformação é expressa pela eq. 2.</p>
$$(2) \ \ \     T =\begin{bmatrix}-S & C & 0& 0& 0& 0\\ 0 & 0 & 1& 0& 0& 0\\ 0 & 0 & 0& -S& C& 0\\ 0 & 0 & 0& 0& 0& 1 \end{bmatrix}$$<br/>

<p style="text-align: justify;"> Sendo a rigidez para um elemento orientaod arbitrariamente no plano determinado pela eq. 3:</p>
$$(3) \ \ \     [k] =[T^{T}][k'][T]$$<br/>

<p style="text-align: justify;">Em um primeiro momento, a dedução da matriz de rigidez será realizada considerando a atuação de apenas rotação e esforços cisalhantes, deste modo, pode-se utilizar a matriz de rigidez de vigas para determinação da matriz de rigidez dos pórticos.
Substituindo a eq. 2 e eq. 32 - viga¹ na eq. 3 se obtém a matriz de rigidez global dos elementos (eq. 4).</p>
$$(4) \ \ \     k =\frac{EI}{L^3}\begin{bmatrix} 12S^2&-12SC&-6LS&-12S^2&12SC&-6LS\\&12C^2&6LC&12SC&-12C^2&6LC\\&&-4L^2&6LS&-6LC&2L^2\\&&&12C^2&-12SC&6LS\\&&&&12C^2&-6LC\\Simetrico&&&&&4L^2\\\end{bmatrix}$$<br/>


<p style="text-align: justify;">Da mesma forma, inserindo os efeitos axiais da direção x', na relação entre deslocamentos locais e globais (eq. 1), resulta-se a eq. 7.</p>
$$(7) \ \ \    \begin{Bmatrix}u'_1\\\nu'_1 \\ \phi'_1\\ u'_2\\\nu'_2 \\ \phi'_2 \end{Bmatrix} = \begin{bmatrix} C & S & 0& 0& 0& 0\\ -S & C& 0& 0& 0 &0\\ 0 & 0& 1& 0& 0& 0\\0 & 0 & 0& C& S& 0\\ 0 & 0 & 0& -S& C& 0\\ 0 & 0& 0& 0& 0& 1 \end{bmatrix}\begin{Bmatrix}u_1\\\nu_1 \\ \phi_1\\ u_2\\\nu_2 \\ \phi_2 \end{Bmatrix}$$<br/>

<p style="text-align: justify;">A nova matriz de transformação é dada portanto através da eq. 8.</p>
$$(8) \ \ \    T = \begin{bmatrix} C & S & 0& 0& 0& 0\\ -S & C& 0& 0& 0 &0\\ 0 & 0& 1& 0& 0& 0\\0 & 0 & 0& C& S& 0\\ 0 & 0 & 0& -S& C& 0\\ 0 & 0& 0& 0& 0& 1 \end{bmatrix}$$<br/>

<p style="text-align: justify;">Por fim, substituindo as eq's. 6 e 8 na eq. 3, obtém-se a matriz de rigidez global para um pórtico plano expresso pela eq. 9.</p>
$$(9) \ \ \    k = \frac{E}{L}\times\begin{bmatrix}AC^2+\frac{12I}{L^2}S^2 & (A-\frac{12I}{L^2})CS & \frac{-6I}{L}S &-(AC^2+\frac{12I}{L^2}S^2)&-(A-\frac{12I}{L^2})CS &-\frac{6I}{L}S\\ 
& AS^2+\frac{12I}{L^2}C^2  & \frac{6I}{L}C &-(A-\frac{12I}{L^2})CS&-(AS^2+\frac{12I}{L^2}C^2)&\frac{6I}{L}C\\
 & & 4I & \frac{6I}{L}S &-\frac{6I}{L}C & 2I\\
& & & AC^2+\frac{12I}{L^2}S^2 & (A-\frac{12I}{L^2})CS&\frac{6I}{L}S\\
& & & & AS^2+\frac{12I}{L^2}C^2& -\frac{6I}{L}C\\
Simetrico & & & & & 4I\end{bmatrix}$$<br/>

