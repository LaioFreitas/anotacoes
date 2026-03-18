#  Indução matemática

### preliminar
raciocínio dedutivo X raciocínio indutivo(de particular para o geral)

### 1) Indução matemática
para toda propriedade p, se:
a) p(0),e 
b) $\forall n \in \mathbb{N}, p(n) \rightarrow p(n+1)$ então, $\forall n \in \mathbb{N}, p(n)$

(base $\land$ passo) $\rightarrow$ conclusão

## 2) exemplo: soma de progressão aritmética 
Quanto vale 1 + 2 + 3 ... +n

Observe: 
$Sn = 1 + 2 + 3 + ... + n - 1 + n$
+
$Sn = n + n - 1 + ..... 2 + 1$
----------
$2S_n = (n+1) + (n+1)+ ... + (n+1)+(n+1)$ "n termos"

$$2S_n = (n+1)n$$
$$2S_n = \frac{(1 + n)n}{2}$$
## 3) Tornando o argumento preciso:
a) A sequência:
	$a_i=i, \forall i \in \mathbb{N}$
	$a_0 = 0$
	$a_1 = 1$
	$a_2 = 2$, etc
b)O somatório

$$\begin{cases} S_0 = a_0 \\ S_{i+1}  = S_i + a_{i+1}, \forall i \in \mathbb{N} \end{cases}$$
$S_n= a_0$
$S_1=S_0 + a_1$ 
$S_2=  S_1 + a_2 = a_0 + a_1 + a_2$
etc

c) Teorema: $\forall n \in \mathbb{N},\large S_n=\frac{(a_0+an)(n+1)}{2}$

__prova__
seja p(n) a afirmação $\large S_n = \frac{(a_0+a_n)(n+1)}{2}$ 

Nós provaremos que,  $\large \forall n \in \mathbb{N}, p(n)$, por indução: 

- Base: "tqmq" p(0), isto é, que $\large S_0=\frac{(a_0+a_0)(0+1)}{2}$ que vale pois $\large  \frac{(a_0+a_n)(n+1)}{2}=a_0$ e, por definição, $S_0=a_0$, o que conclui a base.
- \_passo\_: "tqmq" , $\forall n \in \mathbb{N}, p(n) \rightarrow p(n+1)$. Seja então n um natural qualquer e suponha que vale p(n), ou seja, que $\large S_n = \frac{(a_0 + a_n)(n+1)}{2}$ "tqmq" p(n+1),  ou seja, que $\large S_{n+1}= \frac{(a_0+a_{n+1})(n+1+1)}{2}$ 
de fato, temos:
$$S_{n+1} = S_n + a_{n+1}$$
$$= \frac{(a_0 + a_n)(n+1)}{2} + a_{n+1}$$ 
$$ = \frac{a_0 (n+1)+a_n(n+1)+2a_{n+1}}{2}$$
$$=\frac{n(n+1)+2(n+1)}{2}$$
$$=\frac{(n+1)(n+2)}{2}$$
$$=\frac{(a_0+a_{n+1})(n+2)}{2}$$
