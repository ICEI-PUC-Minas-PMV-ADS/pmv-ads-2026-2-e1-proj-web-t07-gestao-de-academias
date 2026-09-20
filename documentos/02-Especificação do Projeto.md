# Especificação do Projeto

## Perfil de usuário

O projeto possui um único perfil: usuário administrativo, representado pelo proprietário, gestor ou funcionário autorizado da instituição. Esse perfil realiza os mesmos tipos de operação na primeira versão.

| Aspecto | Definição |
| --- | --- |
| Objetivo | Manter os registros administrativos e acompanhar mensalidades. |
| Necessidades | Cadastrar, editar, inativar, pesquisar e consultar registros. |
| Contexto de uso | Atendimento e organização da rotina em computador, tablet ou celular. |
| Dificuldades consideradas | Dados dispersos, dificuldade de consulta e interfaces com excesso de opções. |
| Acesso de alunos e instrutores | Não previsto nesta versão. |

## Organização dos requisitos

Os dez identificadores funcionais da etapa 1 são preservados. O RF-09 foi detalhado para incluir o lançamento de uma mensalidade antes do pagamento, condição necessária para consultar pendências no RF-10. Os critérios de aceitação tornam o comportamento verificável e orientam os protótipos.

| Módulo | Requisitos | Operações |
| --- | --- | --- |
| Acesso | RF-01 e RF-02 | Criar conta demonstrativa, entrar e sair. |
| Alunos | RF-03 e RF-04 | Cadastrar, editar, inativar, listar e filtrar. |
| Modalidades | RF-05 e RF-06 | Cadastrar, editar, inativar, listar e pesquisar. |
| Instrutores | RF-07 e RF-08 | Cadastrar, editar, inativar, listar e pesquisar. |
| Mensalidades | RF-09 e RF-10 | Lançar mensalidade, registrar pagamento e consultar situações. |

## Requisitos funcionais e histórias de usuário

### RF-01 Criar conta administrativa

Requisito: permitir a criação de uma conta administrativa demonstrativa associada à instituição. Prioridade: alta.

História: como gestor, quero criar uma conta para identificar a instituição e acessar os módulos administrativos na demonstração.

Critérios de aceitação: exigir nome da instituição, nome do responsável, e-mail, senha demonstrativa e confirmação. Validar o formato do e-mail e a igualdade entre senha e confirmação. Rejeitar e-mail já cadastrado na base local, preservando os demais dados do formulário. Após o sucesso, apresentar confirmação e encaminhar para a entrada. Não utilizar credenciais reais na demonstração.

### RF-02 Entrar e sair

Requisito: permitir a entrada e a saída da conta demonstrativa. Prioridade: alta.

História: como usuário administrativo, quero iniciar e encerrar minha sessão para acessar os módulos e finalizar o uso do sistema.

Critérios de aceitação: validar os dados de entrada, apresentar mensagem genérica quando não corresponderem a uma conta e permitir nova tentativa. Uma entrada válida abre o início. A ação Sair encerra a sessão demonstrativa e retorna à entrada. A navegação direta para uma tela administrativa sem sessão deve retornar à entrada. Esse controle de interface não equivale a autenticação segura no servidor.

### RF-03 Manter alunos

Requisito: permitir cadastrar, editar e inativar alunos. Prioridade: alta.

História: como usuário administrativo, quero manter os dados dos alunos atualizados para organizar os registros de matrícula.

Critérios de aceitação: exigir nome e uma modalidade ativa. Telefone e e-mail são opcionais, com validação quando preenchidos. Gerar identificador único. Na edição, preservar o identificador e carregar os valores existentes. Antes de inativar, solicitar confirmação com o nome do aluno. A inativação mantém as mensalidades e o histórico consultáveis. Cancelar uma alteração não modifica o cadastro.

### RF-04 Consultar alunos

Requisito: permitir listar e pesquisar alunos por nome, situação cadastral ou modalidade. Prioridade: alta.

História: como usuário administrativo, quero localizar alunos rapidamente para consultar informações sem procurar em registros dispersos.

