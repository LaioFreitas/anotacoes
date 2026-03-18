## 1)
RISC:
- tem um conjunto de instruções mais simples e reduzido.
- instruções de tamanho uniforme e são executadas rápidas em único ciclo de clock.
- só é possível referenciar memória de duas maneiras diferentes com o LOAD/STORE 
- compilador para essa arquitetura deve ser mais trabalhado pois o hardware e instruções são mais simples.
- pipeline reduzido.
- instruções de proposito geral
- eficiência energética;
- alto uso de registradores assim acessando pouco a memória.
CISC:
- Conjunto de instruções mais complexo podendo executar coisas mais alto nível e possuir tamanho variável.
- varias formas de referenciar a memória
- pipeline robusta.
- hardware mais complexo podendo executar tornado o compilador mais simples de implementar pois as instruções mais complexar são quebrada a nível de nível de hardware em operações mais simples. 
- numero de registradores reduzido dependo mais de acesso a memoria principal.
- maior consumo de energia e dissipação de calor
- instrução pode executar varia operações ao meso tempo.

## 2)
A principal diferença está em como elas lidam com os barramentos de dados e instrução ou seja a comunicação interna do processador.
no von neumann a memoria de dados de instriução e dados é unificada e os  barramentos também são compartilhado 
- harvard a memmoria para dados e instrução são separa eo barramentos também são separados permitindo a busca de dados e instruções ao mesmo tempo deixando o designer mais complexo.


