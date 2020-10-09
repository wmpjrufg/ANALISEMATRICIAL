<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script> 
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
    
# Matriz de rigidez Treliça
### Paralela ao eixo x

<p style="text-align: justify;">As treliças são elementos estruturais cujo únicos esforços atuantes são aqueles normais à seção transversal. Isto é possível devido ao fato de que as cargas são aplicadas nos nós, que contém uniões denominadas rótulas, onde é permitido uma maior flexibilidade ao elemento sem a transmissão de esforços de flexão. Deste modo:</p>

$$ \ \ \    f_{1y} = 0, \ f_{2y} = 0, \ m_{1} = 0, m_{2} = 0 $$

Para desenvolvimento da dedução da matriz de rigidez das treliças, os deslocamentos longitudinais serão representados por $$u_1 e u_2 $$.<br/> 
<p style="text-align: justify;">A deformação axial e tensão normal dos elementos são expressos pelas eq's. 1 e 2 respectivamente. </p>
$$(1) \ \ \     \sigma_x= E\varepsilon_x$$<br/>

$$(2) \ \ \     \varepsilon_x = \frac{du}{dx}$$<br/>

<p style="text-align: justify;">Do equilíbrio de forças, se obtém eq. 3.</p>
$$(3) \ \ \     A\sigma_x= T = constante$$<br/>

<p style="text-align: justify;">A equação que governa o deslocamento será portanto a eq. 4:</p>
$$(4) \ \ \     \frac{d}{dx}(AE\frac{du}{dx})$$<br/>

<p style="text-align: justify;">Para este tipo de elemento, com deslocamentos apenas axiais, a função aproximadora pode ser tomada como linear (eq. 5). </p>
$$(5) \ \ \     u = a_1 + a_2x$$<br/>

<p style="text-align: justify;">A função linear aproximadora toma a forma matricial expressa pela eq. 6.</p>

$$(6) \ \ \     u = \begin{bmatrix}1 & x \end{bmatrix}\begin{Bmatrix}a_1 \\ a_2 \end{Bmatrix}$$<br/>

<p style="text-align: justify;">Aplicando a equação de deslocamento para as condições de contorno do elemento, obtém-se as eq's. 7 e 8. </p>
$$(7) \ \ \     u(0) = u_1 = a_1$$<br/>

$$(8) \ \ \     u(L) = u_2 = a_2L + u_1$$<br/>

Resolvendo as eq's. 7 e 8 em função de $$ a_1 e a_2$$ se obtém eq. 9.
<p style="text-align: justify;"> </p>
$$(9) \ \ \     u = (\frac{u_2-u_1}{L})x+u_1$$<br/>

<p style="text-align: justify;">Que na forma matricial é representada pela eq. 10 </p>
$$(10) \ \ \     u = \begin{bmatrix} N_1 & N_2 \end{bmatrix}\begin{Bmatrix} u_1\\ u_2 \end{Bmatrix} $$<br/>

<p style="text-align: justify;">Sendo as funções de forma dadas por:</p>

$$(11) \ \ \    N_1 = -\frac{x}{L}$$<br/>

$$(12) \ \ \    N_2 = \frac{x}{L}$$<br/>

<p style="text-align: justify;">Substituindo a eq. 9 na eq. 2 se obtém eq. 13 que expressa as deformações do elemento.</p>
$$(13) \ \ \     \varepsilon_x = \frac{u_2-u_1}{L}$$<br/>

<p style="text-align: justify;">Substituindo a eq. 9 na eq. 3 se obtém eq. 14 que relaciona os esforços normais com os deslocamentos.</p>
$$(14) \ \ \     T = AE\frac{u_2-u_1}{L}$$<br/>

<p style="text-align: justify;">Aplicando-se o método das seções no elemento, se obtém as seguintes forças axiais.</p> 
$$(15) \ \ \     f_{1x} = -T \ e \ f_{2x} = T $$<br/>

$$(16) \ \ \     f_{1x} = -AE\frac{u_2 - u_1}{L} $$<br/>

$$(17) \ \ \     f_{2x} = AE\frac{u_2 - u_1}{L} $$<br/>

<p style="text-align: justify;">Expressando as eq's. 16 e 17 na forma matricial (eq. 18):
</p> 
$$(18) \ \ \    \begin{Bmatrix}f_{1x}\\f_2x
\end{Bmatrix} = \frac{AE}{L}\begin{bmatrix} 1 & -1 \\ -1 & 1 \end{bmatrix} \begin{Bmatrix}u_1 \\ u_2 \end{Bmatrix}$$<br/>

