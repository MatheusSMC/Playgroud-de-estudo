# 📘 SQL – Anotações de Estudo

## Criar uma Tabela

create table work (
  nome VARCHAR(50),
  email VARCHAR(100),
  funcao VARCHAR(50),
  salario DECIMAL(10,2)
);


-- Inserir dados em uma tabela

Insert into work(nome, email, funcao, salario)

Values

(Miguel, miguel123@gmail.com, secretário, 1600)

-- Usar uma Tabela

Use work;

-- Selecionar tudo que há na tabela

Select * fram work;

-- Selecionar 1 Coluna

Select name from work;

-- Selecianas 2 colunas

Select name, email from work;

-- SQL – Filtros e Condicionais
 ° WHERE

Filtra registros de uma tabela com base em uma condição.
Exemplo:

SELECT nome, idade 
FROM alunos
WHERE idade > 18;

 ° AND

Combina duas ou mais condições, retornando apenas os registros que atendem a todas elas.
Exemplo:

SELECT * 
FROM produtos
WHERE preco > 50 AND categoria = 'Eletrônicos';

 ° OR

Retorna registros que atendem a pelo menos uma das condições.
Exemplo:

SELECT * 
FROM clientes
WHERE cidade = 'São Paulo' OR cidade = 'Rio de Janeiro';

 ° NOT

Inverte o resultado de uma condição.
Exemplo:

SELECT * 
FROM funcionarios
WHERE NOT cargo = 'Estagiário';

 ° IN

Verifica se o valor está dentro de uma lista de opções.
Exemplo:

SELECT * 
FROM pedidos
WHERE status IN ('Pendente', 'Processando');

 ° LIKE

Usado para buscas por padrões em textos. (% = qualquer sequência, _ = um único caractere).
Exemplo:

SELECT * 
FROM clientes
WHERE nome LIKE 'M%'; -- nomes que começam com M

 ° BETWEEN

Seleciona valores dentro de um intervalo.
Exemplo:

SELECT * 
FROM vendas
WHERE data BETWEEN '2025-01-01' AND '2025-01-31';
