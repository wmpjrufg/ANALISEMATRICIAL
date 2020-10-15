<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

# Matriz de rigidez Viga
 
<p style="text-align: justify;">A seguinte matriz de rigidez é baseada na teoria de vigas de Euler-Bernoulli. Onde é considerado que as seções perpendiculares ao eixo longitudinal permanecem planas após a aplicação de cargas.</p>

<p style="text-align: justify;">A função de deslocamento adotada será uma função cúbica (eq. 1), que apresenta boa representação do deslocamento em vigas.</p>
$$(1) \ \ \   \nu(x)=a_{1}x^3+a_{2}x^2+a_{3}x+a_{4}$$

Representando a eq. 8 em função dos graus de liberdade $$\nu_1, \phi_1, \nu_2, \phi_2$$ se obtém eq's. 2 a 5.
<p style="text-align: justify;"> </p>
$$(2) \ \ \      \nu(0)=v_{1}=a_{4}$$<br/>

$$(3) \ \ \      \frac{d\nu(0)}{dx} = \phi_{1}=a_{3}$$<br/>

$$(4) \ \ \      \nu(L)=v_{2}=a_{1}L^3+a_{2}L^2+a_{3}L+a_{4}$$<br/>

$$(5) \ \ \      \frac{d\nu(L)}{dx} = \phi_{2}= 3a_{1}L^2+2a_{1}L+a_{3} $$<br/>

Resolvendo as eq's. 2 a 5 em função dos parâmetros de forma $$a_1 ... a_4$$ e substituindo na eq. 1:
<p style="text-align: justify;"> </p>
$$(6) \ \ \        \nu=\frac{2}{L^3}(\nu_{1}-\nu_{2})+\frac{1}{L^2}(\phi_{1}-\phi_{2})x^3-\frac{3}{L^2}(\nu_{1}-\nu_{2})-\frac{1}{L}(2\phi_{1}-\phi_{2})x^2+\phi_1x+\nu_1$$

Por meio da relação expressa na [eq. 5 da dedução geral do MEF](https://wmpjrufg.github.io/ANALISEMATRICIAL/LIBRARY_MATRIX_ELEMENTS.html) é possível obter as funções de forma $$N_1 ... N_4$$ para o elemento viga (eq's. 8 a 11).
<p style="text-align: justify;"> </p>
$$(7) \ \ \  [N*=[N_1 \ N_2 \ N_3 \ N_4* $$<br/>

$$(8) \ \ \  N_1 = \frac{1}{L^3}(2x^3-3x^2L+L^3)$$<br/>

$$(9) \ \ \  N_2 = \frac{1}{L^3}(x^3L-2x^2L^2+xL^3)$$<br/>

$$(10) \ \ \  N_3 = \frac{1}{L^3}(-2x^3+3x^2L)$$<br/>

$$(11) \ \ \  N_4 = \frac{1}{L^3}(x^3L-x^2L^2)$$<br/>

Sendo a relação entre deformações e deslocamento representado pela eq. 12 e entre o deslocamento axial **(u)** e transversal **$$(\nu)$$** expresso pela eq. 13.
<p style="text-align: justify;"> </p>
$$(12) \ \ \  \varepsilon_x(x,y) = \frac{du}{dx}\\$$<br/>

$$(13) \ \ \  u = -y\frac{d\nu}{dx}\\$$<br/>

Sendo:
+ **y** a distância da linha neutra.

<p style="text-align: justify;">Substituindo a eq. 13 em eq. 12.</p>
$$(14) \ \ \  \varepsilon_x(x,y) = -y\frac{d^2\nu}{dx^2}\\$$

Recorrendo a relação expressa na [eq. 6 da dedução geral do MEF](https://wmpjrufg.github.io/ANALISEMATRICIAL/LIBRARY_MATRIX_ELEMENTS.html)  possível obter a matriz **B**:
<p style="text-align: justify;"> </p>
$$(15) \ \ \  [B] = \frac{-y}{L^3}\left \{ \begin{matrix} (12x - 6L) &  L(6x - 4L) & -(12x - 6L) & L(6x - 2L)\end{matrix}\right \}$$

A matriz de constituição **C** equivalente ao módulo de elasticidade **E**.
Substituindo a eq. 15  e **C** na [eq. 7 da dedução geral do MEF](https://wmpjrufg.github.io/ANALISEMATRICIAL/LIBRARY_MATRIX_ELEMENTS.html) é possível obter a matriz de rigidez **K**:
<p style="text-align: justify;"> </p>
$$(15) \ \ \     K = \int_{0}^{L}\frac{-y}{L^3}\left \{ \begin{matrix} (12x - 6L) &  L(6x - 4L) & -(12x - 6L) & L(6x - 2L)\end{matrix}\right \}^t \\ E \ \frac{-y}{L^3}\left \{ \begin{matrix} (12x - 6L) &  L(6x - 4L) & -(12x - 6L) & L(6x - 2L)\end{matrix}\right \} \ dx \ ^2 \ ^3$$<br/>

$$^2 \ \  I_z = \int\int_{A}^{}y^2 \ dA$$<br/>

$$^3$$ Sendo a área constante, e a variação ocorrendo apenas no eixo x: $$dV = A \ dx$$<br/>


<p style="text-align: justify;">Resolvendo a integral da eq. 15, obtém-se a matriz de rigidez expressa pela eq. 16.</p>
$$(16) \ \ \  
[k*=\frac{EI}{L^3}\begin{bmatrix}
12 & 6L&-12&6L\\
6L&4L^2&-6L&2L^2\\
-12 & -6L&12&-6L\\
6L&2L^2&-6L&4L^2\\
\end{bmatrix}
$$

Sendo $${f} = [K]{d}$$:
<p style="text-align: justify;"></p>
$$(17) \ \ \  
\begin{Bmatrix}
f_{1y}\\
m_1\\
f_{2y}\\
m_1\\
\end{Bmatrix} =\frac{EI}{L^3}\begin{bmatrix}
12 & 6L&-12&6L\\
6L&4L^2&-6L&2L^2\\
-12 & -6L&12&-6L\\
6L&2L^2&-6L&4L^2\\
\end{bmatrix}\begin{Bmatrix}
\nu_1\\
\phi_1\\
\nu_2\\
\phi_2\\
\end{Bmatrix}
$$

     
