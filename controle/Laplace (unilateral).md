Para o caso particular de sinais causais, tem-se
$$X_u(s) = \int_{0}^{\infty} x(t)e^{-st}dt$$
- a transformada bilateral são equivalentes quando $x(t) = 0,  t < 0$.

- Não é possível analisar sinais/sistemas não causais com a transformada unilateral.

- Em problemas práticos,  os sinais e sistemas são causais.

- Nessa condição, uma relação um-pra-um entre $x(t)$ e $X_u(s)$,  não havendo a necessidade de especificar a RC

- $RC \rightarrow$ semi-plano à direita do polo com maior parte real.

## 1) Determine a transformada de Laplace

### a) $x(t) = u(t)$ 
$$u(t) \longleftrightarrow \frac{1}{s}$$
### b) $x(t) = u(t - 3)$

$$\large X(t-t_0) \longleftrightarrow e^{-st_0}$$
$$u(t) \longleftrightarrow \frac{1}{s}$$
$$u(t-3) \longleftrightarrow \frac{1}{s}e^{-3s}$$
### c) $x(t) = \delta(t)$

$$\frac{u(t)}{dt} = \delta(t) $$
### d) $x(t) = \delta(t - t_0),  t_0 > 0$

$$\large \delta(t - t_0) \longleftrightarrow e^{-st_0}$$

### e) $x(t) = u(t + 3)$
$$u(t + 3) \longleftrightarrow \frac{1}{s}$$
Como o sinal começa antes do zero e a transformada é unilateral ele so considera o sinal de 0 para frente.


## 2) Determine a  transformada de Laplace

### $$x(t) = cos(w_0t)u(t)$$
$$cos(\theta)= \frac{e^{+j\theta} + e^{-j\theta}}{2}$$
$$x(t) = \frac{1}{2}e^{jw_0}u(t) + \frac{1}{2}e^{-jw_0}u(t)$$
$$\mathcal{L}\{x(t)\} = \frac{1}{2} \frac{1}{s - jw_0} + \frac{1}{2} \frac{1}{s + jw_0}$$
$$=\frac{1}{2}\Bigl(\frac{s + jw_0 + s - jw_0}{s^2 + w_0^2}\Bigr)$$
$$=\frac{1}{2}\Bigl(\frac{s + \cancel{jw_0}+ s - \cancel{jw_0}}{s^2 + w_0^2}\Bigr)$$
$$=\frac{1}{\cancel{2}}\Bigl(\frac{\cancel{2}s}{s^2 + w_0^2}\Bigr)$$
$$\mathcal{L}\{x(t)\} = \frac{s}{s^2 + w_0^2}$$
forma 2:

$$e^{s_0t}x(t) \longleftrightarrow X(s - S_0)$$
jj$$x(t) = \frac{1}{2}e^{jw_0}u(t) + \frac{1}{2}e^{-jw_0}u(t)$$
$$\frac{1}{2}\frac{1}{s}\Bigg|_{s = s - jw_0} + \frac{1}{2} \frac{1}{s}\Bigg|_{s = s + jw_0}$$
$$\frac{1}{2}\Big(\frac{1}{s - jw_0} + \frac{1}{s + jw_0}\Bigr)$$
resto se desenvolve como a anterior.  


| $x(t)$                         | $X(s)$                              | $RC$            |
| ------------------------------ | ----------------------------------- | --------------- |
| $t^nu(t)$                      | $$\frac{n!}{s^{n + 1}}$$            | $$\Re(s) > 0$$  |
| $\delta(t - t_0), t_0 > 0$<br> | $$ e^{-st_0}$$                      | $$\forall s$$   |
| $t^n e^{-at}$                  | $$\frac{n!}{(s + a)^{n+1}}$$        | $$\Re(s) > -a$$ |
| $cos(w_0t)u(t)$                | $$\frac{s}{s^2+w_0^2}$$             | $$\Re(s) > 0$$  |
| $sin(w_0t)u(t)$                | $$\frac{w_0}{s^2+w_0^2}$$           | $$\Re(s) > 0$$  |
| $e^{-at}cos(w_0t)u(t)$         | $$\frac{s + a}{(s + a)^2 + w_0^2}$$ | $$\Re(t) > -a$$ |
| $e^{-at}sin(w_0t)u(t)$         | $$\frac{w_0}{(s + a)^2 + w_0^2}$$   | $$\Re(t) > -a$$ |

## 3) $x(t) = e^{-at}sin(w_0t)u(t)$

$\large \sin(\theta)=\large\frac{e^{j\theta} - e^{-j\theta}}{2j}$
$$x(t)  = e^{-at}\Big[\frac{1}{2j}\Bigl(e^{+jw_0} - e^{-jw_0}\Bigr)\Big]u(t)$$
$$\mathcal{L}\{x(t)\} = e^{-at} \frac{1}{2j}\Bigl(\frac{1}{s}\Bigg|_{s = s -s jw-0} - \frac{1}{s}\Bigg|_{s + jw_0}\Bigr)$$

$$e^{-at} \frac{1}{2j}\Bigl(\frac{1}{s - jw_0} - \frac{1}{s + jw_0}\Bigr)$$
$$e^{-at} \frac{1}{2j} \Bigl(\frac{\cancel{s} + jw_0 - \cancel{s} + jw_0}{s^2 + w_0^2}\Bigr)$$
$$e^{-at} \frac{1}{\cancel{2j}} \frac{\cancel{2j}w_0}{s^2 + w_0^2}$$
$$\large e^{-at} \frac{w_0}{s^2 + w_0^2}\Bigg|_{s = s + a}$$
$$ \frac{w_0}{(s + a)^2 + w_0^2 }$$

# Propriedades

## 1) Linearidade:

$$ax_1(t) + bx_2(t) \longleftrightarrow aX_1(s) + bX_2(s)$$
 ## 2) escalonamento o tempo:
$$x(at) \longleftrightarrow \frac{1}{a} X\Bigl(\frac{s}{a}\Bigr) $$ p/ a > 0 

## 3) Deslocamento no tempo:

$$x(t - t_0) \longleftrightarrow e^{-st_0}X(s)$$
$t_0 > 0$ 

## 4) Deslocamento no domínio s:

$$e^{s_0t}x(t) \longleftrightarrow X(s - s_0)$$
## 5) Convolução:
$$x(t)*y(t) \longleftrightarrow X(s)Y(s)$$
## 6) Diferenciação no domínio do tempo:

$$-tx(t) \longleftrightarrow \frac{dX(s)}{ds}$$
## 7) Diferenciação no domínio do tempo:
$$\frac{dx(t)}{dt} \longleftrightarrow sX(s) - x(0^-)$$

## 8) Integração no domínio do tempo:
$$\large \int_{-\infty}^t x(\tau)d\tau \longleftrightarrow \frac{X(s)}{s} + \frac{\int_{-\infty}^{0^-} x(\tau)d\tau}{s}$$
## 9) Teorema do valor inicial:
se $x(t) = 0$ para $t<0$ e $M < N$, tem-se que  

$$x(0^+)  = lim_{s}{}$$