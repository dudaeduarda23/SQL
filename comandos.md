## SELECT ##
É um comando utilizado para selecionar as colunas que quer consultar.
Mas toda consulta de tabelas precisa ao menos de duas instruções em sua sintaxe. A primeira é a SELECT, onde é passado uma lista de colunas que se deseja obter ou realizar a criação de novas colunas e cálculos.

![comando select](image.png)
Gera essa coluna

![coluna](image-1.png)

## FROM ##
Esta é a segunda instrução necessária para realizar uma consulta simples. Devemos informar a partir de qual tabela desejamos obter os dados

Para selecionar *** todas *** colunas de uma tabela, utilizamos *(asterisco).
<img src="image-2.png" alt="comando asterisco" style="float: left; margin-right: 10px;" width="200"/>

Este é um parágrafo que envolverá a imagem. O texto fluirá ao redor da imagem que está alinhada à esquerda. A propriedade `margin-right` adiciona um pequeno espaço entre a imagem e o texto.

Caso queremos analisar colunas específicas, escrevemos o nome da coluna e se quisermos mais de uma coluna adicionamos uma vírgula(,)
<img src="image-3.png" alt="comando select e from" style="float: left; margin-right: 10px;" width="200"/>

<img src="image-4.png" alt="tabela" style="float: left; margin-right: 10px;" width="400"/>

LIMIT - limita quantas linhas queremos.

Resumo
SELECT
FROM *** cliente ***
Podemos ler esse código da seguinte forma:
"selecione todas colunas da tabela cliente"
***