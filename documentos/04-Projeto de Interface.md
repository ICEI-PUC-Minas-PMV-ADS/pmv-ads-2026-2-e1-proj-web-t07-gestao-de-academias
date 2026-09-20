# Projeto de Interface

## Objetivo da interface

O projeto de interface traduz os dez requisitos funcionais em telas e percursos de uso. O protótipo mantém o foco no usuário administrativo e utiliza formas simples, textos e tons de cinza para destacar a organização das informações, a posição das ações e o comportamento esperado de cada operação.

As telas utilizam dados fictícios da Academia Demo. A data de referência dos cenários é 15/09/2026. Os registros exemplificam situações de uso, sem representar alunos, profissionais ou pagamentos reais.

## Organização da navegação

A entrada e a criação de conta compõem a área de acesso. Após entrar, o usuário encontra o início e um menu com Alunos, Modalidades, Instrutores e Mensalidades. A ação Sair da conta permanece disponível no menu.

No computador, a navegação é lateral e a área principal apresenta título, explicação breve, ação principal e conteúdo. As listas utilizam pesquisas e filtros próximos aos registros. Os formulários mantêm rótulos visíveis, indicação de obrigatoriedade e ações de salvar e cancelar.

No celular, o menu é recolhido, os campos se organizam verticalmente e as linhas de tabela são substituídas por cartões. As quatro telas móveis representam padrões de adaptação para a implementação. Elas não constituem uma versão móvel completa de todos os percursos.

## User Flow

Os fluxos representam ações, decisões e retornos. Cada tela possui um identificador que também aparece no inventário e nos arquivos de imagem. As decisões usam saídas identificadas e as operações de alteração mantêm a possibilidade de cancelar sem salvar.

### Acesso administrativo

O usuário abre a entrada. Se ainda não possui conta demonstrativa, informa os dados da instituição e do responsável, corrige eventuais erros e conclui o cadastro. Depois da confirmação, realiza a entrada. Credenciais inválidas mantêm o usuário na tela de acesso, com uma mensagem de correção. A saída encerra a sessão demonstrativa.

O fluxo F01 está reproduzido no protótipo.

### Cadastros e inativação

O usuário abre a lista do módulo, pesquisa um registro ou inicia um cadastro. A gravação depende da validação dos campos. A edição preserva o identificador. A inativação pede confirmação e mantém o histórico. Quando a modalidade possui alunos ativos, o sistema bloqueia a operação e permite consultar esses alunos para ajustar os vínculos.

O fluxo F02 está reproduzido no protótipo.

### Mensalidades e pagamentos

O lançamento cria uma mensalidade em aberto com aluno, competência, valor e vencimento. A aplicação rejeita duplicidades e valores inválidos. Para registrar um recebimento, o usuário seleciona uma mensalidade em aberto, confere o valor integral, informa a data do pagamento e confirma a operação. A lista apresenta o resultado e a situação atualizada.

O fluxo F03 está reproduzido no protótipo.

### Classificação financeira

A presença de data de pagamento define a situação Paga. Sem pagamento, um vencimento anterior ao dia atual define Vencida. Quando o vencimento é hoje ou está no futuro, a situação permanece Pendente. A competência é o mês de referência e não substitui a data de vencimento nessa comparação.

O fluxo F04 está reproduzido no protótipo.

## Protótipo de baixa fidelidade

O conjunto contém **34 telas**, sendo 30 de computador e quatro de celular, além de quatro fluxos. As telas contemplam as operações principais e estados de confirmação, erro, vazio e bloqueio.

O protótipo representa estados fixos de referência. Os campos ilustram preenchimentos, e as pesquisas e validações descrevem o comportamento que será implementado. A navegação usa percursos demonstrativos de Ana Souza, Jiu-jitsu, Boxe e Felipe Costa. Os demais registros contextualizam as listas. Retornar ao início de um cenário restabelece seu estado de referência.

### Acesso ao protótipo editável

- Computador e fluxos: https://www.canva.com/d/EL_k1MvUVqiQI8A
- Telas móveis: https://www.canva.com/d/26iAAAs_WsaJcij3

## Padrões visuais e de interação

| Elemento | Padrão definido |
| --- | --- |
| Estrutura | Menu lateral no computador e menu recolhido no celular. |
| Hierarquia | Título da tela, explicação breve, ação principal, filtros e conteúdo. |
| Cores | Escala de cinza, com botões principais escuros e texto claro. |
| Formulários | Rótulos permanentes, campos obrigatórios com asterisco e mensagens junto ao campo. |
| Situações | Rótulos textuais para Ativo, Inativo, Paga, Pendente e Vencida. |
| Alterações | Botões específicos de salvar, cancelar ou confirmar inativação. |
| Busca vazia | Mensagem de ausência de resultados e ação para limpar filtros. |
| Primeiro acesso | Orientação para cadastrar uma modalidade antes dos alunos. |
| Responsividade | Referência de 1440 × 960 pixels para as pranchas de computador e 390 × 844 pixels para as telas móveis. |
| Acessibilidade | Rótulos legíveis e situações identificadas por texto. Foco, teclado e semântica deverão ser verificados no código. |

