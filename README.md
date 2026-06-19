Organizador de Estudos Web

Descrição

Sistema desenvolvido para auxiliar estudantes no gerenciamento de tarefas acadêmicas, permitindo o cadastro e organização de atividades de estudo.

Tecnologias Utilizadas

HTML5
CSS3
JavaScript
SQL
Git
GitHub

Estrutura do Banco de Dados

Usuario

id_usuario
nome
email
senha

Categoria

id_categoria
nome_categoria

Tarefa

id_tarefa
titulo
descricao
data_limite
status
id_usuario
id_categoria

Relacionamentos

Um usuário pode possuir várias tarefas.
Uma categoria pode estar associada a várias tarefas.
Cada tarefa pertence a um usuário e a uma categoria.

Como Executar

Baixar ou clonar o repositório.
Executar o script banco.sql em um SGBD compatível.
Utilizar as consultas SQL para testar o funcionamento do banco de dados.

Autores

Rahyssa Alves Meireles
Izaías Aguiar de Lima
