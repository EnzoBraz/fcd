---
layout: page
title: Funções
nav_order: 9
---
[<img src="https://raw.githubusercontent.com/flaviovdf/fcd/master/assets/colab_favicon_small.png" style="float: right;">](https://colab.research.google.com/github/flaviovdf/fcd/blob/master/_lessons/09-Funcoes.ipynb)

# Tópico 9 – Funções e Apply
{: .no_toc .mb-2 }

Vamos aprender sobre funções Python e como aplicar as mesmas em `DataFrame`.
{: .fs-6 .fw-300 }

{: .no_toc .text-delta }
Resultados Esperados

1. Entender como definir funções `def`
1. Entender como aplicar funções em `DataFrame`s (`apply`)

{: .no_toc .text-delta }
Material Adaptado do [DSC10 (UCSD)](https://dsc10.com/)


```python
#In: 
import babypandas as bpd
import matplotlib.pyplot as plt
import numpy as np
plt.style.use('ggplot')
```

### Agenda

- Funções.
- Aplicando funções a DataFrames.
- Exemplo: Nomes de alunos.

## Funções

### Definindo funções
* Aprendemos bastante como fazer em Python:
* Manipular arrays, séries e DataFrames.
* Execute operações em strings.
* Crie visualizações.
* Mas até agora, estamos restritos ao uso de funções existentes (por exemplo, `max`, `np.sqrt`, `len`) e métodos (por exemplo, `.groupby`, `.assign`, `.plot`).

### Motivação

Suponha que você dirija até um restaurante 🥘 em Ouro Preto, localizado a exatamente 100 quilômetros de distância.

- Nos primeiros 80 quilômetros, você dirige a 80 quilômetros por hora.
- Nos últimos 20 quilômetros, você dirige a 60 quilômetros por hora.

- **Pergunta:** Qual é a sua **velocidade média** durante a viagem?

- 🚨 A resposta não é 70 quilômetros por hora! Você precisa usar o fato de que $\text{velocidade} = \frac{\text{distancia}}{\text{tempo}}$.

$$\text{velocidade média} = \frac{\text{distância}}{\text{tempo}} = \frac{80 + 20}{\text{tempo}_1 + \text{tempo}_2} \text { km por hora}$$

No segmento 1, quando você dirigiu 80 quilômetros a 80 quilômetros por hora, você dirigiu por $\frac{80}{80}$ horas:

$$\text{velocidade}_1 = \frac{\text{distância}_1}{\text{tempo}_1}$$

$$80 \text{ km por hora} = \frac{80 \text{ km}}{\text{time}_1} \implies \text{time}_1 = \frac{80}{80} \text{ horas} = 1$$

Da mesma forma, no segmento 2, quando você dirigiu 20 quilômetros a 60 quilômetros por hora, você dirigiu por $\text{time}_2 = \frac{20}{60} \text{ horas} = \frac{1}{3} horas$.

Então,

$$\text{velocidade média} = \frac{80 + 20}{\frac{1}{1} + \frac{1}{3}} \text{ km por hora} $$

$$\begin{align*}\text{velocidade média} &= 100 \cdot \frac{1}{\frac{1}{1} + \frac{1}{3}} \text{ km por hora} \\ &= 100 \frac{1}{\frac{3 + 1}{3}} \\ &= 100 \frac{3}{4} \\ &= 75 \text{ km por hora}\end{align*} $$

### Exemplo: média harmônica

A **média harmônica** ($\text{HM}$) de dois números positivos, $a$ e $b$, é definida como

$$\text{HM} = \frac{2}{\frac{1}{a} + \frac{1}{b}}$$

Geralmente é usado para encontrar a média de múltiplas **taxas**.

Encontrar a média harmônica de 80 e 60 não é difícil:


```python
#In: 
2 / (1 / 1 + 1 / 3)
```




    1.5



Mas e se quisermos determinar a média harmónica de 80 e 70? 80 e 90? 20 e 40? **Isso exigiria muito copiar e colar, o que é propenso a erros.**

Acontece que podemos **definir** nossa própria função de "média harmônica" **apenas uma vez e reutilizá-la várias vezes.


```python
#In: 
def harmonic_mean(a, b):
    return 2 / (1 / a + 1 / b)
```


```python
#In: 
harmonic_mean(1, 3)
```




    1.5




```python
#In: 
harmonic_mean(1, 5)
```




    1.6666666666666667



Observe que só tivemos que especificar como calcular a média harmônica uma vez!

### Funções

Funções são uma forma de dividir nosso código em pequenas subpartes para evitar que escrevamos código repetitivo. Cada vez que **definirmos** nossa própria função em Python, usaremos o seguinte padrão.


```python
#In: 
from IPython.display import display, IFrame
def show_def():
    src = "https://docs.google.com/presentation/d/e/2PACX-1vRKMMwGtrQOeLefj31fCtmbNOaJuKY32eBz1VwHi_5ui0AGYV3MoCjPUtQ_4SB1f9x4Iu6gbH0vFvmB/embed?start=false&loop=false&delayms=60000"
    width = 960 
    height = 569
    display(IFrame(src, width, height))
show_def()
```



<iframe
    width="960"
    height="569"
    src="https://docs.google.com/presentation/d/e/2PACX-1vRKMMwGtrQOeLefj31fCtmbNOaJuKY32eBz1VwHi_5ui0AGYV3MoCjPUtQ_4SB1f9x4Iu6gbH0vFvmB/embed?start=false&loop=false&delayms=60000"
    frameborder="0"
    allowfullscreen

></iframe>



### Funções são "receitas"

- As funções recebem entradas, conhecidas como **argumentos**, fazem algo e produzem algumas saídas.
- A beleza das funções é que **você não precisa saber como elas são implementadas para usá-las!**
- Esta é a premissa da ideia de **abstração** na ciência da computação – você ouvirá muito sobre isso no DSC 20.


```python
#In: 
harmonic_mean(1, 1)
```




    1.0




```python
#In: 
harmonic_mean(1, 3)
```




    1.5




```python
#In: 
harmonic_mean(1, 2)
```




    1.3333333333333333



### Parâmetros e argumentos

`triple` tem um **parâmetro**, `x`.


```python
#In: 
def triple(x):
    return x * 3
```

Quando chamamos `triple` com o **argumento** 5, você pode fingir que há uma primeira linha invisível no corpo de `triple` que diz `x = 5`.


```python
#In: 
triple(5)
```




    15



Observe que os argumentos podem ser de qualquer tipo!


```python
#In: 
triple('triton')
```




    'tritontritontriton'



### Funções podem receber 0 ou mais argumentos

As funções podem ter qualquer número de argumentos. Até agora, criamos uma função que leva dois argumentos – `harmonic_mean` – e uma função que leva um argumento – `triple`.

`saudação` não aceita argumentos!


```python
#In: 
def greeting():
    return 'Hi! 👋'
```


```python
#In: 
greeting()
```




    'Hi! 👋'



### As funções não são executadas até que você as chame!

O corpo de uma função não é executado até que você use (**call**) a função.

Aqui, podemos definir `where_is_the_error` sem ver uma mensagem de erro.


```python
#In: 
def where_is_the_error(something):
    '''You can describe your function within triple quotes. For example, this function 
    illustrates that errors don't occur until functions are executed (called).'''
    return (1 / 0) + something
```

Somente quando **chamamos** `where_is_the_error` que o Python nos dá uma mensagem de erro.


```python
#In: 
where_is_the_error(5)
```


    ---------------------------------------------------------------------------

    ZeroDivisionError                         Traceback (most recent call last)

    Cell In[16], line 1
    ----> 1 where_is_the_error(5)


    Cell In[15], line 4, in where_is_the_error(something)
          1 def where_is_the_error(something):
          2     '''You can describe your function within triple quotes. For example, this function 
          3     illustrates that errors don't occur until functions are executed (called).'''
    ----> 4     return (1 / 0) + something


    ZeroDivisionError: division by zero


### Exemplo: `primeiro_nome`

Vamos criar uma função chamada `first_name` que recebe o nome completo de alguém e retorna seu primeiro nome. Um exemplo de comportamento é mostrado abaixo.
```py
>>> first_name('Flavio Figueiredo')
'Flavio'
```
*Dica*: Use o método string `.split`.

Estratégia geral para escrever funções:
1. Primeiro, tente fazer com que o comportamento funcione em um único exemplo.
2. Em seguida, encapsule esse comportamento dentro de uma função.


```python
#In: 
'Flavio Figueiredo'.split(' ')[0]
```




    'Flavio'




```python
#In: 
def first_name(full_name):
    '''Returns the first name given a full name.'''
    return full_name.split(' ')[0]
```


```python
#In: 
first_name('Flavio Figueiredo')
```




    'Flavio'




```python
#In: 
# What if there are three names?
first_name('Mestre Flavio Figueiredo')
```




    'Mestre'



### Retornando

- A palavra-chave `return` especifica qual deve ser a saída da sua função, ou seja, como será avaliada uma chamada para a sua função.
- A maioria das funções que escrevemos usará `return`, mas usar `return` não é obrigatório.
- Tenha cuidado: `print` e `return` funcionam de forma diferente!


```python
#In: 
def pythagorean(a, b):
    '''Computes the hypotenuse length of a triangle with legs a and b.'''
    c = (a ** 2 + b ** 2) ** 0.5
    print(c)
```


```python
#In: 
x = pythagorean(3, 4)
```

    5.0



```python
#In: 
# No output – why?
x
```


```python
#In: 
# Errors – why?
x + 10
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[24], line 2
          1 # Errors – why?
    ----> 2 x + 10


    TypeError: unsupported operand type(s) for +: 'NoneType' and 'int'



```python
#In: 
def better_pythagorean(a, b):
    '''Computes the hypotenuse length of a triangle with legs a and b, and actually returns the result.'''
    c = (a ** 2 + b ** 2) ** 0.5
    return c
```


```python
#In: 
x = better_pythagorean(3, 4)
x
```




    5.0




```python
#In: 
x + 10
```




    15.0



### Retornando
Depois que uma função executa uma instrução `return`, ela para de funcionar.


```python
#In: 
def motivational(quote):
    return 0
    print("Uma frase motivacional:", quote)
```


```python
#In: 
motivational('Caia sete vezes e se levante oito.')
```




    0



### Escopo 🩺

Os nomes que você escolhe para os parâmetros de uma função são conhecidos apenas por essa função (conhecido como **escopo local**). O restante do seu notebook não é afetado pelos nomes dos parâmetros.


```python
#In: 
def what_is_awesome(s):
    return s + ' is awesome!'
```


```python
#In: 
what_is_awesome('data science')
```




    'data science is awesome!'




```python
#In: 
# descomente para ver o erro
# s
```


```python
#In: 
s = 'FCD'
```


```python
#In: 
what_is_awesome('data science')
```




    'data science is awesome!'



## Aplicando funções a DataFrames

### Dados dos alunos de FCD

A `df` do DataFrame contém os nomes de todos os alunos matrículados em FCD.


```python
#In: 
nomes = 'ANNY \
ARTHUR \
ARTHUR \
CAIO \
CAROLINA \
CLARA \
DANIELLE \
EDUARDO \
EDUARDO \
EMANUEL \
ENZO \
FELIPE \
FELIPE \
FRANCISCO \
GABRIEL \
GABRIEL \
GABRIELLY \
GAEL \
GUILHERME \
GUILHERME \
GUSTAVO \
ISAAC \
JOAO \
JOAO \
KARINA \
LETICIA \
LETICIA \
LIVIA \
LORRANY \
LUCAS \
LUIS \
MARCO \
MATEUS \
MATEUS \
MATHEUS \
RAIZA \
RENATO \
SOPHIA \
THAYRELAN \
VICTOR'
```


```python
#In: 
df = bpd.DataFrame().assign(
    nome=nomes.split()
)
df = df.sample(df.shape[0])
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>nome</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>18</th>
      <td>GUILHERME</td>
    </tr>
    <tr>
      <th>23</th>
      <td>JOAO</td>
    </tr>
    <tr>
      <th>37</th>
      <td>SOPHIA</td>
    </tr>
    <tr>
      <th>7</th>
      <td>EDUARDO</td>
    </tr>
    <tr>
      <th>2</th>
      <td>ARTHUR</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
    </tr>
    <tr>
      <th>13</th>
      <td>FRANCISCO</td>
    </tr>
    <tr>
      <th>4</th>
      <td>CAROLINA</td>
    </tr>
    <tr>
      <th>28</th>
      <td>LORRANY</td>
    </tr>
    <tr>
      <th>27</th>
      <td>LIVIA</td>
    </tr>
    <tr>
      <th>30</th>
      <td>LUIS</td>
    </tr>
  </tbody>
</table>
<p>40 rows × 1 columns</p>
</div>



### Exemplo: qual a primeira letra mais comum entre os nomes dos discentes de FCD?

- **Problema**: Não podemos responder agora, pois não temos uma coluna com primeira letra. Se o fizéssemos, poderíamos agrupar por ele.



- **Solução**: Criar uma função.

### Criando uma função `primeira_letra`

De alguma forma, precisamos chamar `'primeira_letra'` no `'nome'` de cada aluno.


```python
#In: 
def primeira_letra(nome):
    return nome[0]
```


```python
#In: 
primeira_letra('FLAVIO')
```




    'F'




```python
#In: 
primeira_letra(df.get('nome').iloc[0])
```




    'G'




```python
#In: 
primeira_letra(df.get('nome').iloc[1])
```




    'J'



Idealmente, existe uma solução melhor do que fazer isso centenas de vezes...

### `.apply`

- Para **aplicar** uma função a cada elemento da coluna `column_name` no DataFrame `df`, use

<br>

<center><code>df.get(column_name).apply(function_name)</code></center>

- O método `.apply` é um método de uma **Series** **não** de um DataFrame.
- **Importante:** Usamos `.apply` em séries, **não** em DataFrames.
- A saída de `.apply` também é uma série.

- Passe _apenas o nome_ da função – não a chame!
- Bom ✅: `.apply(primeira_letra)`.
- Ruim ❌: `.apply(primeira_letra())`.


```python
#In: 
df.get('nome').apply(primeira_letra)
```




    18    G
    23    J
    37    S
    7     E
    2     A
         ..
    13    F
    4     C
    28    L
    27    L
    30    L
    Name: nome, Length: 40, dtype: object



### Exemplo: nomes próprios comuns


```python
#In: 
df = df.assign(
    primeira=df.get('nome').apply(primeira_letra)
)
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>nome</th>
      <th>primeira</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>18</th>
      <td>GUILHERME</td>
      <td>G</td>
    </tr>
    <tr>
      <th>23</th>
      <td>JOAO</td>
      <td>J</td>
    </tr>
    <tr>
      <th>37</th>
      <td>SOPHIA</td>
      <td>S</td>
    </tr>
    <tr>
      <th>7</th>
      <td>EDUARDO</td>
      <td>E</td>
    </tr>
    <tr>
      <th>2</th>
      <td>ARTHUR</td>
      <td>A</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>13</th>
      <td>FRANCISCO</td>
      <td>F</td>
    </tr>
    <tr>
      <th>4</th>
      <td>CAROLINA</td>
      <td>C</td>
    </tr>
    <tr>
      <th>28</th>
      <td>LORRANY</td>
      <td>L</td>
    </tr>
    <tr>
      <th>27</th>
      <td>LIVIA</td>
      <td>L</td>
    </tr>
    <tr>
      <th>30</th>
      <td>LUIS</td>
      <td>L</td>
    </tr>
  </tbody>
</table>
<p>40 rows × 2 columns</p>
</div>




```python
#In: 
letra_count = (df.
               groupby('primeira').
               size().
               sort_values(ascending=False)
)
letra_count
```




    primeira
    G    7
    L    6
    E    4
    M    4
    A    3
        ..
    I    1
    K    1
    S    1
    T    1
    V    1
    Length: 15, dtype: int64



### Atividade

Abaixo:
- Crie um **gráfico de barras** para a `primeira` e `ultima` letra de cada nome.
- O que você consegue tirar dos dois gráficos?


```python
#In: 
...
```




    Ellipsis




```python
#In: 
...
```




    Ellipsis



### Nota: `.apply` também funciona com funções já existentes!

Por exemplo, para encontrar o comprimento de cada nome, podemos usar a função `len`:


```python
#In: 
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>nome</th>
      <th>primeira</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>18</th>
      <td>GUILHERME</td>
      <td>G</td>
    </tr>
    <tr>
      <th>23</th>
      <td>JOAO</td>
      <td>J</td>
    </tr>
    <tr>
      <th>37</th>
      <td>SOPHIA</td>
      <td>S</td>
    </tr>
    <tr>
      <th>7</th>
      <td>EDUARDO</td>
      <td>E</td>
    </tr>
    <tr>
      <th>2</th>
      <td>ARTHUR</td>
      <td>A</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>13</th>
      <td>FRANCISCO</td>
      <td>F</td>
    </tr>
    <tr>
      <th>4</th>
      <td>CAROLINA</td>
      <td>C</td>
    </tr>
    <tr>
      <th>28</th>
      <td>LORRANY</td>
      <td>L</td>
    </tr>
    <tr>
      <th>27</th>
      <td>LIVIA</td>
      <td>L</td>
    </tr>
    <tr>
      <th>30</th>
      <td>LUIS</td>
      <td>L</td>
    </tr>
  </tbody>
</table>
<p>40 rows × 2 columns</p>
</div>




```python
#In: 
df.get('nome').apply(len)
```




    18    9
    23    4
    37    6
    7     7
    2     6
         ..
    13    9
    4     8
    28    7
    27    5
    30    4
    Name: nome, Length: 40, dtype: int64



### Atividade

Encontre o nome mais curto da turma que seja compartilhado por pelo menos dois alunos na mesma seção.

*Dica*: Você terá que usar `.assign` e `.apply`.


```python
#In: 
...
```




    Ellipsis



## Resumo, da próxima vez

### Resumo

- Funções são uma forma de dividir nosso código em pequenas subpartes para evitar que escrevamos código repetitivo.
- O método `.apply` nos permite chamar uma função em cada elemento de uma Série, o que geralmente vem de `.get`ting uma coluna de um DataFrame.

### Próxima vez

Manipulações mais avançadas de DataFrame!
