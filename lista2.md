# UNIFOR
**Disciplina**Raciocínio lógico algorítmico <br>
**Orientador** prof. Ricardo Carubbi

## Lista de exercícios 02

### Exercício 01 
Calcule a média de quatro números inteiros dados.

#### Fluxograma

```mermaid
flowchart TD
A([INICIO]) --> B{{"Digite o número 1:"}}
B --> C[/num1/]
C --> D{{"Digite o número 2:"}}
D --> E[/num2/]
E --> F{{"Digite o número 3:"}}
F --> G[/num3/]
G --> H{{"Digite o número 2:"}}
H --> I[/num4/]
I --> J["media = (num1 + num2 + num3 + num4)/4"]
J --> K{{A média é, media}}
K --> L([FIM]) 
```

#### Pseudocódigo 

```
ALGORTIMO Media
DECLARE num1, num2, num3, num4: REAL

INICIO
ESCREVA "Digite o número 1:"
LEIA num1
ESCREVA "Digite o número 2:"
LEIA num2
ESCREVA "Digite o número 3:"
LEIA num3
ESCREVA "Digite o número 4:"
LEIA num4
media <- (num1 + num2 + num3 + num4)/4
ESCREVA "A média é", media

FIM
```
### Exercício 02 
Leia uma temperatura dada em Celsius (C) e imprima o equivalente em Fahrenheit (F). (Fórmula de conversão: F = (9/5) * C + 32)

#### Fluxograma 

```mermaid
flowchart TD
A([INICIO]) --> B{{"Digite a temperatura em Celisus:"}}
B --> C[/C/]
C --> D["F = (9/5) * C + 32"]
D --> E{{A temperatura em Fahrenheit é, F, graus}}
E --> F([FIM])
```

#### Pseudocódigo 

```
ALGORTIMO ConverteCelsiusFarenheit
DECLARE C, F: REAL
INICIO
ESCREVA "Digite a temperatura em Celisus:"
LEIA C
F <- (9/5) * C + 32
ESCREVA "A temperatura em Fahrenheit é", F, "graus"

FIM
```
### Exercício 03 
Receba dois números reais e um operador e efetue a operação correspondente com os valores recebidos (operandos). 
O algoritmo deve retornar o resultado da operação selecionada simulando todas as operações de uma calculadora simples.

#### Fluxograma 

```mermaid
flowchart TD
A([INICIO]) --> B{{"Operações válidas: 1(soma), 2(subtração), 3(multiplicação) e 4(divisão)"}}
B --> C{{Digite uma operação:}}
C --> D[/op/]
D --> E{{Digite um número:}}
E --> F[/num1/]
F --> G{{Digite outro número:}}
G --> H[/num2/]
H --> I{op == 1}
I --FALSE--> J{op == 2}
J --FALSE--> L{op == 3}
L --FALSE--> O{op == 4}
O --FALSE--> Q{{Operação inválida!}}
Q --> R([FIM])
I --TRUE--> M[res = num1 + num2]
M --> S{{num1, + , num2, =, res}}
J --TRUE--> K[res = num1 - num2]
K --> T{{num1, - , num2, =, res}}
L --TRUE--> N[res = num1 * num2]
N --> U{{num1, * , num2, =, res}}
O --TRUE--> P{num2 != 0}
P --FALSE--> X{{Impossível dividir!}}
P --TRUE--> Z[res = num1 / num2]
Z --> V{{num1, / , num2, =, res}}
X --> R
S --> R
T --> R
U --> R
V --> R
```

#### Pseudocódigo 

```
ALGORITMO CalculadoraSimples
DECLARE op: INTEIRO; num1,num2,res: REAL
  INICIO
    ESCREVA "Operações válidas: 1(soma), 2(subtração), 3(multiplicação) e 4(divisão)"
    ESCREVA "Digite uma operação:"
    LEIA op
    ESCREVA "Digite um número:"
    LEIA num1
    ESCREVA "Digite outro número:"
    LEIA num2
    ESCOLHA
        CASO op == 1
            res = num1 + num2
            ESCREVA num1, "+", num2, "=", res
        CASO op == 2
            res = num1 - num2
            ESCREVA num1, "-", num2, "=", res
        CASO op == 3
            res = num1 * num2
            ESCREVA num1, "*", num2, "=", res
        CASO op == 4
            SE num2 != 0 ENTAO
                res = num1 / num2
                ESCREVA num1, "/", num2, "=", res
   SENAO
          ESCREVA "Impossível dividir!"
       FIM_SE
    SENAO
        ESCREVA "Operação inválida!"

    FIM_ESCOLHA

FIM
```
### Exercício 04 
Elaborar um algoritmo que, dada a idade, classifique nas categorias: infantil A (5 - 7 anos), infantil B (8 -10 anos), juvenil A (11 - 13 anos), juvenil B (14 -17 anos) e adulto (maiores que 18 anos).

#### Fluxograma 

```mermaid
flowchart TD
A([INICIO]) --> B{{"Digite a idade do aluno:"}}
B --> C[/idade/]
C --> D{idade >=5 <br>E <br>idade <= 7}
D --FALSE--> F{idade >=8 <br>E <br>idade <= 10}
F --FALSE--> G{idade >=11 <br>E <br>idade <= 13}
G --FALSE--> H{idade >=14 <br>E <br>idade <= 17}
H --FALSE--> I{idade >=18}
I --FALSE--> P{{"Digite uma idade válida!"}}
P --> Z([FIM])
D --TRUE--> Q{{Infantial A}}
F --TRUE--> K{{"Infantial B"}}
G --TRUE--> L{{Juvenil A}}
H --TRUE--> M{{Juvenil B}}
I --TRUE--> N{{Adulto}}
Q --> Z
K --> Z
L --> Z
M --> Z
N --> Z
```

#### Pseudocódigo

```
ALGORTIMO ClassificaCategoria
DECLARE idade: INTEIRO

INICIO
    ESCREVA "Digite a idade do aluno:"
    LEIA idade
    ESCOLHA
        CASO idade >=5 E idade <= 7
            ESCREVA "Infantial A"
        CASO idade >=8 E idade <= 10
            ESCREVA "Infantial B"
        CASO idade >=11 E idade <= 13
            ESCREVA "Juvenil A"
        CASO idade >=14 E idade <= 17
            ESCREVA "Juvenil B"
        CASO idade >=18
            ESCREVA "Adulto"
    SENAO
        ESCREVA "Digite uma idade válida!"

    FIM_ESCOLHA

FIM
```



