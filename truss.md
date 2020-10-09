<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script> 
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
<div class="MathJax_Display" style="text-align: left;">
    
#Matriz de rigidez Treliça

<p style="text-align: justify;">As treliças são elementos estruturais cujo únicos esforços atuantes são aqueles normais à seção transversal. Isto é possível devido ao fato de que as cargas são aplicadas nos nós, que contém uniões denominadas rótulas, onde é permitido uma maior flexibilidade ao elemento sem a transmissão de esforços de flexão. Deste modo:</p>

$$ \ \ \    f_{1y} = 0, \ f_{2y} = 0, \ m_{1} = 0, m_{2} = 0 $$

Para desenvolvimento da dedução da matriz de rigidez das treliças, os deslocamentos longitudinais serão representados por $$u_1 e u_2 $$. 
<p style="text-align: justify;">A deformação axial e tensão normal dos elementos são expressos pelas eq's. 1 e 2 respectivamente. </p>
$$(1) \ \ \     \sigma_x= E\varepsilon_x$$<br/>

$$(2) \ \ \     \varepsilon_x = \frac{du}{dx}$$<br/>

Do equilíbrio de forças, se obtém eq. 3.
$$(3) \ \ \     A\sigma_x= T = constante$$<br/>

A equação que governa o deslocamento será portanto:
$$(4) \ \ \     \frac{d}{dx}(AE\frac{du}{dx})$$<br/>

<p style="text-align: justify;">Para este tipo de elemento, com deslocamentos apenas axiais, a função aproximadora pode ser tomada como linear (eq. 5). </p>
$$(5) \ \ \     u = a_1 + a_2x$$<br/>

$$(6) \ \ \     u = (\frac{u_2-u_1}{L})x+u_1$$<br/>

$$(7) \ \ \     u = \begin{bmatrix} N_1 & N_2 \end{bmatrix}\begin{Bmatrix} u_1\\ u_2 \end{Bmatrix} $$<br/>

As funções de forma são dadas por:

$$(8) \ \ \    N_1 = N_2 = \frac{x}{L}$$<br/>

$$(9) \ \ \     \varepsilon_x = \frac{u_2-u_1}{L}$$<br/>

$$(10) \ \ \     T = AE\frac{u_2-u_1}{L}$$<br/>

Por convenção (Figura):
$$(11) \ \ \     f_{1x} = -T \ e \ f_{2x} = T $$<br/>

$$(12) \ \ \     f_{1x} = f_{1x} = AE\frac{u_2u_1}{L} $$<br/>

Expressando na forma matricial:

$$(13) \ \ \    \begin{Bmatrix}f_{1x}\\f_2x
\end{Bmatrix} = \frac{AE}{L}\begin{bmatrix} 1 & -1 \\ -1 & 1 \end{bmatrix} \begin{Bmatrix}u_1 \\ u_2 \end{Bmatrix}$$<br/>

$$(14) \ \ \     {f} = [k]{d} $$<br/>

Onde a matriz de rigidez é:

$$(15) \ \ \    [k] = \frac{AE}{L}\begin{bmatrix} 1 & -1 \\ -1 & 1 \end{bmatrix}$$<br/>

Para a barra arbitrariamente orientada no plano global x-y.

$$(16) \ \ \    \begin{Bmatrix}f'_{1x}\\f'_2x
\end{Bmatrix} = \frac{AE}{L}\begin{bmatrix} 1 & -1 \\ -1 & 1 \end{bmatrix}$$<br/>
