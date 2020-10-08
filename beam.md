<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

# Matriz de rigidez Viga
 
<p style="text-align: justify;">A seguinte matriz de rigidez é baseada na teoria de vigas de Euler-Bernoulli. Onde é considerado que as seções perpendiculares ao eixo longitudinal permanecem planas após a aplicação de cargas.
Sendo uma viga submetida a uma carga distribuída w(x), das equações de equilíbrio se obtém eq.1.</p>
$$(1) \ \ \     \sum{F_y }= 0: V-(V+dV)-w(x)dx=0 \label{1}$$

<p style="text-align: justify;">Simplificando a Eq. 1, obtém-se eq. 2 e 3.</p>
$$(2) \ \ \      -wdx - dV = 0 \   or \ w=-\frac{dV}{dx}$$
$$(3) \ \ \      \sum{M_2}=0: -Vdx+dM+w(x)dx\frac{dx}{2}=0 \ ou \ V=\frac{dM}{dx}$$

<p style="text-align: justify;">A curvatura das vigas pode ser obtida por meio da eq. 4.</p>
$$(4) \ \ \      \kappa = \frac{1}{\rho }=\frac{M}{EI}$$

Equanto a curvatura para pequenas rotações $$\phi = \frac{d\nu}{dx}$$ é dada pela eq. 5.
$$(5) \ \ \      \kappa = \frac{d^2v}{dx^2 }$$

<p style="text-align: justify;">Substituindo as eq's. 2 e 3 na eq. 5:</p>
$$(6) \ \ \      \frac{d^2}{dx^2}[EI\frac{d^2v}{dx^2}]=-w(x)$$

<p style="text-align: justify;">Para um módulo de rigidez longitudinal (EI) constante, e com atuação de apenas forças e momentos, a eq. 6 se torna eq. 7.</p>
$$(7) \ \ \      EI\frac{d^4v}{dx^4}$$

<p style="text-align: justify;">A função de deslocamento adotada será uma função cúbica (eq. 8), que apresenta boa representação do deslocamento em vigas.</p>
$$(8) \ \ \   \nu(x)=a_{1}x^3+a_{2}x^2+a_{3}x+a_{4}$$

Representando a eq. 8 em função dos graus de liberdade $$\nu_1, \phi_1, \nu_2, \phi_2$$ se obtém eq's. 9 a 12.
$$(9) \ \ \      \nu(0)=v_{1}=a_{4}$$
$$(10) \ \ \      \frac{d\nu(0)}{dx} = \phi_{1}=a_{3}$$
$$(11) \ \ \      \nu(L)=v_{2}=a_{1}L^3+a_{2}L^2+a_{3}L+a_{4}$$
$$(12) \ \ \      \frac{d\nu(L)}{dx} = \phi_{2}= 3a_{1}L^2+2a_{1}L+a_{3} $$

Resolvendo as eq's. 9 a 12 em função dos parâmetros de forma $$a_1 ... a_4$$ e substituindo na eq. 8:
$$(13) \ \ \        \nu=\frac{2}{L^3}(\nu_{1}-\nu_{2})+\frac{1}{L^2}(\phi_{1}-\phi_{2})x^3-\frac{3}{L^2}(\nu_{1}-\nu_{2})-\frac{1}{L}(2\phi_{1}-\phi_{2})x^2+\phi_1x+\nu_1$$

Transformando as expressões para as formas matriciais descritas nas eq's 14 a 16, é possível obter as funções de forma $$N_1 ... N_4$$ para o elemento viga eq's. 17 a 20.
$$(14) \ \ \        \nu = [N*\{d\}$$
$$(15) \ \ \        
\{d\}=\begin{Bmatrix}
\nu_1\\
\phi_1\\
\nu_2\\
\phi_2\\
\end{Bmatrix}
$$
$$(16) \ \ \  [N*=[N_1 \ N_2 \ N_3 \ N_4* $$
$$(17) \ \ \  N_1 = \frac{1}{L^3}(2x^3-3x^2L+L^3)$$
$$(18) \ \ \  N_2 = \frac{1}{L^3}(x^3L-2x^2L^2+xL^3)$$
$$(19) \ \ \  N_3 = \frac{1}{L^3}(-2x^3+3x^2L)$$
$$(20) \ \ \  N_4 = \frac{1}{L^3}(x^3L-x^2L^2)$$

Sendo a relação entre deformações e deslocamento representado pela eq. 21 e entre o deslocamento axial (u) e transversal $$(\nu)$$ expresso pela eq. 22.
$$(21) \ \ \  \varepsilon_x(x,y) = \frac{du}{dx}\\$$
$$(22) \ \ \  u = -y\frac{d\nu}{dx}\\$$

<p style="text-align: justify;">Substituindo a eq. 22 em eq. 21.</p>
$$(23) \ \ \  \varepsilon_x(x,y) = -y\frac{d^2\nu}{dx^2}\\$$

<p style="text-align: justify;">A partir da lei de Hooke (eq 23), substituindo a eq. 4 na eq. 23, é obtido a formulação para tensões em vigas (eq. 24).</p>
$$(24) \ \ \  \sigma_x = \frac{-My}{I}\\$$

<p style="text-align: justify;">A relação do momento fletor e esforço cortante com os deslocamentos pode ser expressa pelas eq's. 25 e 26.</p>
$$(25) \ \ \  m(x)=EI\frac{d^2\nu}{dx^2}\\$$
$$(26) \ \ \  V = EI\frac{d^3\nu}{dx^3}\\$$

<p style="text-align: justify;">Substituindo a equação de deslocamento eq. 13 nas eq's. 25 e 26, obtém-se os momentos fletores e esforços cortantes nos nós da viga (eq's. 27 a 30).</p>
$$(27) \ \ \  f_{1y}=V=EI\frac{d^3\nu(0)}{dx^3}=\frac{EI}{L^3}(12\nu_1+6L\phi_1-12\nu_2+6L\phi_2)\\
(28) \ \ \  m_{1}=-m=-EI\frac{d^2\nu(0)}{dx^2}=\frac{EI}{L^3}(6L\nu_1+4L^2\phi_1-6L\nu_2+2L^2\phi_2)\\
(29) \ \ \  f_{2y}=V=EI\frac{d^3\nu(L)}{dx^3}=\frac{EI}{L^3}(-12\nu_1-6L\phi_1+12\nu_2-6L\phi_2)\\
(30) \ \ \  m_{2}=-m=-EI\frac{d^2\nu(L)}{dx^2}=\frac{EI}{L^3}(6L\nu_1+2L^2\phi_1-6L\nu_2+4L^2\phi_2)$$

<p style="text-align: justify;">Por meio das eq's. 27 a 30 é possível obter a forma matricial dos deslocamentos globais (eq. 31).</p>
$$(31) \ \ \  
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

<p style="text-align: justify;">Onde a matriz de rigidez do elemento viga é expresso pela eq. 32.</p>
$$32) \ \ \  
[k*=\frac{EI}{L^3}\begin{bmatrix}
12 & 6L&-12&6L\\
6L&4L^2&-6L&2L^2\\
-12 & -6L&12&-6L\\
6L&2L^2&-6L&4L^2\\
\end{bmatrix}
$$
     
