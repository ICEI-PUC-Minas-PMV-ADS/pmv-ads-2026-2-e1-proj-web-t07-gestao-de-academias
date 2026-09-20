# Especificação do Projeto

## Perfil de Usuário

<table>
<tbody>
<tr align="center">
<th colspan="2">Perfil 01: Usuário Administrativo</th>
</tr>
<tr>
<td width="150px"><b>Descrição</b></td>
<td width="600px">Proprietário, gestor ou funcionário autorizado responsável pelos cadastros e pelo acompanhamento administrativo da academia ou escola de artes marciais.</td>
</tr>
<tr>
<td><b>Necessidades</b></td>
<td>1. Cadastrar e consultar alunos.<br>2. Cadastrar e consultar modalidades.<br>3. Cadastrar e consultar instrutores.<br>4. Lançar mensalidades e registrar pagamentos.<br>5. Consultar mensalidades pagas, pendentes e vencidas.</td>
</tr>
</tbody>
</table>

## Requisitos Funcionais + Histórias de Usuários

| ID | Descrição | EU COMO... | QUERO/PRECISO... | PARA... | PÁGINA | Prioridade |
| --- | --- | --- | --- | --- | --- | --- |
| RF-01 | Permitir a criação de uma conta administrativa demonstrativa. | Gestor | criar uma conta administrativa | identificar a instituição e acessar os módulos do sistema | Cadastro | ALTA |
| RF-02 | Permitir entrar e sair da conta demonstrativa. | Usuário administrativo | iniciar e encerrar a sessão | acessar os módulos e finalizar o uso do sistema | Acesso | ALTA |
| RF-03 | Permitir cadastrar, editar e inativar alunos. | Usuário administrativo | manter os dados dos alunos atualizados | organizar os registros de matrícula | Alunos | ALTA |
| RF-04 | Permitir listar e pesquisar alunos. | Usuário administrativo | localizar alunos por nome, situação ou modalidade | consultar informações com rapidez | Alunos | ALTA |
| RF-05 | Permitir cadastrar, editar e inativar modalidades. | Usuário administrativo | manter as modalidades da instituição | organizar as atividades oferecidas | Modalidades | ALTA |
| RF-06 | Permitir listar e pesquisar modalidades. | Usuário administrativo | consultar modalidades cadastradas | localizar as atividades registradas | Modalidades | MÉDIA |
| RF-07 | Permitir cadastrar, editar e inativar instrutores. | Usuário administrativo | manter os dados dos instrutores atualizados | organizar as informações dos profissionais | Instrutores | MÉDIA |
| RF-08 | Permitir listar e pesquisar instrutores. | Usuário administrativo | localizar instrutores por nome ou especialidade | consultar dados de contato e atuação | Instrutores | MÉDIA |
| RF-09 | Permitir lançar mensalidades e registrar pagamentos integrais. | Usuário administrativo | registrar competência, valor, vencimento e pagamento | acompanhar mensalidades previstas e recebidas | Mensalidades | ALTA |
| RF-10 | Permitir consultar mensalidades pagas, pendentes ou vencidas. | Usuário administrativo | filtrar as mensalidades por situação | identificar pagamentos realizados e valores em aberto | Mensalidades | ALTA |

**Prioridade: Alta / Média / Baixa.**

## Requisitos Não Funcionais

| ID | Descrição | Prioridade |
| --- | --- | --- |
| RNF-01 | A aplicação deverá ser publicada em endereço HTTPS acessível pela Internet. | ALTA |
| RNF-02 | A interface deverá ser responsiva para computador, tablet e celular e ser verificada nos navegadores Chrome, Firefox e Edge. | ALTA |
| RNF-03 | O conteúdo principal das telas deverá buscar carregamento em até 3 segundos em condições de teste definidas durante a implementação. | ALTA |
| RNF-04 | A versão acadêmica deverá simular controle de sessão e utilizar somente dados e credenciais demonstrativos. | ALTA |
| RNF-05 | O código deverá separar telas, componentes, validações e persistência local em módulos. | MÉDIA |

**Prioridade: Alta / Média / Baixa.**