Critérios de aceitação: apresentar nome, modalidade, situação e ação de consulta. Combinar pesquisa textual com filtros de situação e modalidade. Ignorar diferenças de maiúsculas e minúsculas na pesquisa. Exibir quantidade de resultados e ação Limpar filtros. Diferenciar uma lista sem cadastros de uma busca sem resultados.

### RF-05 Manter modalidades

Requisito: permitir cadastrar, editar e inativar modalidades. Prioridade: alta.

História: como usuário administrativo, quero manter as modalidades da instituição para organizar as atividades que podem ser vinculadas aos alunos.

Critérios de aceitação: exigir nome e permitir descrição opcional. Impedir nomes duplicados após normalização de espaços e de maiúsculas e minúsculas. Preservar o identificador na edição. Bloquear a inativação quando houver alunos ativos vinculados, indicando a necessidade de editar esses vínculos. Sem vínculos ativos, solicitar confirmação e preservar os registros históricos.

### RF-06 Consultar modalidades

Requisito: permitir listar e pesquisar modalidades cadastradas. Prioridade: média.

História: como usuário administrativo, quero consultar as modalidades para encontrar as atividades registradas pela instituição.

Critérios de aceitação: listar nome, descrição resumida, situação e ações. Pesquisar por nome. Permitir visualizar registros ativos e inativos. Se não houver resultados, informar a situação e oferecer a limpeza da busca.

### RF-07 Manter instrutores

Requisito: permitir cadastrar, editar e inativar instrutores. Prioridade: média.

História: como usuário administrativo, quero manter os dados dos instrutores atualizados para organizar as informações dos profissionais.

Critérios de aceitação: exigir nome e especialidade. Telefone e e-mail são opcionais. Gerar identificador único e preservá-lo na edição. Confirmar a inativação com identificação do profissional e manter o registro para consulta. Não criar conta de acesso para o instrutor.

### RF-08 Consultar instrutores

Requisito: permitir listar e pesquisar instrutores por nome ou especialidade. Prioridade: média.

História: como usuário administrativo, quero localizar instrutores por nome ou especialidade para consultar seus dados de contato e atuação.

Critérios de aceitação: apresentar nome, especialidade, contato, situação e ações. A busca deve verificar nome e especialidade. Exibir estado sem resultados e ação para limpar a pesquisa.

### RF-09 Lançar mensalidade e registrar pagamento

Requisito: permitir lançar uma mensalidade de aluno e registrar seu pagamento integral. Prioridade: alta.

História: como usuário administrativo, quero registrar competência, valor, vencimento e pagamento para acompanhar as mensalidades previstas e recebidas.

Critérios de aceitação: no lançamento, exigir aluno ativo, competência mensal, valor maior que zero e data de vencimento válida. Impedir outra mensalidade para o mesmo aluno e competência. Criar o registro sem data de pagamento. Para dar baixa, selecionar uma mensalidade em aberto, mostrar seus dados e solicitar a data do pagamento integral, que não pode estar no futuro. Confirmar a operação e atualizar a situação para Paga. Cancelar não altera o registro. Não processar transações financeiras, pagamentos parciais, descontos ou estornos nesta versão.

### RF-10 Consultar mensalidades

Requisito: permitir consultar mensalidades pagas, pendentes ou vencidas. Prioridade: alta.

História: como usuário administrativo, quero filtrar as mensalidades para identificar pagamentos realizados e valores em aberto.

Critérios de aceitação: listar aluno, competência, valor, vencimento, situação e ação. Combinar busca por aluno, competência e situação. Uma mensalidade paga possui data de pagamento. Sem pagamento, será Pendente quando vencer hoje ou em data futura, e Vencida quando o vencimento for anterior à data atual. Recalcular essa classificação ao consultar os registros. Mostrar a data de pagamento no detalhe e evitar uma segunda baixa de mensalidade já paga.

## Regras de negócio

