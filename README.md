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

- Operadores de pertencimento
  - `in` - Verifica se um elemento pertence a uma sequência.
  - `not in` - Verifica se um elemento não pertence a uma sequência.

```python
frutas = ['maçã', 'banana', 'uva']

print('banana' in frutas) # --> True
print('laranja' not in frutas) # --> True
```
 
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

O comando `for` é utilizado para percorrer uma sequência de elementos ou repetir um bloco de código determinado número de vezes.

**range()**

Gera uma sequência de números, utilizada principalmente em estruturas de repetição.

```python
# range(início, fim, intervalo)

for i in range(1, 10, 2):
    print(i)

# Resultado: 1, 3, 5, 7, 9
```

#### WHILE

Executa um bloco de código enquanto uma condição for verdadeira.

```python
a = 0

while a < 5:
    print(a)
    a += 1
```

**break**

Interrompe a execução de uma estrutura de repetição.

```python
for i in range(10):
    if i == 5:
        break
    print(i)

# Resultado: 0, 1, 2, 3, 4
```

**continue**

Interrompe a execução atual e passa para a próxima repetição.

```python
for i in range(5):
    if i == 2:
        continue
    print(i)

# Resultado: 0, 1, 3, 4
```

## Funções para números

Funções utilizadas para realizar operações e manipulações numéricas.

**abs()**

Retorna o valor absoluto de um número, ou seja, seu valor sem considerar o sinal.

```python
print(abs(-10)) # --> 10
```

**round()**

Arredonda um número para a quantidade de casas decimais desejada.

```python
print(round(3.14159)) # --> 3
print(round(3.14159, 2)) # --> 3.14
```

**pow()**

Calcula a potência de um número.

```python
print(pow(2, 3)) # --> 8
```

**min()**

Retorna o menor valor de uma sequência ou conjunto de números.

```python
numeros = [5, 2, 8, 1, 9]

print(min(numeros)) # --> 1
```

**max()**

Retorna o maior valor de uma sequência ou conjunto de números.

```python
numeros = [5, 2, 8, 1, 9]

print(max(numeros)) # --> 9
```

## Funções para strings

Funções e métodos utilizados para manipular e modificar textos.

**upper()**

Transforma todos os caracteres de uma string em letras maiúsculas.

```python
texto = 'python'

print(texto.upper()) # --> PYTHON
```

**lower()**

Transforma todos os caracteres de uma string em letras minúsculas.

```python
texto = 'PYTHON'

print(texto.lower()) # --> python
```

**strip()**

Remove os espaços em branco do início e do final de uma string.

```python
texto = '   Olá mundo!   '

print(texto.strip()) # --> Olá mundo!
```

**replace()**

Substitui uma parte do texto por outra.

```python
texto = 'Gosto de Java'

print(texto.replace('Java', 'Python'))
# --> Gosto de Python
```

**split()**

Divide uma string em uma lista de elementos, utilizando os espaços como separadores por padrão.

```python
texto = 'maçã banana uva'

print(texto.split())
# --> ['maçã', 'banana', 'uva']
```

**find()**

Localiza a posição da primeira ocorrência de um determinado trecho dentro de uma string. Retorna -1 caso não encontre.

```python
texto = 'Gosto de Python'

print(texto.find('Python')) # --> 9
print(texto.find('Java')) # --> -1
```

## Funções para listas (vetores)

Listas são utilizadas para armazenar vários elementos em uma única variável. Seus elementos são separados por vírgulas e ficam entre colchetes `[]`.

**len()**

Retorna a quantidade de elementos de uma lista.

```python
numeros = [1, 2, 3, 4, 5]

print(len(numeros)) # --> 5
```

**append()**

Adiciona um elemento ao final da lista.

```python
numeros = [1, 2, 3]

numeros.append(4)

print(numeros) # --> [1, 2, 3, 4]
```

**insert()**

Adiciona um elemento em uma posição específica da lista.

```python
numeros = [1, 2, 4]

numeros.insert(2, 3)

print(numeros) # --> [1, 2, 3, 4]
```

**remove()**

Remove a primeira ocorrência de um determinado elemento da lista.

```python
numeros = [1, 2, 3, 2]

numeros.remove(2)

print(numeros) # --> [1, 3, 2]
```

**pop()**

Remove e retorna um elemento da lista. Caso não seja informada uma posição, remove o último elemento.

```python
numeros = [1, 2, 3, 4]

numeros.pop()

print(numeros) # --> [1, 2, 3]
```

**sort()**

Organiza os elementos da lista em ordem crescente. Também pode ser utilizado para ordem decrescente com `reverse=True`.

```python
numeros = [5, 2, 8, 1, 3]

numeros.sort()

print(numeros) # --> [1, 2, 3, 5, 8]
```

**reverse()**

Inverte a ordem dos elementos de uma lista.

```python
numeros = [1, 2, 3, 4]

numeros.reverse()

print(numeros) # --> [4, 3, 2, 1]
```

## Manipulação de arquivos

Comandos utilizados para abrir, ler, escrever e fechar arquivos.

**open()**

Abre um arquivo, permitindo realizar operações de leitura ou escrita.

- `'r'` - Modo de leitura.
- `'w'` - Modo de escrita (cria ou sobrescreve o arquivo).

```python
arquivo = open('dados.txt', 'r')
```

**read()**

Lê todo o conteúdo de um arquivo.

```python
arquivo = open('dados.txt', 'r')

conteudo = arquivo.read()

print(conteudo)

arquivo.close()
```

**readline()**

Lê uma linha do arquivo por vez.

```python
arquivo = open('dados.txt', 'r')

linha = arquivo.readline()

print(linha)

arquivo.close()
```

**write()**

Escreve um conteúdo em um arquivo.

```python
arquivo = open('dados.txt', 'w')

arquivo.write('Olá, mundo!')

arquivo.close()
```

**close()**

Fecha um arquivo que foi aberto anteriormente, liberando os recursos utilizados.

```python
arquivo = open('dados.txt', 'r')

conteudo = arquivo.read()

arquivo.close()
```

**with**

Permite trabalhar com arquivos, realizando seu fechamento automaticamente ao finalizar o bloco de código.

```python
with open('dados.txt', 'r') as arquivo:
    conteudo = arquivo.read()
    print(conteudo)
```