## Rastreabilidade dos requisitos

| Requisito | Telas de referência | Fluxos |
| --- | --- | --- |
| RF-01 | T02 e T34 | F01 |
| RF-02 | T01, T03 e T24, além da ação de saída | F01 |
| RF-03 | T05, T06, T07, T08 e T25 | F02 |
| RF-04 | T04, T06, T22, T29, T30 e T33 | F02 |
| RF-05 | T10, T11, T12, T13 e T26 | F02 |
| RF-06 | T09 e T26 | F02 |
| RF-07 | T15, T16, T17 e T27 | F02 |
| RF-08 | T14 e T27 | F02 |
| RF-09 | T19, T20, T21 e T23 | F03 |
| RF-10 | T06, T18, T21 e T31 | F03 e F04 |
| RNF-02 | T29, T30, T31 e T32 como amostra visual | Verificação funcional na implementação. |

## Percursos para revisão

| Cenário | Sequência | Resultado esperado |
| --- | --- | --- |
| Criar conta | T01, T02, T34, T03 | Confirmação da criação e entrada demonstrativa. |
| Editar aluno | T04, T06, T07, T06 | Dados existentes no formulário e retorno ao cadastro. |
| Inativar aluno | T06, T08, T25 | Aluno Inativo e histórico preservado. |
| Bloquear inativação | T09, T11, T12, T33 | Consulta de alunos ativos vinculados a Jiu-jitsu. |
| Inativar modalidade livre | T09, T13, T26 | Boxe Inativa, preservando registros. |
| Inativar instrutor | T14, T16, T17, T27 | Felipe Costa Inativo. |
| Registrar pagamento | T18, T20, T21 | Ana Souza Paga em 15/09/2026 e totais atualizados. |
| Busca sem resultado | T22, T04 | Limpeza dos filtros e exibição da lista. |
| Corrigir lançamento | T23, T19 | Indicação de duplicidade e valor inválido. |
| Primeiro acesso | T28, T10 | Cadastro da primeira modalidade. |
| Navegação móvel | T29, T30, T31, T32 | Padrões móveis de consulta e menu. |

## Inventário das telas

| ID | Tela | Referência |
| --- | --- | --- |
| T01 | Entrada administrativa | RF-02 |
| T02 | Criar conta administrativa | RF-01 |
| T03 | Início administrativo | RF-02 a RF-10 |
| T04 | Lista de alunos | RF-03 e RF-04 |
| T05 | Novo aluno | RF-03 |
| T06 | Cadastro do aluno | RF-03, RF-04 e RF-10 |
| T07 | Editar aluno | RF-03 |
| T08 | Inativar aluno | RF-03 |
| T09 | Lista de modalidades | RF-05 e RF-06 |
| T10 | Nova modalidade | RF-05 |
| T11 | Editar modalidade | RF-05 |
| T12 | Inativar modalidade | RF-05 |
| T13 | Inativar modalidade | RF-05 |
| T14 | Lista de instrutores | RF-07 e RF-08 |
| T15 | Novo instrutor | RF-07 |
| T16 | Editar instrutor | RF-07 |
| T17 | Inativar instrutor | RF-07 |
| T18 | Lista de mensalidades | RF-09 e RF-10 |
| T19 | Nova mensalidade | RF-09 |
| T20 | Registrar pagamento integral | RF-09 |
| T21 | Mensalidade paga e confirmação | RF-09 e RF-10 |
| T22 | Busca de alunos sem resultados | RF-03 e RF-04 |
| T23 | Nova mensalidade com erros | RF-09 |
| T24 | Entrada com erro | RF-02 |
| T25 | Alunos após inativação | RF-03 e RF-04 |
| T26 | Modalidades após inativação | RF-05 e RF-06 |
| T27 | Instrutores após inativação | RF-07 e RF-08 |
| T28 | Primeiro acesso sem cadastros | RF-03 a RF-10 |
| T29 | Alunos | RF-04 e RNF-02 |
| T30 | Cadastro do aluno | RF-03 e RNF-02 |
| T31 | Mensalidades | RF-10 e RNF-02 |
| T32 | Menu mobile | RNF-02 |
| T33 | Alunos ativos vinculados a Jiu-jitsu | RF-04 e RF-05 |
| T34 | Conta criada com sucesso | RF-01 e RF-02 |
