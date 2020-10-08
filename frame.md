#Matriz de rigidez Pórtico

<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script> <script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

\documentclass[journal]{IEEEtran}
\usepackage{nccmath}

\usepackage{lipsum} % for generating dummy text, not use in real document

\begin{document}
\lipsum[11]
\begin{align}
            x   & = \frac{-b\pm\sqrt{b^2-4ac}}{2a}          \label{eq1} \\
\frac{d}{dx}r^n & = nx^{n-1}                                \label{eq2} \\
\mathrm{Length} & = \int_{a}^{b}\sqrt{[f't]^2+[g't]^2}dt    \label{eq3}
\end{align}
or
\begin{fleqn}
\begin{equation}\label{eq1}
x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}
\end{equation}

\begin{equation}\label{eq2}
\frac{d}{dx}r^n=nx^{n-1}
\end{equation}

\begin{equation}\label{eq3}
Length=\int_{a}^{b}\sqrt{[f't]^2+[g't]^2}dt
\end{equation}
\end{fleqn}
\lipsum[11]

\end{document}
