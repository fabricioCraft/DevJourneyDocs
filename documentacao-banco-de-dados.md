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