a) $\forall ABC, A \subseteq B \rightarrow ((\neg C \subseteq B) \rightarrow (\neg C \subseteq A))$

~~Não vale. Pegando A, B e $\neg$C valendo $\{ 1 \}, \{1, 2\}$ e $\{1, 2\}$ respectivamente
observamos que tomamos $A \subseteq B$ como verdade e $\neg C \subseteq B$ também e a inda assim chegamos em um caso que $\neg C \subseteq A$ não vale tornado a afirmativa inteira falsa.~~  


b) $\forall CDE, ((C \subseteq D) \lor (C \cup D \subseteq E)) \rightarrow (C \setminus D \subseteq E)$

Supomos C,D e E qualquer e $((C \subseteq D) \lor (C \cup D \subseteq E))$ temos que provar que $(C \setminus D \subseteq E)$. Pela hipótese temos dois casos, e temos que fazer analise de casos
- caso 1 $(C \subseteq D)$: 
	como $C$ é subconjunto de $D$ então $C \setminus D = \varnothing$, deste modo, temos que $\varnothing \subseteq E$ o que é verdade pois pela definição de subconjunto temos que $\forall e, (e \in \varnothing) \rightarrow e \in E$ deste modo, por vacuidade a afirmação $\varnothing \subseteq E$ é verdadeira.  
- caso 2 $(C \cup D \subseteq E)$: 	
	
- resposta 2
	supomos então C, D e E qualquer e $((C \subseteq D) \lor (C \cup D \subseteq E))$ temos que provar $(C \setminus D \subseteq E)$. Para isso supomos um $e$ sendo um elemento qualquer e $e \in C \land e \notin D \land e \notin E$ e tem quer ser feito uma analise de casos.
	- caso 1 $C \subseteq D$: pela definição de de subconjunto temos que todo elemento de C também pertence a D, no entanto pela hipótese anterior o elemento $e$ pertence a C e não pertence a D, logo obtemos uma contradição, então, $C \setminus D \subseteq E$ vale. 
	
	- caso 2 $C \cup D \subseteq E$: pela definição de união temos que um elemento qualquer pertence a C ou a D e novamente pela hipótese(premissa) $e \in C \land e \notin D \land e \notin E$ obtemos uma contradição já que $e \in C$ por sua vez $e \in C \cup D$ que é subconjunto de E, sendo assim, não exite $e$ que satisfaça $e \in C \land e \notin D \land e \notin E$, logo, $C \setminus D \subseteq E$ vale.
	
	como foi possível chegar ao mesmo resultado usando a eliminação da conjunção a afirmação é verdadeira. 
c) $\forall XYZ,  X \subseteq Y \cup Z \rightarrow (X \cup  Y) \setminus Z = Y \setminus Z$  

Supomos X, Y e Z qualquer e que $X \subseteq Y \cup Z$ vale, temos que provar $(X \cup Y) \setminus Z = Y \setminus Z$. Pela definição de igualdade ~~e pela de e pela diferença de conjuntos temos~~ $\forall e, e \in (X \cup Y) \setminus Z \leftrightarrow e \in Y \setminus Z$ ~~e pela definição de diferença de conjuntos pegamos um $e$ qualquer com a seguinte propriedade $e \in (X \cup Y) \land e \notin Z$~~, provemos então a ida e a volta.
- **ida** $(X \cup Y) \setminus Z \rightarrow Y \setminus Z$: supomos o antecedente e um $e$ qualquer temos que provar $Y \setminus Z$, para isso faremos uma analise de casos já que pela definição de união temos que $e$ está em X ou em Y.
	- caso 1 $e \in X$: como pela hipótese inicial X é subconjunto de $(Y \cup Z)$ novamente temos dois casos possíveis, porem, pela premissa de $e \in (X \cup Y) \land e \notin Z$ $e$ so pode está em Y, sendo assim, $Y \setminus Z$ vale.
	- caso 2 $e \in Y$: de maneia trivial novamente pela premissa $e \in Y \land e \notin Z$, $e$  pertence a $Y \setminus Z$ 

	como foi possível chegar ao mesmo resultado com os dois casos então $Y \setminus Z$ é verdadeiro  
-  **volta** $Y \setminus Z \rightarrow (X \cup Y) \setminus Z$: Supomos $Y \setminus Z$ e temos que provar $(X \cup Y) \setminus Z$, pela hipótese anterior $e \in Y \land e \notin Z$ então $e$ pertence a $X \cup Y$ e como não pertence a $Z$ então $(X \cup Y) \setminus Z$ vale. 
provando assim a implicação como um todo.  

d) $\forall MNO, (M \cap N = N \land N = N \cup O) \rightarrow O \setminus M = \varnothing$ 

suponha M, N e O qualquer e que vale $(M \cap N = N \land N = N \cup O)$, temos que provar $O \setminus M = \varnothing$. pela hipótese vale $M \cap N = N$ e $N = N \cup O$, sendo assim, pela definição de extensionalidade da igualdade temos um $e$ qualquer que pertence a $M \cap N$ tem que pertence também a $N$ e por sua vez, pela definição de interseção $e$ pertence a $M$ e a $N$, logo, como expressão vale $M = N$. Em $N = N \cup O$ novamente pela extencionalidade da igualdade um elemento qualquer $e$ que pertence a $N$ tem que pertencer a $N \cup O$ e vice e verça, pela definição de união $e$ pertence a $N$ ou a $O$ de forma trivial se $e$ pertencer a $N$ no entanto se $e$ pertencer a $O$ como $N = N \cup O$ vale, o único jeito disso ser verdade é $O = N$. Tendo as informações que $N = M$ e $O = N$ se for feito $O \setminus M$ o resultado e o conjunto $\varnothing$ como queríamos provar