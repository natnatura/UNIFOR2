# UNIFOR
**Disciplina**Raciocínio lógico algorítmico <br>
**Orientador** prof. Ricardo Carubbi
## Lista de exercícios 03

### Exercício 01
Atualize o algoritmo para determinar se um número inteiro e positivo é par ou ímpar, usando uma laço condicional para aceitar apenas números maiores ou iguais a zero. 

#### Fluxograma

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite um número:}}
B --> C[\num\]
C --> D{num < 0}
D --FALSE--> E[resto = num % 2]
E --> H{resto == 0}
H --FALSE--> I{{O número é impar!}}
H --TRUE--> J{{O número é par!}}
I --> Z([FIM])
J --> Z
D --TRUE--> F{{Digite um número maior ou igual a zero:}}
F --> G[/num/]
G --LOOP--> D
```

#### Pseudocódigo 

```
ALGORTIMO verifica_par_impar
DECLARE num, resto: INTEIRO

INICIO
	ESCREVA "Digite um número: "
	LEIA num
	ENQUANTO num < 0 FAÇA
		ESCREVA "Digite um número maior ou igual a zero:"
		LEIA num
    FIM_ENQUANTO
	SE num >= 0 ENTAO
		resto ← num % 2
		SE resto == 0 ENTAO
			ESCREVA "O número é par!"
		SENAO
			ESCREVA "O número é impar!"
        FIM_SE
	SENAO                               
		ESCREVA "O número deve ser postivo!"
    FIM_SE

FIM
```
### Exercício 02 
Faça um algoritmo que exiba na tela uma contagem de 0 até 30, exibindo apenas os múltiplos de 3.

#### Fluxograma 

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite a quantidade de números: }}
B --> C[\n\]
C --> E[[i=0 ATÉ n-1 PASSO 3]]
E --> G([FIM])
E --> F{{ESCREVA i}}
F --LOOP--> E
```

#### Pseudocódigo

```
ALGORTIMO MultiploTres
DECLARE n: INTEIRO

INICIO
	ESCREVA "Digite a quantidade de números:"
	LEIA n
	PARA i DE 0 ATÉ n-1 PASSO 3 FAÇA
		ESCREVA i
    FIM_PARA
FIM
```
### Exercício 03 
Dada uma sequência de números inteiros, calcular a sua soma. 
Por exemplo, para a sequência {12, 17, 4, -6, 8, 0}, o seu programa deve escrever o número 35.

#### Fluxograma 1

```mermaid
flowchart TD
A([INICIO]) --> B{{"Digite a quantidade de números:"}}
B --> C[\n\]
C --> D[i = 1]
D --> E[soma = 0]
E --> F{i <= n}
F --FALSE--> G{{A soma dos número é, soma}}
G --> L([FIM])
F --TRUE--> H{{Digite o número, i,:}}
H --> I[\num\]
I --> J[soma = soma + num]
J --> K[i = i + 1]
K --LOOP--> F
```

#### Fluxograma 2
```mermaid
flowchart TD
A([INICIO]) --> B{{"Digite a quantidade de números:"}}
B --> C[\n\]
C --> D[soma = 0]
D --> E[[i=1 ATE n, PASSO 1]]
E --FALSE--> F{{A soma dos número é, soma}}
F --> L([FIM])
E --TRUE--> G{{Digite o número, i,:}}
G --> H[\num\]
H --> I[soma = soma + num]
I --LOOP--> E
```

#### Pseudocódigo 

```
ALGORITMO SomaValores
DECLARE n,i: INTEIRO; soma,num: REAL

INICIO
	ESCREVA "Digite a quantidade de números:"
	LEIA n
	    soma <- 0
	    i <- 1
	ENQUANTO i <= n FAÇA
		ESCREVA "Digite o número", i,":"
		LEIA num
		soma <- soma + num
		i <- i + 1
    FIM_ENQUANTO
	ESCREVA "A soma dos número é", soma
FIM
```
### Exercício 04 
Escreva um programa que leia a nota de diversos alunos, até que seja digitada uma nota negativa. 
Nesse momento, ele mostra a média aritmética de todas as notas lidas e quantas notas foram lidas. 
Ex. Foram lidas 14 notas. A média aritmética é 6.75!

#### Fluxograma

```mermaid
flowchart TD
A([INICIO]) --> B[/soma/]
B --> C[/cont/]
C --> D{{"Digite a nota do aluno (nota negativa finaliza): "}}
D --> E{nota >= 0}
E --FALSE--> F{cont > 0}
F --FALSE--> Z([FIM]) 
F --TRUE--> G[media = soma / cont]
G --> H{{Foram lidas, cont, notas. A média aritmética é, media!}}
H --> Z
E --TRUE--> I[soma += nota]
I --> J[cont += 1]
J --> K{{"Digite a nota do aluno (nota negativa finaliza): "}}
K --LOOP-->  E
```

#### Pseudocódigo

```
ALGORTIMO QuantMedia
DECLARE nota, soma, media: REAL; cont: INTEIRO

INICIO
	ESCREVA "Digite a nota do aluno (nota negativa finaliza): "
	LEIA nota
	soma <- 0
	cont <- 0
	ENQUANTO nota >= 0 FAÇA
		soma <- soma + nota
		cont <- cont + 1
		ESCREVA "Digite a nota do aluno (nota negativa finaliza): "
		LEIA nota

	FIM_ENQUANTO
	SE cont > 0 ENTÃO
		media <- soma / cont
		ESCREVA "Foram lidas", cont, "nota(s). A média aritmética é", media
    FIM_SE

FIM
```


    
```

