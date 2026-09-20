# Metodologia

## Organização do trabalho

O planejamento da etapa 2 utiliza um processo incremental, com acompanhamento visual de tarefas inspirado em Kanban. A equipe deverá organizar o trabalho em unidades pequenas, relacionar cada atividade a um requisito e revisar os artefatos antes de consolidar a entrega. A visualização do fluxo e o controle do trabalho em andamento seguem os princípios do The Kanban Guide (KANBAN GUIDES, 2025).

Essa organização permite identificar dependências, como a definição das regras de mensalidade antes da conclusão de suas telas, e evita que documentação e protótipo avancem com comportamentos diferentes.

## Divisão de papéis

A distribuição abaixo é uma proposta para a execução da etapa 2, sujeita ao alinhamento entre os integrantes. Ela define responsáveis de referência e revisores, sem restringir a participação dos demais membros. As contribuições efetivas deverão ficar registradas no repositório.

| Integrante | Responsabilidade principal proposta | Entrega de referência | Revisão cruzada |
| --- | --- | --- | --- |
| Arthur Morais Pianchão de Oliveira | Requisitos e regras de negócio | Especificação e critérios de aceitação | Revisar mensalidades com Pedro. |
| Guilherme Augusto Ferreira de Sousa Campos | Processo e organização do repositório | Metodologia, quadro e integração dos arquivos | Revisar contexto e referências com Matheus. |
| Kristian Arcanjo de Oliveira | Experiência do usuário e projeto de interface | User Flow, componentes e protótipo | Revisar navegação e redação com Arthur. |
| Matheus Henrique Pinheiro Abreu | Contexto e fundamentação | Problema, objetivos, justificativa e referências | Revisar metodologia com Guilherme. |
| Pedro Augusto Pereira dos Santos | Qualidade e rastreabilidade | Conferência entre RF, telas e cenários de validação | Revisar protótipo com Kristian. |

O professor tutor, Humberto Azevedo Nigri do Carmo, exerce a orientação acadêmica. A equipe deverá analisar suas devolutivas, registrar os ajustes e conferir a adequação da entrega às orientações da disciplina.

## Processo

O quadro proposto terá as colunas A fazer, Em andamento, Em revisão e Concluído. Cada tarefa deverá conter título, responsável, requisito ou seção relacionada, descrição do resultado esperado, dependências e evidência da entrega.

Como política inicial, cada integrante deverá manter no máximo uma tarefa principal em andamento. Bloqueios precisam ser registrados no próprio item, com a informação necessária para resolvê-los. Uma atividade só poderá ser considerada concluída depois da revisão e da correção dos problemas encontrados.

O ciclo de trabalho proposto compreende:

1. Revisar a etapa 1 e registrar dúvidas, inconsistências e ajustes indicados pelo professor.
2. Consolidar o perfil administrativo, os requisitos e as regras de negócio.
3. Definir os fluxos principais, alternativos e de cancelamento.
4. Produzir o protótipo de baixa fidelidade e relacionar cada tela aos requisitos.
5. Realizar uma revisão cruzada de texto, navegação, legibilidade e consistência.
6. Corrigir os apontamentos, atualizar os arquivos e registrar a versão da entrega.

A equipe deverá combinar uma reunião breve semanal e realizar atualizações assíncronas no quadro. A cadência e os horários dependem da disponibilidade dos integrantes. Decisões de escopo devem ser registradas no repositório para que a documentação reflita o acordo mais recente.

## Versionamento e revisão

O Git será utilizado para versionar os arquivos, com o GitHub como repositório compartilhado. Alterações deverão ser feitas em branches com nomes relacionados à tarefa, como `docs/metodologia` ou `design/fluxo-mensalidades`. As mensagens de commit devem descrever a alteração de forma objetiva.

Antes de integrar uma alteração à branch principal, o autor deverá abrir um pull request com o motivo, os arquivos alterados e as verificações realizadas. Outro integrante deverá conferir a coerência com os requisitos e registrar eventuais ajustes. Esse procedimento é uma política proposta para o trabalho da equipe, e não um histórico de ações já realizadas.

Os arquivos Markdown serão a fonte de consulta no repositório. O documento consolidado e as imagens de interface devem ser atualizados a partir da mesma versão, evitando divergências. O protótipo editável deverá permanecer acessível à equipe pelo link registrado na documentação.

## Ferramentas

| Ferramenta | Finalidade no projeto | Evidência esperada |
| --- | --- | --- |
| Git e GitHub | Versionar arquivos, reunir documentação e revisar alterações. | Commits, branches e pull requests. |
| GitHub Issues e Projects | Registrar tarefas, dependências e situação do trabalho. | Itens relacionados aos requisitos e quadro atualizado. |
| Canva | Editar as telas e os fluxos disponibilizados nesta entrega. | Dois designs editáveis, com links no guia do protótipo. |
| Figma | Opção para continuidade da prototipação com camadas nativas e ligações entre telas. | Arquivo a gerar com o recurso complementar e a validar no editor. |
| Microsoft Teams | Realizar alinhamentos e registrar decisões da equipe. | Anotações e encaminhamentos acordados. |
| Visual Studio Code | Editar Markdown e, nas próximas etapas, o código da aplicação. | Arquivos versionados. |
| Navegadores e ferramentas de desenvolvimento | Verificar comportamento, responsividade e desempenho durante a implementação. | Registros de testes com ambiente identificado. |

O GitHub Projects permite organizar itens em visualizações como quadro e tabela e relacioná-los ao trabalho do repositório (GITHUB, s.d.). Para esta etapa, a escolha das ferramentas prioriza rastreabilidade e edição compartilhada.

## Critérios para concluir uma tarefa

- O conteúdo atende ao requisito ou à seção vinculada.
- Textos, nomes de campos, situações e ações seguem a mesma terminologia.
- O fluxo contempla confirmação, cancelamento e os erros pertinentes.
- Os arquivos abrem corretamente e os links relativos apontam para arquivos existentes.
- O responsável registra a entrega e o revisor confere os pontos aplicáveis.
- Ajustes identificados na revisão são resolvidos antes da consolidação.

## Sequência de execução

| Ordem | Trabalho | Dependência | Resultado esperado |
| --- | --- | --- | --- |
| 1 | Revisar contexto e especificação | Etapa 1 e devolutiva do professor | Requisitos consistentes. |
| 2 | Definir metodologia e responsáveis | Alinhamento da equipe | Processo registrado. |
| 3 | Desenhar os fluxos | Regras e requisitos definidos | Caminhos e decisões identificados. |
| 4 | Elaborar o protótipo | Fluxos revisados | Telas editáveis e identificadas. |
| 5 | Revisar e corrigir | Documentação e telas disponíveis | Artefatos coerentes entre si. |
| 6 | Consolidar no repositório | Ajustes concluídos | Entrega organizada e acessível. |

Os prazos deverão ser associados ao calendário da disciplina, sem substituir as datas oficiais de entrega. Os estudos e as atividades avaliativas dos Microfundamentos permanecem como responsabilidade individual de cada integrante, acompanhada no ambiente acadêmico.
