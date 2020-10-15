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

$$(11) \ \ \    N_1 = 1-\frac{x}{L}$$<br/>

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

<p style="text-align: justify;"> Para a barra arbitrariamente orientada no plano global x-y, a matriz de forças pode ser expressa pela eq. 20, ou eq. 21 na forma simplificada. </p> 

$$(20) \ \ \    \begin{Bmatrix}f'_{1x}\\f'_2x
\end{Bmatrix} = \frac{AE}{L}\begin{bmatrix} 1 & -1 \\ -1 & 1 \end{bmatrix} \begin{Bmatrix}u'_1 \\ u'_2 \end{Bmatrix}$$<br/>

$$(21) \ \ \     {f'} = [k']{d'} $$<br/>

Onde:
$${f'}$$: Forças aplicadas aos nós nos eixos locais x'-y';
$$[k']$$: Matriz de rigidez do elemento orientado no plano x'-y';
$${d'}$$: Deslocamentos nodais nos eixos locais x'-y';

<p style="text-align: justify;"> Sendo a barra arbitrariamente orientada no espaço, devido a decomposição de forças, a matriz de deslocamentos global será representada pela eq. 22. </p>
$$(22) \ \ \    \begin{Bmatrix}f_{1x}\\f_1y\\f_{2x}\\f_2y
\end{Bmatrix} = [k] \begin{Bmatrix}u_1 \\ \nu_1 \\u_2 \\ \nu_2 \end{Bmatrix}$$<br/>

<p style="text-align: justify;"> A relação dos deslocamentos locais e x'-y' com os deslocamentos globais em x-y é dado pelas eq's. 23 e 24. </p>
$$(23) \ \ \     u'_1 = u_1cos\theta + \nu_1sin\theta $$<br/>

$$(24) \ \ \     u'_2 = u_2cos\theta + \nu_2sin\theta $$<br/>

<p style="text-align: justify;"> As eq's. 23 e 24 na forma matricial são expressos pela eq. 25. </p>
$$(25) \ \ \    \begin{Bmatrix}u'_{1x}\\u'_2x
\end{Bmatrix} = \begin{bmatrix} C & S & 0 & 0 \\ 0 & 0 & C & S  \end{bmatrix} \begin{Bmatrix}u_1 \\ \nu_1 \\ u_2 \\ \nu_2 \end{Bmatrix}$$<br/>

<p style="text-align: justify;"> Nota-se então através da eq. 25 que a transformação dos deslocamentos locais e globais apresenta a seguinte relação (eq. 26) </p>
$$(26) \ \ \     {d'} = [T]{d} $$<br/>

<p style="text-align: justify;">Esta transformação de coordenadas é possível devido à [T], representado pela eq. 27.  </p>
$$(27) \ \ \   [T] = \begin{bmatrix} C & S & 0 & 0 \\ 0 & 0 & C & S  \end{bmatrix}$$<br/>

<p style="text-align: justify;"> De forma similar aos deslocamentos, a transformação das forças locais em globais é dada pela eq. 28. </p>
$$(28) \ \ \    \begin{Bmatrix}f'_{1x}\\f'_2x
\end{Bmatrix} = \begin{bmatrix} C & S & 0 & 0 \\ 0 & 0 & C & S  \end{bmatrix} \begin{Bmatrix}f_1x \\ f_1y \\ f_2x \\ f_2y \end{Bmatrix}$$<br/>

<p style="text-align: justify;"> Da forma simplificada: </p>
$$(29) \ \ \     {f'} = [T]{f} $$<br/>

<p style="text-align: justify;"> Substituindo as eq's. 26 e 27 na eq. 21, é obtido a eq. 30: </p>
$$(30) \ \ \     [T]{f} = [k'][T]{d} $$<br/>

<p style="text-align: justify;"> Uma eventual obtenção dos deslocamentos não seria possível haja vista que substituindo a eq. 25 na eq. 30, resultaria em uma matriz [T] não quadrada, impossibilitando a obtenção de sua matriz inversa. Deste modo, é necessária expandir a eq. 25, incluindo os deslocamentos e forças perpendiculares ao eixo do elemento, mesmo sabendo que estes são nulos:  </p>
$$(31) \ \ \    \begin{Bmatrix}u'_1\\ \nu'_1 \\ u'_2\\ \nu'_2
\end{Bmatrix} = \begin{bmatrix} C & S & 0 & 0 \\ -S & C & 0 & 0 \\ 0 & 0 & C & S \\  0 & 0 & -S & C  \end{bmatrix} \begin{Bmatrix}u_1 \\ \nu_1 \\ u_2 \\ \nu_2 \end{Bmatrix}$$<br/>

<p style="text-align: justify;">A nova matriz de transformação será portanto a eq. 32.  </p>
$$(32) \ \ \    [T] = \begin{bmatrix} C & S & 0 & 0 \\ -S & C & 0 & 0 \\ 0 & 0 & C & S \\  0 & 0 & -S & C  \end{bmatrix} $$<br/>

<p style="text-align: justify;">Aplicando o mesmo processo de expansão referente a eq. 31 à eq. 20:  </p>
$$(33) \ \ \    \begin{Bmatrix}f'_1x\\ f'_1y \\ f'_2x\\ f'_2y
\end{Bmatrix} = \frac{AE}{L}\begin{bmatrix} 1 & 0 & -1 & 0 \\ 0 & 0 & 0 & 0 \\ -1 & 0 & 1 & 0 \\  0 & 0 & 0 & 0  \end{bmatrix} \begin{Bmatrix}u_1 \\ \nu_1 \\ u_2 \\ \nu_2 \end{Bmatrix}$$<br/>

<p style="text-align: justify;">Identifica-se a matriz de rigidez [k'] como:  </p>
$$(34) \ \ \    [k'] = \frac{AE}{L}\begin{bmatrix} 1 & 0 & -1 & 0 \\ 0 & 0 & 0 & 0 \\ -1 & 0 & 1 & 0 \\  0 & 0 & 0 & 0  \end{bmatrix}$$<br/>

<p style="text-align: justify;">Isolando a eq. 30 em função de {f}: </p>
$$(35) \ \ \     {f} = [T]^{-1}[k'][T]{d} $$<br/>

<p style="text-align: justify;">Nota-se devido às características da matriz [T] que sua inversa é também a matriz transposta: </p>
$$(36) \ \ \     [T]^{-1}=[T]^T $$<br/>

<p style="text-align: justify;">Deste modo, a eq. 35 toma a seguinte forma: </p>
$$(37) \ \ \     {f} = [T]^T[k'][T]{d} $$<br/>

<p style="text-align: justify;">Onde a rigidez é expressa por: </p>
$$(38) \ \ \     [k] = [T]^T[k'][T] $$<br/>

<p style="text-align: justify;">Substituindo as eq's. 32 e 34 na eq. 38, obtém-se a matriz de rigidez (eq. 39) referente às coordenadas globais x-y:   </p>
$$(39) \ \ \    [k] = \frac{AE}{L}\begin{bmatrix} C^2 & CS & -C^2 & -CS \\ CS & S^2 & -CS & -S^2 \\ -C^2 & -CS & C^2 & CS \\  -CS & -S^2 & CS & S^2  \end{bmatrix} $$<br/>


