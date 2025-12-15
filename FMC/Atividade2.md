## EX1:
a)$\huge p \land q$:
$\neg(\neg p \lor \neg q)$  

b)$\huge p \lor q$:
$\neg(\neg p \land \neg q)$ 

c)$\huge p \leftrightarrow q$ 
$p \rightarrow q \land q \rightarrow p$

d)$\huge p \oplus q$
$p \land \neg q \lor \neg p \land q$  

e)$\huge p \rightarrow q$ 


Tabela de karnaugh:

|  $\diagdown$   | $\overline{q}$ | $q$ |
| :------------: | :------------: | :-: |
| $\overline{p}$ |       1        |  1  |
|      $p$       |       0        |  1  |
$\overline{p} \lor q$
|
|
|f)#TODO
\000
## EX2:
a)$\huge (p \leftrightarrow q) \rightarrow (p \rightarrow q)$ 
supomos o antecessor $(p \leftrightarrow q)$ e temos que provar que $(p \rightarrow q)$. Como pela hipótese temos que p é verdadeira ou falsa, temos então que $p \rightarrow q$ é sempre verdade.

b)$\huge (p \rightarrow q) \rightarrow (p \leftrightarrow q)$
É falso basta. Basta ter $\mathcal{p}$ como falso, assim temos que o antecedente $p \rightarrow q$	é verdadeiro, porém, por sua vez $p \leftrightarrow q$ é falso, já que $p \rightarrow q \land q \rightarrow p$
não vale o lado direito. Sendo assim fica provado que a implicação não vale.

c)$\huge (p \rightarrow q) \rightarrow ((p \lor q) \rightarrow q)$ 
Temos que supor que $(p \rightarrow q)$ vale, Deste modo, temos que provar então $(p \lor q) \rightarrow q$, então supomos $p \lor q$, provaremos $q$. Por eliminação da disjunção temos $\mathcal{p}$ ou $\mathcal{q}$.
- 	Supomos então $\mathcal{p}$, temos que pela primeira hipótese $(p \rightarrow q)$ vale, então temos que $\mathcal{q}$ é verdade.
- 	Supomos agora $q$, de maneira trivial se chega a uma valida já que era o que queríamos provar.	

Assim provamos a implicação.

d)$\huge \neg (p \land q) \leftrightarrow (\neg p \lor \neg q)$ 

Abrindo a expressão em $[\neg (p \land q) \rightarrow (\neg p \lor \neg q)] \land [(\neg p \lor \neg q) \rightarrow \neg (p \land q)]$. Pela a eliminação da conjunção temos que tanto $\neg (p \land q) \rightarrow (\neg p \lor \neg q)$ quanto $(\neg p \lor \neg q) \rightarrow \neg (p \land q)$ valem. Deste modo, verificando as implicações:

- ida:
começando por $\neg (p \land q) \rightarrow (\neg p \lor \neg q)$, temos que supor $\neg (p \land q)$ e provar $(\neg p \lor \neg q)$. para chegarmos em uma contradição supomos $\neg (\neg p \lor \neg q)$, agora supomos $\neg p$ temos uma contradição já que $\neg (\neg p \lor \neg q)$ então vale p e em seguida supomos $\neg q$ analogamente ao caso anterior vale q, desta maneira temos que $p \land q$ vale e temos uma contradição em relação a $\neg (p \land q)$, logo $(\neg p \lor \neg q)$ vale.

- volta
supomos $(\neg p \lor \neg q)$  e temos que provar $\neg (p \land q)$, agora para obtermos uma contradição supomos $(p \land q)$ então temos $p$ e $q$ tornado a hipótese inicial falsa logo $\neg (p \land q)$ é verdadeira.

sabemos (não p) ou (não q)
sabemos p
sabemos q

##### TODO ver se é possível prova pela conjunção

e) 
### EX 3


