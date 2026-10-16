# Dicionário Python

## Entrada/Saída

Para capturarmos um valor inserido pelo usuário, atribuimos a uma variável a função "**_input()_**"

### Entrada
```python
# Entradas simples

txt = input() # --> Strings
num = int(input()) # --> Números

# Entradas Múltiplas

y = input().split() # --> Remove os espaços e transforma em array
x, y = map(int, input().split()) # --> Formato numérico
x, y = list(map(int, input().split())) # --> Formato de Array numérico
```

Para mostrarmos um valor utilizamos a função "**_print()_**"

### Saída
```python
# Saída simples
print('Banana!')
```

```python
# Exemplo utilizando "f" para manipulação da saída

a = 10
print(f'O jogador de camisa número {a}')

# É possível manipular o valor da variavél dentro das chaves
print(f'O jogador de camisa número {2*a}')

# Adicionando casas decimais
print(f'O refrigerante custa R${a:.2f}') # --> R$ 10.00
```

## Variáveis e tipos de dados
### Númericos
- Inteiros
  - Pode ser negativos ou positivos (Ex: -67, 67)
-Decimais
  - Número com casas decimais (Ex: 6,7)
### String
- Conjuto de caracteres, frases ou textos
- Delimitadas por '' ou ""
### Boleano
- Pode assumir dois valores: verdadeiro (True) ou falso (False)
### Array
São definidos usando colchetes para delimitar a lista e utiliza-se vírgulas para a separação dos elementos

## Operadores
- Aritméticos
  - '+' = soma
  - '-' = subtração
  - '*' = multiplicação
  - / = divisão real
  - // = divisão inteira (retorna um número inteiro)
  - % = resto da divisão
  - ** = potência
  - () = agrupar expressões

- Lógicos
  - and - as duas condições devem ser verdadeiras
  - or - pelo menos uma das condições deve ser verdadeira 
  - not - inverte o valor do elemento

- Relacionais
  - '>' - maior
  - '>=' - maior igual
  - '<' - menor
  - '<=' - menor igual
  - == - igual (para igualdade)
  - != - diferente
 
## Estruturas condicionais
Estruturas de decisão

```python
# Exemplo
a = int(input('Digite um número entre 0 e 5'))

if a > 2:
  print("O número ", a, " é maior que 2")
elif a == 2:
  print("O número informado é 2")
else:
  print("O número ", a, " é menor que 2")
```

## Estruturas de repetição

#### FOR
```python
for i in range(1, 10):
  print(i)

```
