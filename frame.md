<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script> <script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

# Matriz de rigidez Pórtico

<p style="text-align: justify;">Pórticos são elementos estruturais arbitrariamente orientados no plano, em que sua modelagem físico-matemática são considerados rotações, translações verticais e translações horizontais.</p>

$$\begin{Bmatrix}\nu'_1 \\ \phi'_1\\ \nu'_2 \\ \phi'_2 \end{Bmatrix} = \begin{bmatrix}-S & C & 0& 0& 0& 0\\ 0 & 0 & 1& 0& 0& 0\\ 0 & 0 & 0& -S& C& 0\\ 0 & 0 & 0& 0& 0& 1 \end{bmatrix}\begin{Bmatrix}u_1\\\nu_1 \\ \phi_1\\ u_2\\\nu_2 \\ \phi_2 \end{Bmatrix}$$
\\
\\
$$T =\begin{bmatrix}\-S & C & 0& 0& 0& 0\\ 0 & 0 & 1& 0& 0& 0\\ 0 & 0 & 0& -S& C& 0\\ 0 & 0 & 0& 0& 0& 1 \end{bmatrix}$$

\\
\\

$$k =\frac{EI}{L^3}\begin{bmatrix} 12S^2&-12SC&-6LS&-12S^2&12SC&-6LS\\&12C^2&6LC&12SC&-12C^2&6LC\\&&-4L^2&6LS&-6LC&2L^2\\&&&12C^2&-12SC&6LS\\&&&&12C^2&-6LC\\Simetrico&&&&&4L^2\\\end{bmatrix}$$


$$\begin{Bmatrix}f'_{1x} \\ f'_{1y}\\ m'_{1} \\ f'_{2x} \\ f'_{2y} \\ m'_{2} \end{Bmatrix} = \begin{bmatrix}C_1 & 0 & 0& -C_1& 0& 0\\ 0 & 12C_2 & 6C_2L& 0& -12C_2& 6C_2L\\ 0 & 6C_2L& 4C_2L^2& 0& -6C_2L& 2C_2L^2\\-C_1 & 0 & 0& C_1& 0& 0\\ 0 & -12C_2 & -6C_2L& 0& 12C_2& -6C_2L\\ 0 & 6C_2L& 2C_2L^2& 0& -6C_2L& 4C_2L^2 \end{bmatrix}\begin{Bmatrix}u'_1\\\nu'_1 \\ \phi'_1\\ u'_2\\\nu'_2 \\ \phi'_2 \end{Bmatrix}$$

$$C_1 = \frac{AE}{L} \ \ e \ \ C_2 = \frac{EI}{L^3}$$

$$k' =\begin{bmatrix}C_1 & 0 & 0& -C_1& 0& 0\\ 0 & 12C_2 & 6C_2L& 0& -12C_2& 6C_2L\\ 0 & 6C_2L& 4C_2L^2& 0& -6C_2L& 2C_2L^2\\-C_1 & 0 & 0& C_1& 0& 0\\ 0 & -12C_2 & -6C_2L& 0& 12C_2& -6C_2L\\ 0 & 6C_2L& 2C_2L^2& 0& -6C_2L& 4C_2L^2 \end{bmatrix}$$

$$\begin{Bmatrix}u'_1\\\nu'_1 \\ \phi'_1\\ u'_2\\\nu'_2 \\ \phi'_2 \end{Bmatrix} = \begin{bmatrix} C & S & 0& 0& 0& 0\\ -S & C& 0& 0& 0 &0\\ 0 & 0& 1& 0& 0& 0\\0 & 0 & 0& C& S& 0\\ 0 & 0 & 0& -S& C& 0\\ 0 & 0& 0& 0& 0& 1 \end{bmatrix}\begin{Bmatrix}u_1\\\nu_1 \\ \phi_1\\ u_2\\\nu_2 \\ \phi_2 \end{Bmatrix}$$

$$ T = \begin{bmatrix} C & S & 0& 0& 0& 0\\ -S & C& 0& 0& 0 &0\\ 0 & 0& 1& 0& 0& 0\\0 & 0 & 0& C& S& 0\\ 0 & 0 & 0& -S& C& 0\\ 0 & 0& 0& 0& 0& 1 \end{bmatrix}$$

$$k = \frac{E}{L}\times\begin{bmatrix}AC^2+\frac{12I}{L^2}S^2 & (A-\frac{12I}{L^2})CS & \frac{-6I}{L}S &-(AC^2+\frac{12I}{L^2}S^2)&-(A-\frac{12I}{L^2})CS &-\frac{6I}{L}S\\ 
& AS^2+\frac{12I}{L^2}C^2  & \frac{6I}{L}C &-(A-\frac{12I}{L^2})CS&-(AS^2+\frac{12I}{L^2}C^2)&\frac{6I}{L}C\\
 & & 4I & \frac{6I}{L}S &-\frac{6I}{L}C & 2I\\
& & & AC^2+\frac{12I}{L^2}S^2 & (A-\frac{12I}{L^2})CS&\frac{6I}{L}S\\
& & & & AS^2+\frac{12I}{L^2}C^2& -\frac{6I}{L}C\\
Simetrico & & & & & 4I\end{bmatrix}$$



258/106
