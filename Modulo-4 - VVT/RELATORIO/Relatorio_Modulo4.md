### 2.3.1 Matriz de Homologação de Testes

| ID | Componente | Cenário de Teste / Procedimento | Resultado Esperado | Status |
| :--- | :--- | :--- | :--- | :--- |
| **CT-01** | Cadastro de Usuário | Inserir novo usuário preenchendo todos os dados válidos obrigatórios (INSERT). | Usuário persistido no banco com ID único gerado. | **Aprovado** |
| **CT-02** | Cadastro de Usuário | Tentar registrar um novo usuário utilizando um e-mail já existente no banco. | Sistema bloqueia a inserção e retorna erro de duplicidade. | **Aprovado** |
| **CT-03** | Login de Usuário | Autenticar usuário informando credenciais corretas cadastradas (SELECT). | Sessão iniciada com sucesso e redirecionamento para o painel. | **Aprovado** |
| **CT-04** | Criar Categoria | Cadastrar uma nova categoria de estudos (ex: "Matemática Discreta"). | Categoria salva e vinculada diretamente ao ID do usuário criador. | **Aprovado** |
| **CT-05** | Criar Tarefa | Criar uma nova atividade associando a um Usuário e Categoria existentes. | Registro salvo com sucesso (restrição FOREIGN KEY validada). | **Aprovado** |
| **CT-06** | Criar Tarefa | Tentar criar uma tarefa vinculando-a a um ID de Categoria inexistente. | Banco de dados rejeita a operação devido à restrição de integridade. | **Aprovado** |
| **CT-07** | Listagem de Estudos | Executar consulta utilizando INNER JOIN entre Usuário, Categoria e Tarefa. | Exibição correta da lista contendo unicamente os dados do usuário logado. | **Aprovado** |
| **CT-08** | Atualizar Tarefa | Alterar o status de uma tarefa pendente para "Concluída" (UPDATE). | Campo modificado no banco com sucesso e refletido na interface web. | **Aprovado** |
| **CT-09** | Alterar Cadastro | Modificar o nome ou e-mail do perfil do estudante no painel de configurações. | Dados atualizados no banco de dados sem corromper o ID relacional. | **Aprovado** |
| **CT-10** | Excluir Tarefa | Remover uma atividade específica diretamente do painel visual (DELETE). | Registro deletado no banco; as demais tarefas continuam intactas. | **Aprovado** |
| **CT-11** | Excluir Categoria | Deletar uma categoria contendo tarefas ativas associadas a ela. | Sistema impede a exclusão ou aplica exclusão em cascata (conforme regra). | **Aprovado** |
| **CT-12** | Filtro de Tarefas | Filtrar as atividades visuais escolhendo uma categoria específica. | Exibição filtrada correta via instrução condicional SELECT ... WHERE. | **Aprovado** |
| **CT-13** | Segurança de Escopo | Tentar acessar ou alterar tarefas de outro usuário manipulando parâmetros na URL. | O sistema barra a requisição e redireciona para a página de erro ou login. | **Aprovado** |
| **CT-14** | Validação de Campos | Enviar o formulário de criação de tarefa deixando campos obrigatórios vazios. | Validação de front-end e back-end impede o envio da query vazia ao banco. | **Aprovado** |
| **CT-15** | Persistência de Dados | Forçar a atualização da página (F5) logo após realizar as operações CRUD. | O estado das informações permanece totalmente consistente, vindo do MySQL. | **Aprovado** |a
