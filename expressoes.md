# Expressões 
São combinações de um ou mais **valores,operadores e funções** que retornam um valor.

## Tipos de Expressões
As expressões em SQL são categorizadas pelo tipo de dado que retornam:

1.**Expressões Numéricas:** Retornam um valor numérico.

Exemplo: `Salario * 12`, `SUM(Vendas).`

**Expressões de Data e Hora:** Retornam um valor de data/hora.

Exemplo: `Data_Atual + 7`, `DATEDIFF(day, Data_Inicial, Data_Final).`

**Expressões de Caracteres (String):** Retornam um valor de texto.

Exemplo: `Nome || ' ' || Sobrenome (concatenação)`

**Expressões Booleanas (Condicionais):** Retornam um valor lógico (TRUE, FALSE ou UNKNOWN no caso de NULL).

Exemplo: `Idade >= 18, Status = 'Ativo'.`

**Expressões Especiais:** Como a expressão CASE, que permite lógica condicional (como um "if/then/else") e retorna um valor baseado nessa lógica.

Exemplo: `CASE WHEN Preco > 100 THEN 'Caro' ELSE 'Barato' END.`

