 k-ésimo elemento
 entradaq - conjunto com n elementos
		 - inteiro k

saída: k-ésimo elemento

#### algorítimo: ordenação O($nlog(n)$)
k=1 0(n)   k=n O(n)   k=$\frac{n}{2}$ (mediana)

![[imagem 1 -problema de selecao.excalidraw]]
```text
Selecao(A, p, r, k)
	se (p = r)
		retorna a[r]
	pivot <- A[r] (usar uma recursao para encontra um bom pivo)
	q <- particiona(A, p, r, pivot)
	se (k = q)
		return A[q]
	se q > k 
		return selecao(A, p, q-1, k)
	se nao
		return Selecao(A, q + 1, 1, k - q)
```


1) divide os n elementos da entrada em $\frac{n}{5}$ grupo de 5 elementos cada
![[image2- problema de selecao.48.44.excalidraw]]


2) ordena cada grupo

3) forma um vetor de tamanho $\frac{n}{5}$ com as mediana de cada grupo
![[image3-problema de selecao.excalidraw]]

ate aqui o tempo O(n)
3) encontra a mediana x do vetor de medianas (usar esse elemento como pivot) chama recursivamente

##### curiosidade: 
tempo do algorítimo = $T(n) = T(\frac{n}{5}) + T(\frac{7n}{10}) + n$  
que da O(n)

![[image4- problema da seleção.excalidraw]]

