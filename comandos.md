## SELECT ##
É um comando utilizado para selecionar as colunas que quer consultar.
Mas toda consulta de tabelas precisa ao menos de duas instruções em sua sintaxe. A primeira é a SELECT, onde é passado uma lista de colunas que se deseja obter ou realizar a criação de novas colunas e cálculos.

![comando select](image.png)
Gera essa coluna
![coluna](image-1.png)

## FROM ##
Esta é a segunda instrução necessária para realizar uma consulta simples. Devemos informar a partir de qual tabela desejamos obter os dados

Para selecionar *** todas *** colunas de uma tabela, utilizamos *(asterisco).
![comando *](image-2.png)

Caso queremos analisar colunas específicas, escrevemos o nome da coluna e se quisermos mais de uma coluna adicionamos uma vírgula(,)

![comando select, from](image-3.png)
![tabela](image-4.png)

LIMIT - limita quantas linhas queremos.

Resumo
SELECT
FROM *** cliente ***
Podemos ler esse código da seguinte forma:
"selecione todas colunas da tabela cliente"
***