# Organizador de Estudos Web

## Descrição

Sistema desenvolvido para auxiliar estudantes no gerenciamento de tarefas acadêmicas, permitindo o cadastro e organização de atividades de estudo.

O projeto foi desenvolvido para a disciplina Projeto Integrador e utiliza banco de dados relacional para armazenamento das informações.

## Tecnologias Utilizadas

- HTML5
- CSS3
- JavaScript
- SQL
- MySQL
- phpMyAdmin
- Git
- GitHub
- XAMPP

## Estrutura do Banco de Dados

### Usuario

- id_usuario
- nome
- email
- senha

### Categoria

- id_categoria
- nome_categoria

### Tarefa

- id_tarefa
- titulo
- descricao
- data_limite
- status
- id_usuario
- id_categoria

## Relacionamentos

- Um usuário pode possuir várias tarefas.
- Uma categoria pode possuir várias tarefas.
- Cada tarefa pertence a um único usuário.
- Cada tarefa pertence a uma única categoria.

## Operações Implementadas

### CREATE

Criação das tabelas do banco de dados.

### INSERT

Inserção de registros.

### SELECT

Consultas de dados.

### UPDATE

Atualização de registros.

### DELETE

Remoção de registros.

## Como Executar

1. Instalar XAMPP.
2. Iniciar Apache e MySQL.
3. Acessar phpMyAdmin.
4. Criar o banco de dados organizacao_estudos.
5. Executar o script banco.sql.
6. Executar os comandos SQL para testes.

## Autores

- Rahyssa Alves Meireles
- Izaías Aguiar de Lima