Sendo $${f} = [k]{d}$$, a matriz de rigidez será (eq. 19):
<p style="text-align: justify;"> </p> 
$$(19) \ \ \    [k] = \frac{AE}{L}\begin{bmatrix} 1 & -1 \\ -1 & 1 \end{bmatrix}$$<br/>

### Arbitrariamente orientada no plano x-y
Para a barra arbitrariamente orientada no plano global x-y.

$$(16) \ \ \    \begin{Bmatrix}f'_{1x}\\f'_2x
\end{Bmatrix} = \frac{AE}{L}\begin{bmatrix} 1 & -1 \\ -1 & 1 \end{bmatrix} \begin{Bmatrix}u'_1 \\ u'_2 \end{Bmatrix}$$<br/>

$$(17) \ \ \     {f'} = [k]{d'} $$<br/>

Sendo a barra arbitrariamente orientada no espaço, devido a decomposição de forças, a matriz de deslocamentos toma a seguinte forma:

$$(18) \ \ \    \begin{Bmatrix}f_{1x}\\f_1y\\f_{2x}\\f_2y
\end{Bmatrix} = [k] \begin{Bmatrix}u_1 \\ \nu_1 \\u_2 \\ \nu_2 \end{Bmatrix}$$<br/>

$$(19) \ \ \     u'_1 = u_1cos\theta + \nu_1sin\theta $$<br/>

$$(20) \ \ \     u'_2 = u_2cos\theta + \nu_2sin\theta $$<br/>

Na forma matricial:


$$(21) \ \ \    \begin{Bmatrix}u'_{1x}\\u'_2x
\end{Bmatrix} = \begin{bmatrix} C & S & 0 & 0 \\ 0 & 0 & C & S  \end{bmatrix} \begin{Bmatrix}u_1 \\ \nu_1 \\ u_2 \\ \nu_2 \end{Bmatrix}$$<br/>

$$(22) \ \ \     {d'} = [T]{d} $$<br/>

$$(23) \ \ \   [T] = \begin{bmatrix} C & S & 0 & 0 \\ 0 & 0 & C & S  \end{bmatrix}$$<br/>

$$(24) \ \ \    \begin{Bmatrix}f'_{1x}\\f'_2x
\end{Bmatrix} = \begin{bmatrix} C & S & 0 & 0 \\ 0 & 0 & C & S  \end{bmatrix} \begin{Bmatrix}f_1x \\ f_1y \\ f_2x \\ f_2y \end{Bmatrix}$$<br/>

$$(25) \ \ \     {f'} = [T]{f} $$<br/>

$$(26) \ \ \     {f'} = [k'][T]{d} $$<br/>

$$(27) \ \ \     [T]{f'} = [k'][T]{d} $$<br/>

$$(28) \ \ \    \begin{Bmatrix}u'_1\\ \nu'_1 \\ u'_2\\ \nu'_2
\end{Bmatrix} = \begin{bmatrix} C & S & 0 & 0 \\ -S & C & 0 & 0 \\ 0 & 0 & C & S \\  0 & 0 & -S & C  \end{bmatrix} \begin{Bmatrix}u_1 \\ \nu_1 \\ u_2 \\ \nu_2 \end{Bmatrix}$$<br/>

$$(29) \ \ \    [T] = \begin{bmatrix} C & S & 0 & 0 \\ -S & C & 0 & 0 \\ 0 & 0 & C & S \\  0 & 0 & -S & C  \end{bmatrix} $$<br/>

$$(30) \ \ \    \begin{Bmatrix}f'_1x\\ f'_1y \\ f'_2x\\ f'_2y
\end{Bmatrix} = \frac{AE}{L}\begin{bmatrix} 1 & 0 & -1 & 0 \\ 0 & 0 & 0 & 0 \\ -1 & 0 & 1 & 0 \\  0 & 0 & 0 & 0  \end{bmatrix} \begin{Bmatrix}u_1 \\ \nu_1 \\ u_2 \\ \nu_2 \end{Bmatrix}$$<br/>

$$(31) \ \ \     {f} = [T]^-1[k'][T]{d} $$<br/>

$$(32) \ \ \     [T]^-1=[T]^T $$<br/>

$$(33) \ \ \     {f} = [T]^T[k'][T]{d} $$<br/>

$$(34) \ \ \     [k] = [T]^T[k'][T] $$<br/>

$$(35) \ \ \    [k] = \frac{AE}{L}\begin{bmatrix} C^2 & CS & -C^2 & -CS \\ CS & S^2 & -CS & -S^2 \\ -C^2 & -CS & C^2 & CS \\  -CS & -S^2 & CS & S^2  \end{bmatrix} $$<br/>
