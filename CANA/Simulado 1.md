### 2)
--é da prova 1 esse aqui

| 1   | 50  | 2   | 40  | 3   | 30  | 5   | 7   | 10  | 4   |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

dividindo por 2: cai no em $A[5]$ que é 3

primeira parte: 

| 1   | 50  | 2   | 40  | 3   |
| --- | --- | --- | --- | --- |

| 30  | 5   | 7   | 10  |
| --- | --- | --- | --- |


--agora sim é da do simulado

## 2
$A[i...n]$ existe i tal que $A[i] = i$ ?
	$[2, 4, 4, 5, 6, 7 , 9, 11, 12, 20, 23,24,27,58,80]$
```text
busca-binaria(A[i..j])	
	se i > j
		retorne -1
	
	m <- (i + j) / 2
	se A[m] = m
		retorna m
	se nao se A[m] < m 
		busca-binaria(A[m+1]..j)
	se nao
		busca-binaria(i...A[m - 1])
```

1 3 4    5 6 10      12 15 16


1 3 