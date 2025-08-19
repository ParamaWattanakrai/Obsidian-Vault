$k$ is the artificial neuron
$m$ is the number of input
$$\begin{flalign}
y_k=\phi(\sum\limits^m_{i=0}w_{kj}x_j)&&
\end{flalign}$$
Usually, the input $x_0$ is assigned the value +1, which makes it a bias input with $w_{k0}=b_k$
$$\begin{flalign}
y_k=\phi(\sum\limits^m_{i=1}w_{kj}x_j+b_k)&&
\end{flalign}$$