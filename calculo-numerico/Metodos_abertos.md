# 1- Método de Newton-Raphson:

_i)_ uma das condições de convergência e que $|\varphi'(x)| <= M < 1, \forall x \in I$, onde $I$ e um intervalo centrado na raiz;     

_ii)_ a convergência do método sera mais rápida quando menor for $|\varphi'(\xi)|$.

O que o método de Newton faz, na tentativa de acelerar a convergência é escolher uma função de interação tal que $\varphi'(x) = 0$.

Então, dada $\varphi(x) = 0$ e partido da forma geral de $\varphi(x)$, queremos obter $A(x)$ tal que $\varphi'(\xi) = 0$. 

$$\varphi(x) = x + A(x)f(x)$$ $$\varphi'(x) = 1 + A'(x)f(x) + A(x)f'(x)$$
$$\varphi'(\xi) = 1 + A'(\xi)f(\xi) + A(\xi)f'(\xi)$$
como $f(\xi) = 0$ 
$$\varphi'(\xi) = 1 + A(\xi)f'(\xi)$$
Assim fazendo $\varphi'(\xi) = 0$  
$$1 + A(\xi)f'(\xi) = 0$$
$$A(\xi) = \frac{-1}{f'(x)}$$
logo tendo
$$A(x) = \frac{-1}{f'(x)}$$
sendo assim dada $f(x)$, a função de interação $\varphi(x) = x - \frac{f(x)}{f'(x)}$ sera de tal forma que $\varphi'(x) = 0$ como podemos verificar:

$$\varphi'(x) = 1 - \frac{(f'(x)^2 - f(x)f''(x)}{f'(x)^2} = \frac{f(x)f''(x)}{f'(x)^2}$$

como $f(\xi) = 0$, $\varphi'(\xi) = 0$ tendo $f'(\xi) \ne 0$, a sequencia {$X_k$} sera determinada por $x_{k+1} = x_k + \frac{f(x_k)}{f'(x_k)}$ 

## motivação geométrica:

O método de Newton e obtido geometricamente da seguinte forma:

dado o ponto ($x_k$, $f(x)$) trocamos a reta $L_k(x)$ tangente a curva neste pontos 