| Regra | Definição |
| --- | --- |
| RN-01 | Cada registro possui identificador estável. Alterar um nome não pode romper os vínculos. |
| RN-02 | Cada aluno possui uma modalidade nesta versão. O cadastro e a troca de modalidade utilizam apenas modalidades ativas. |
| RN-03 | Inativação preserva o registro e seus vínculos históricos. A interface não oferece exclusão definitiva. |
| RN-04 | Modalidade com alunos ativos vinculados não pode ser inativada. Primeiro é necessário alterar esses vínculos ou inativar os alunos, conforme a situação real. |
| RN-05 | Aluno inativo não recebe novos lançamentos. Mensalidades anteriores permanecem consultáveis e podem receber pagamento. |
| RN-06 | A combinação entre aluno e competência é única. A competência identifica mês e ano de referência, independentemente do vencimento. |
| RN-07 | Pagamento é integral e manual. A data de pagamento determina a situação Paga. O sistema não movimenta dinheiro. |
| RN-08 | Pendente significa sem pagamento e com vencimento igual ou posterior a hoje. Vencida significa sem pagamento e com vencimento anterior a hoje. |
| RN-09 | Valores usam reais, com duas casas decimais. Datas são exibidas em dia/mês/ano e comparadas como datas de calendário, sem horário. |
| RN-10 | Campos obrigatórios têm rótulo e indicação visível. Erros preservam o preenchimento válido e indicam a correção necessária. |

## Dados essenciais

| Entidade | Campos previstos |
| --- | --- |
| Conta demonstrativa | Identificador, instituição, responsável, e-mail e dados exclusivos de demonstração do acesso. |
| Aluno | Identificador, nome, modalidadeId, telefone opcional, e-mail opcional e situação cadastral. |
| Modalidade | Identificador, nome, descrição opcional e situação cadastral. |
| Instrutor | Identificador, nome, especialidade, telefone opcional, e-mail opcional e situação cadastral. |
| Mensalidade | Identificador, alunoId, competência, valor em centavos, vencimento e data de pagamento opcional. |

A situação financeira é derivada das datas. Não deve ser mantida como campo independente que possa divergir do pagamento e do vencimento. Os conjuntos de dados pertencem à conta demonstrativa em uso. A persistência é local e não sincroniza dispositivos (MDN WEB DOCS, s.d.).

## Requisitos não funcionais

| ID | Requisito e forma de verificação | Prioridade |
| --- | --- | --- |
| RNF-01 | Publicar a aplicação em endereço HTTPS acessível pela Internet. Manter a meta de 95% de disponibilidade mensal durante a operação acadêmica, calculada pela proporção de verificações bem-sucedidas em intervalos regulares. Não declarar essa meta cumprida antes de existir medição. | Alta |
| RNF-02 | Adaptar a interface a larguras de referência de 390, 768 e 1440 pixels e verificar as duas versões estáveis mais recentes de Chrome, Firefox e Edge disponíveis na validação. Conferir teclado, foco, rótulos, mensagens de erro e ausência de cortes de conteúdo essencial. | Alta |
| RNF-03 | Buscar carregamento do conteúdo principal em até 3 segundos. Medir com cache desativado, conexão de teste de 10 Mbps e latência de 100 ms, em cinco execuções por tela principal. Usar a mediana de LCP e uma base fictícia de 500 alunos e 3000 mensalidades. Registrar ambiente e resultados na implementação. | Alta |
| RNF-04 | Simular controle de sessão e redirecionar acessos sem sessão para a entrada. Encerrar a sessão pela ação Sair. Utilizar somente registros e credenciais demonstrativos. O front-end isolado não garante confidencialidade ou autorização contra manipulação do navegador. | Alta |
| RNF-05 | Separar telas, componentes, validações e persistência local em módulos. Verificar que acesso ao armazenamento fica concentrado em uma camada própria, sem repetição de regras nas telas. | Média |

As verificações de contraste, navegação por teclado, foco e identificação de erros serão orientadas pelas WCAG 2.2. O protótipo permite inspecionar a apresentação e os fluxos, mas não comprova a acessibilidade do código nem o desempenho ou a disponibilidade da aplicação (W3C, 2024).
