[[ponteiros topicos]]
## o que é
Um tipo de dado em c e c++ que como nome já diz aponta para algo, esse algo em sua forma concreta é um endereço de memória, ou seja o ponteiro em si tem informação apenas de onde está não o seu conteúdo, porém, é possível conferir e manipular o valor que está no endereço que o ponteiro aponta. Desta maneira, todo ponteiro tem um tamanho fixo na memória independente do tipo de dado que ele aponte, o suficiente para endereçar um endereço de memória.
Um ponto curioso é que por baixo dos panos os arrays e matrizes na verdade não passa de ponteiros disfarçados, na prática é um ponteiro apontando para o primeiro elemento do array e compilador sabe ate  aonde o ponteiro pode ir. No que se trata da matriz o principio é mesmo, no entanto, os elemento para que o ponteiro aponta para um vetor, ou seja, para outro ponteiro. 

## Funcionamento
Para utilizar um ponteiro, como qualquer outro tipo em c, primeiro você deve declara-lo dizendo o seu tipo e nomeando-o, porém, com um ```*``` antes de nome da variável. Para fazer uma atribuição assim como as outras atribuições é usando ```'='``` porem passando agora o endereço da variável que você quer guardar utilizando o ```&``` antes do nome da variável passando assim o endereço dela  

```c
#include <stdio.h>

int main()
{
	int *num;
	int a = 4;
	
	num = &a;
	
	printf("o endereco que num aponta e %x", num);
	printf("o endereco de a e  %x", &a);
	printf("o valor que esta no endereco de memoria apontado por num e %d", *num);
	

	return 0;
}
```

#### output 
```text
o endereco que num aponta e 3afb338c
o endereco de a e  3afb338c
o valor que esta no endereco de memoria apontado por num e 4
```
como é possível perceber ```nem``` e ```a```  possuem o mesmo endereço de memória e o conteúdo para para qual o ```num``` aponta é igual ```4``` que é o valor que a variável ```a```  armazenava. 
Caso queira acessar o valor que está armazenado naquela posição de memória você deve colocar um ```*``` antes da variável, no entanto, diferente de quando estávamos declarando essa sintaxe simboliza que você está pegando o valor que está naquele local de memória e a partir disso é possível fazer atribuições para deste valor para outra variáveis ou ate mesmo mudando o seu valor, fazendo isso estará afetando diretamente a variável que está naquela posição na memória.       
```c
#include <stdio.h>

int main()
{
	int a = 10;
	int *point = &a;
	int b;
	
	b = *point;

	printf("ovalor de a e %d\n", a);
	printf("o conteudo de b e %d\n", b);
	
	
	*point = 12;
	
	printf("o novo valor de point e %d\n", *point);
	printf("o novo valor de a e %d\n", a);
	
	return 0;
}
```

####  output
```text
o valor de a e 10
o conteudo de b e 10
o novo valor de point e 12
o novo valor de a e 12
```

No código acima ocorreu justamente o que foi descrito o valor da variável original ```a``` mudou já que o valor que estava em seu endereço foi alterado.



Como já se sabe uma string em c nada mais é que um vetor de caracteres, por esse motivo você pode manipular ela com um ponteiro, podendo passar por todos seus caracteres e manipula-los ao seu desejo, para percorrer basta somar um valor ao valor do endereço do primeiro elemento, como são elementos sequencias na memória você pode acessar até o ultimo caractere que o de fim de string ```\0``` 

```c
#include <stdio.h>

int main()
{
	char *palavra = "palavra";
	int i = 0;
	while (*(palavra + i) != '\0')
	{
		printf("%c", *(palavra + i));	
		i++;
	}
	
	return 0;
}
```

#### output

```text
palavra
```

Acima existe o exemplo funcional porem pouco comum de se percorrer uma string utilizado de aritmética de ponteiros para isso, é bem mais comum fazer a interação como um vetor

```c
#include <stdio.h>

int main()
{
	char *palavra = "palavra";
	int i = 0;
	while (palavra[i] != '\0')
	{
		printf("%c", palavra[i]));	
		i++;
	}
	return 0;
}
```

por baixo dos panos está sendo feita uma aritmética de de ponteiros, porem, dessa maneira fica bem mais legível e facilita a compreensão. 

### Ponteiros em função

#### Ponteiros como parâmetro de função
Os ponteiros também podem ser usados como parâmetros de funções e isso na verdade é muito útil. Para isso funcionar basta definir os parâmetros como ponteiros e passar o endereço da variável como argumento h. É usado quando quer-se usar o valor de uma certa variável e não quer gastar mais memória ou quer que as manipulações nos valores delas não sejam perdidos. Por padrão arrays são passados como endereços nos argumentos de uma função, sendo assim, qualquer alteração nele feita dento da função mudará o array fora também.

```c
#include <stdio.h>

void inverte(int *a, int tam)
{
    int b[tam];
	for (int i = 0; i < tam; i++ )
	{
		b[i] = a[(tam - 1 ) - i];
	}
    for (int i = 0; i < tam; i++ )
	{
		a[i] = b[i];
	}
}

void print_array(int *a, int tam)
{
	for (int i = 0; i < tam; i++)
	{
		printf("%d", a[i]);	
	}
    printf("\n");
}

int main()
{
	int a[] = {1, 2, 3, 4};
    printf("array origianl ");
	print_array(a, 4);	
	inverte(a, 4);
    printf("array invertido ");  
	print_array(a, 4);
	
	return 0;
}
```

#### output
```text
array origianl 1234
array invertido 4321
```
### ponteiro como retorno de função

ponteiros também podem ser parâmetros de retorno, mais especificamente um endereço pode ser o elemento de retorno 

```c
#include <stdio.h>

char* mensagem()
{
    char * a = "teste";
    return a;
}

int main()
{
    char *teste = mensagem();
    printf("%s\n", teste);

	return 0;
}
```

#### output
```text
teste
```

### Ponteiros para função

Em C também é possível apontar para uma função e isso se da da seguinte forma o ponteiro aponta para a área da memória de seguimento de código que a função está definida e podendo ser acessada por essa variável ponteiro 


```c
#include <stdio.h>

void incrementa(int *i)
{
    printf("%d\n", *i);
	(*i)++;
}

int main()
{
	int valor = 0;
	void (*point)(int*);	
	point = incrementa;
	printf("%valor = d\n", valor);
	
	point(&valor);
	point(&valor);
	point(&valor);
    printf("%novo valor = %d\n", valor);

    return 0;
}
```

#### output
```text
valor = 0
novo valor = 3
```