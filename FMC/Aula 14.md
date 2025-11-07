base : 0 
onde n é um número natural
$S_0 = 0$
$S_i + 2(i + 1) - 1$
-----
solução
$S_n = n²$ 
-----
corretude:

Prova (por indução):
- Base:
temos que provar $S_0 = 0$
é evidente já que 
$S_0 = 0² = 0$  
- passo:
$S_n = n²$ (hipótese indutiva)
temos que provar que $\forall n \in \mathbb{N},$ se $S_n = n²$, então $S_{n + 1} = (n + 1)²$ 
De fato, seja n um natural qualquer e suponha que $S_n = n²$ temos que mostra que $S_n = (n + 1)²$. Temos:
$$S_{n + 1} = S_n + 2(n +1) -1$$
como temos a hipótese indutiva vele:
$$n² +  2(n + 1) - 1$$
$$n² +  2n +  1 $$
$$(n + 1)²$$
provando como desejado.
### 2)  encontrar a formula do somatório de uma PG 
a) Encontre uma fórmula para a soma dos  n primeiros termos de uma progressão geométrica de razão $r > 1$.
$$a_0$$
$$a_1 = a_0r$$
$$a_2 = a_1r$$
$$.....$$
b)Prove a corretude da Fórmula.


a)
$$a_2 = (a_0r)r$$
$$a_3 = ((a_0r)r)r$$
$$a_3 = a_0r³$$
temos então que o enésimo termo da progressão é dado por:  
$$a_n = a_0r^n$$
para soma então
$$
\begin{cases}
	S_0 = a_o \\
	S_{i + 1} = S_i + a_{i + 1}\\	
\end{cases}
$$
ideia:
$$S_n = a_0+a_0r+a_0r²...+a_0r^n$$ 
$$S_{n+1} = a_0+a_0r+a_0r²...+a_0r^n + a_0r^{n+1}$$
$$S_{n+1} = a_0 + r(a_0 + a_0r + a_0r²...a_0r^n)$$
por definição temos que $a_0 + a_0r + a_0r²...+a_0r^n$ é o próprio $S_n$ logo:
$$S_{n+1} = a_0 + rS_n$$
$$S_{n+1} = S_n + a_{n+1}$$