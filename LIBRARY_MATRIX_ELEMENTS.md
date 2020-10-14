<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

# Formulação geral do Método dos Elementos finitos.

<p style="text-align: justify;"> O Método dos Elementos Finitos pode ser definido como um método aproximado para resolução de equações diferenciais utilizando o princípio variacional e aproximação polinomial de funções (BABUSKA; STROUBOULIS, 2001). A forma generalizado do MEF para aplicação em estruturas contínuas, bi e tridimensionais pode ser deduzida através do princípio dos deslocamentos virtuais, onde "Para toda estrutura, o incremento de primeira ordem da energia de deformação é igual ao incremento de primeira ordem de trabalho externo". Representada pela eq. 1.  </p>
$$(1) \ \ \     [\delta_U] = [\delta_W]$$

<p style="text-align: justify;"> De forma generalizada, nos casos em que há componentes de tensão e deformação atuando em um elemento infinitesimal, sendo as parcelas de força volumétricas, superficiais ou nodais, a eq. 1 é expressa pela eq. 2:</p>
$$(2) \ \ \     \int_{0}^{V}\{\delta_{\varepsilon}\}\{\sigma\}dV = \int_{0}^{V}\{\delta_U\}\{q\}dV + \int_{0}^{\Gamma }\{\delta_U\}\{p\}d\Gamma +\{\delta_d\}\{f\}$$

Onde de acordo com Vaz (2011):
+ $$ \delta_{\varepsilon} \ e \ \delta_d$$ São grandezas cinemáticas e virtuais;
+ $$ \sigma\ e \ f$$ São grandezas estáticas e reais;

<p style="text-align: justify;">Entende-se virtual por potencial, podendo ou não ser real. </p>
Para as grandezas virtuais, vetor de deslocamentos **u**  relaciona-se com os deslocamentos nodais do elemento **d** através da eq. 3.
<p style="text-align: justify;"></p>
$$(3) \ \ \     \{\delta_U\} = [N]\{\delta_d\}$$

Sendo:
+ $$ [N]$$ Funções de interpolação ou forma do elemento. 

O vetor de deslocamentos nodais **d**  relaciona-se com as deformações no interior do elemento **$$\varepsilon$$** elemento através da eq. 4.
<p style="text-align: justify;"></p>
$$(4) \ \ \     \{\delta_\varepsilon \} = [B]\{\delta_d\}$$

Sendo:
+ $$ [B]$$ Matriz de compatibilidade cinemática. 

<p style="text-align: justify;">No caso das grandezas reais, a relação expressa na eq. 3 e 4 tomam respectivamente as eq's. 5 e 6.</p>
$$(5) \ \ \     u = Nd$$

$$(6) \ \ \     \varepsilon = Bd$$

p style="text-align: justify;">A relação entre tensão no interior dos elementos e deformação é expressa na eq. 7.</p>
$$(7) \ \ \     \sigma = C\varepsilon$$

Onde: 
+ $$ \sigma$$ Tensão no interior dos elementos;
+ $$ \varepsilon$$ Deformação no interior dos elementos;
+ $$ [C]$$ Matriz constitutiva que depende das características mecânicas do material;

p style="text-align: justify;">Substituindo as eq's. 3 a 7 na eq. 2, obtém-se a eq. 8: </p>
$$(8) \ \ \     \delta_d^t\int_{0}^{V}B^tCBdVd = \delta_d^t\left ( \int_{0}^{V}N^tq \ dV + \int_{0}^{\Gamma }N^tp \ d\Gamma + f \right )$$



[K]\{d\} = f_q + f_p + f
\\
\\
K = \int_{0}^{V}B^tCBdVd
\\
\\
f_q = \int_{0}^{V}N^tq \ dV
\\
\\
f_p = \int_{0}^{\Gamma }N^tp \ d\Gamma

















A seguir são listadas o desenvolvimento dos cálculos para determinação das matrizes de rigidez das seguintes estruturas:
1. [Viga](https://wmpjrufg.github.io/ANALISEMATRICIAL/beam.html)
2. [Treliça](https://wmpjrufg.github.io/ANALISEMATRICIAL/truss.html)
3. [Pórtico](https://wmpjrufg.github.io/ANALISEMATRICIAL/frame.html)
