# slide2-LPI

## exercicio 2
Faça um programa que leia dois valores e exiba o maior valor lido.

- Dicas:
    - `printf`
    - `scanf`
    - `if`
### Resposta:

```c
#include <stdio.h>

int main(int x , int y) {
	printf("digite o primeiro número: \n");
	scanf("%d" , &x);
	printf("digite o segundo número: \n");
	scanf("%d" , &y);
	if (x > y) {
		printf("o maior número é : %d\n" , x);
	} else {
		printf("o maior número é : %d\n" , y);
	}
    return 0;
} 
```

## exercicio 3
Um aluno de LP1 está indo aos Estados Unidos e quer comprar um celular novo.
Ele não quer gastar mais do que 1000 reais. Um dólar está custando 3.17 reais.
Faça um programa que leia o preço de um celular em dólares e, caso seja um bom
negócio, escreva `BOM NEGÓCIO`.
### Resposta:
```c
#include <stdio.h>

void main(int x , bool z) {
	printf("Qual o valor em dolar? \n");
	scanf("%d" , &x);
	z = (x * 3.17) < 1000;
	if (z == 1) {
		printf("Bom negocio, valor em real: %.2f R$ \n" , (x * 3.17));
	} else {
		printf("Pessimo negocio, valor em real: %.2f R$ \n" , (x * 3.17));
	}
}
```
## exercicio 4
Agora o aluno alugou um carro.
Ele está preocupado com o limite de velocidade, mas não entende muito bem
o sistema de milhas por hora (mph).
Ele pretende manter sempre uma velocidade entre 80 e 100 quilômetros por hora
(kph).
Sabe-se que que 1 milha tem aproximadamente 1.6 quilômetros.
Crie um programa que leia a velocidade atual do carro em mph e escreva na tela
`ACELERE`, `DESACELERE` ou `MANTENHA`.
### Resposta:
```c
#include <stdio.h>
#include <stdlib.h>

void main(int vel) {
	printf("Qual a velocidade atual do carro em mph? \n");
	scanf("%d" , &vel);
	if ((vel * 1.6) < 80){
		printf("ACELERE, velocidade atual em kph: %.1f \n" , (vel * 1.6));
	} else if ((80 <= (vel * 1.6)) && ((vel * 1.6) <= 100)){
		printf("MANTENHA, velocidade atual em kph: %.1f \n" , (vel * 1.6));
	} else{
		printf("DESACELERE, velocidade atual em kph: %.1f \n" , (vel * 1.6));
	}
}
```
## exercicio 5
Faça um programa que leia números continuamente até que seja digitado `0`.
Ao final, o programa deve exibir a soma de todos os números lidos.

- Dicas:
    - `while`
### Resposta:
```c
#include <stdio.h>

void main(int x , int soma) {
	x = 1;
	soma = 0;
	while (x != 0) {
		printf("digite um número: \n");
		scanf("%d" , &x);
		soma = (soma + x);
	}
	printf("soma de todas as entradas: %d \n" , soma);
}
```
## exercicio 6
Faça um programa que leia um número `N` e calcule o somatório a seguir:

<img width="117" height="148" alt="sum" src="https://github.com/user-attachments/assets/49b4aa8b-40ff-448b-beb9-43ab1265be80" />

### Resposta:
```c
#include <stdio.h>
#include <stdlib.h>

void main(int n , int soma , int i) {
	soma = 0;
	printf("Digite o n do somatorio: ");
	scanf("%d" , &n);
	for (i = 1 ; i < n + 1 ; i++){
		soma = soma + (i*i);
	}
	printf("resposta do somatorio: %d \n" , soma);
}
```
## exercicio 7
O Campeonato Brasileiro está na reta final com 20 times na disputa.

Uma vitória vale 3 pontos, um empate vale 1 ponto e uma derrota vale 0 pontos.
Escreva um programa que, para cada time, leia o nome (ou um identificador
numérico), número de vitórias, número de empates e número de derrotas.

Ao final, o programa deve escrever os nomes (ou identificadores) dos times com
mais e menos pontos até o momento.
### Resposta:
```c
#include <stdio.h>

void main(char time_maior , char time_menor , char time , int ponto_maior , int ponto_menor , int ponto , int vitoria , int empate , int perda , int i){
	ponto_maior = 0;
	ponto_menor = 120;
	for (i = 0 ; i < 20 ; i++){
		printf("Qual o nome do time? ");
		scanf(" %c" , &time);
		printf("Quantas vitórias? ");
		scanf("%d" , &vitoria);
		printf("Quantos empates? ");
		scanf("%d" , &empate);
		printf("Quantas derrotas? ");
		scanf("%d" , &perda);
		ponto = (vitoria * 3) + empate;
		if (ponto > ponto_maior){
			time_maior = time;
			ponto_maior = ponto;
		}
		if (ponto < ponto_menor){
			time_menor = time;
			ponto_menor = ponto;
		}
	}
	printf("Melhor time: %c , pontuação: %d \n" , time_maior , ponto_maior);
	printf("Pior time: %c , pontuação: %d \n" , time_menor , ponto_menor);
}
```
## exercicio 8
- Ler dois números n1 e n2
- Exibir todos os números entre n1 e n2
- Fazer em Python e em C
### Resposta C:
```c
#include <stdio.h>


void main(int n1 , int n2 , int i) {
	printf("digite n1: ");
	scanf("%d" , &n1);
	printf("digite n2: ");
	scanf("%d" , &n2);
	for (i = n1 ; i < n2 + 1 ; i++) {
		printf("%d \n" , i);
	}
	
}
```
### Resposta PY:
```py
n1 = n2 = soma = 0
n1 = int(input("Digite n1: "))
n2 = int(input("Digite n2: "))
for i in range(n1 , (n2 + 1)):
    print (i)
```
