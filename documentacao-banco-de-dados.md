# Sumário

# Criar banco de dados

````sql
create database ecommerce;
````

# Deletar banco de dados

````sql
drop database ecommerce;
````

# Criar tabela

````sql
create table produtos (
    id serial primary key,
    nome text,
    preco float,
    descricao text

);
````

# Consulta SQL

````sql
select * from produtos; // Consulta todos os registros da tabela
````

Se quiser consultar por campos específicos:

````sql
select id, nome from produtos;
````

## Where

O comando `Where` serve para filtrar registros de acordo com uma condição.

````sql
select * from produtos where price < 100;
````
## Predicados de Comparação

Têm a mesma função dos operadores de comparação e são representados por algumas palavras reservadas.

**Between:** Compra se um valor está entre um intervalo de valores.

**Not Between:** Compara se um valor não está entre um intervalo de valores.

**Is Null:** Verifica se o valor de um campo é nulo.

**Is Not Null:** Verifica se o valor de um campo não é nulo.

**Like:** Permite comparar um valor ou uma parte dele.

**ILike:** Permite comparar um valor ou uma parte delse sem diferenciar caracteres maiúsculos e minúsculos.