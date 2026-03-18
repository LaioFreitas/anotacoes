# relação de recorrência

1. exemplo(cont): Torres de Hanói.

quantos movimentos são suficientes para levar os n discos da torres/pinos 1 à torre 3? 

 Com alguma experimentação, é possível chegar à seguinte estratégia de solução:
se n > 1
  > 1. recursivamente, levar os n-1 menores discos da torre de origem (no início, a torre 1) à torre auxiliar (no inicio, a torre 2);
  > 2. levar o discos maior à torre de destino (no início, a torre 3);
  > 3. recursivamente, levar os n-1 discos menores da torre auxiliar à torre final.

se n=1
> 5. move o disco da torre de origem à torre de destino

A observação-chave é que os passos 1 e 3 podem ser realizados "sem preocupação" em relação ao disco maior, pois quaisquer discos podem ser colocados acima dele 
	É fácil perceber que, seguindo esse algorítimo, o número de movimentos realizado é.
  