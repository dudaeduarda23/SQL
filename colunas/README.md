# Criação de colunas

Como criar colunas novas a partir de colunas que já existem.

Exemplo: Selecionar a tabela cliente e adicionar 10 pontos para cada usuário.

SELECT *, 
      QtdePontos + 10

FROM clientes

-- selecionando todas as colunas e adicionando uma a mais
**Antes**

![alt text](image-13.png)

**Depois**

![Depois](image-12.png)

`Isso é uma expressão QtdePontos + 10`

obs:**Essa expressõa não modifica os dados do banco principal**, a expressão só é exibida, mas não é armazenada permanentemente.

### Como renomear uma colunas (AS - apelido)

![AS-código](image-15.png)

![AS](image-14.png)

