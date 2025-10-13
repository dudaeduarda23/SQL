## SELECT ## (Pedir para ver dados)
É um comando utilizado para selecionar as colunas que quer consultar.
Mas toda consulta de tabelas precisa ao menos de duas instruções em sua sintaxe. A primeira é a SELECT, onde é passado uma lista de colunas que se deseja obter ou realizar a criação de novas colunas e cálculos.

![comando select](image.png)

Gera essa coluna

![coluna](image-1.png)

## FROM ##
Esta é a segunda instrução necessária para realizar uma consulta simples. Devemos informar a partir de qual tabela desejamos obter os dados

Para selecionar *** todas *** colunas de uma tabela, utilizamos *(asterisco).

![alt text](image-2.png)

Este é um parágrafo que envolverá a imagem. O texto fluirá ao redor da imagem que está alinhada à esquerda. A propriedade `margin-right` adiciona um pequeno espaço entre a imagem e o texto.

Caso queremos analisar colunas específicas, escrevemos o nome da coluna e se quisermos mais de uma coluna adicionamos uma vírgula(,)
<img src="image-3.png" alt="comando select e from" style="float: left; margin-right: 10px;" width="200"/>

<img src="image-4.png" alt="tabela" style="float: left; margin-right: 10px;" width="400"/>

LIMIT - limita quantas linhas queremos.
o comando LIMIT é sempre na última linha do código.

Resumo
SELECT
FROM *** cliente ***
Podemos ler esse código da seguinte forma:
"selecione todas colunas da tabela cliente"
***

## .tables
É o comando utilizado para dizer quantas tabelas tem no banco de dados que estamos usando.

obs: Esse comando varia de acordo com o banco de dados, por exemplo SHOW TABLES em MySQL.

### comentários 
![alt text](image-5.png)

obs: Não podemos comentar na última linha do código(normalmente depois do comando LIMIT), pois senão o código não roda.

## WHERE
É o comando utilizado para realizar um filtro **em linhas**.

![comando where](image-6.png)

Podemos ler esse código da seguinte forma " selecione todas colunas da tabela cliente onde os valores da coluna Flemail sejam iguais a 1

obs: utilizamos aspas simples ' ', pois é uma STRING.

![tabela do where](image-7.png)

## OR, IN, LIKE (Comandos de filtrar)
Exemplo: Selecione produtos que contêm ‘churn’ no nome.

Na tabela temos 'churn_10pp'
                'churn_5pp'
                'churn_2pp'


Podemos começar filtrando com WHERE, mas ele se limita a comparar **apenas um valor**

WHERE DescNomeProduto = 'Churn_10pp'

![WHERE](image-9.png)

obs: Se colocarmos WHERE DescNomeProduto = 'Churn_', não aparece nada.

### OR
É uma forma funcional de buscar múltiplos valores, mas se torna longa e menos legível à medida que a lista de valores aumenta.

**WHERE** DescNomeProduto = 'Churn_10pp'
**OR** DescNomeProduto = 'Churn_5pp'
**OR** DescNomeProduto = 'Churn_2pp'

![OR](image-10.png)

Le-se `Onde` DescNomeProduto seja igual a **Churn_10pp** `OU` igual a **Churn_5pp**  `OU` ...

### Comando IN (lista de valores)

O comando IN é a forma preferida e mais limpa de substituir múltiplos ORs com o mesmo campo.

Where DescNomeProduto `IN` ('churn_10pp','churn_5pp', 'churn_2pp')

Le-se Onde DescNomeProduto esteja dentro dessa lista

### LIKE (tem que ser parecido com...)

WHERE DescNomeProduto `LIKE` **'Churn%'**

**Símbolo %**

palavra **%** - indica que a frase começa com essa palavras

**%**palavra - indica que a frase termina com essa palavras

**%**palavra **%** - indica que no meio do valor tem essa palavra

`% indica onde deve ocorrer a comparação.`
***
### MAS a melhor forma de escrever essa Query seria:

obs: Isso também depende de como os dados estão organizados, mas nesse contexto é possível escrever dessa forma:

WHERE DescCategoriaProduto = **'churn_model'**

![WHERE](image-8.png)

 No final o menos custoso de processamento é o de igualdade(WHERE) mas cada uso depende de como o banco está organizado.

 ## Quando utilizar cada forma(desempenho)

 A desvantagem do LIKE é que ele é custoso, se você sabe o que quer buscar utiliza IN. No final o menos custoso de processamento é o de igualdade (WHERE)."