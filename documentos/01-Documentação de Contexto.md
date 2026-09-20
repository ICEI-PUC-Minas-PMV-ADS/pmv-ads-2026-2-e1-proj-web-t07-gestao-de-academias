# Documentação de Contexto

## Introdução

Academias, estúdios e escolas de artes marciais administram cadastros de alunos, modalidades, instrutores e mensalidades. Quando essas informações ficam distribuídas entre cadernos, planilhas e mensagens, a consulta depende de buscas em diferentes locais e da atualização manual de cada registro.

O projeto **Gestão de Academias** propõe uma aplicação web que reúne esses controles em um único ambiente. O usuário administrativo poderá manter cadastros, localizar informações e acompanhar mensalidades pagas, pendentes e vencidas. A primeira versão concentra as operações essenciais para estabelecimentos de pequeno e médio porte, com atenção especial às equipes administrativas reduzidas.

O desenvolvimento integra o Projeto Eixo 1 de Desenvolvimento de Aplicação Web Front-End. Nessa versão acadêmica, os fluxos de acesso serão demonstrativos e os registros serão fictícios, armazenados no navegador. O projeto de interface representa o comportamento esperado da aplicação e orienta sua implementação nas próximas etapas.

## Problema

O problema central é a dificuldade de manter informações administrativas consistentes e disponíveis para consulta quando cada tipo de registro utiliza um controle separado. Identificar a modalidade de um aluno ou conferir uma mensalidade pode exigir a comparação de arquivos e anotações, aumentando a possibilidade de duplicidade, informação desatualizada e retrabalho.

Esse cenário é especialmente relevante para estabelecimentos com equipes reduzidas. A necessidade de organização deve ser atendida por uma interface que permita concluir tarefas recorrentes com poucos passos e mensagens compreensíveis.

A questão que orienta o projeto é: **como centralizar os cadastros e o acompanhamento de mensalidades de uma academia em uma aplicação web simples, adequada à rotina do usuário administrativo?**

## Objetivos

### Objetivo geral

Desenvolver uma aplicação web para organizar os dados básicos de alunos, modalidades, instrutores e mensalidades de academias e escolas de artes marciais.

### Objetivos específicos

- Permitir o cadastro, a edição e a inativação de alunos, modalidades e instrutores, preservando os registros relacionados.
- Disponibilizar listas, pesquisas e filtros para localizar informações administrativas.
- Permitir o lançamento de mensalidades e o registro de pagamentos integrais.
- Diferenciar mensalidades pagas, pendentes e vencidas por regras consistentes de valor e data.
- Oferecer navegação e formulários compreensíveis em computadores, tablets e celulares.
- Organizar os módulos para que os vínculos entre alunos, modalidades e mensalidades permaneçam consistentes.

## Justificativa

A organização da informação influencia a capacidade de uma pequena empresa de consultar seus registros e tomar decisões operacionais. Moraes e Escrivão Filho (2006) discutem a gestão da informação considerando as características dessas empresas. Essa perspectiva sustenta a escolha de concentrar, na aplicação, os dados utilizados nas tarefas administrativas do estabelecimento.

Krafta e Freitas (2008) abordam o uso da gestão da informação na ação comercial de uma pequena empresa de tecnologia. Embora o estudo pertença a outro setor, contribui para a discussão sobre adequar o uso da informação às necessidades concretas de uma organização de menor porte.

No contexto específico de academias, Neves et al. (2024) apresentam um sistema com cadastros e controle de mensalidades. Os autores relatam a substituição de fichas manuais e a possibilidade de consultar pagamentos com maior rapidez. O trabalho oferece uma referência relacionada ao problema, sem determinar as tecnologias deste projeto.

Com base nessas referências, a proposta concentra cadastros e consultas em quatro módulos. Espera-se reduzir buscas em controles dispersos e facilitar o acompanhamento da situação dos alunos. Esses benefícios constituem objetivos de projeto e deverão ser avaliados durante a utilização da aplicação.

## Público-alvo

O público-alvo primário é composto por proprietários, gestores e funcionários autorizados de academias, estúdios e escolas de artes marciais de pequeno e médio porte. São usuários responsáveis por cadastros e consultas durante a rotina administrativa, inclusive em estabelecimentos que utilizam cadernos ou planilhas.

O projeto considera pessoas com diferentes níveis de familiaridade com sistemas de gestão. Por isso, a interface utiliza termos do domínio, ações explícitas e mensagens que explicam como corrigir um preenchimento.

Alunos e instrutores são registros administrados pela instituição. A primeira versão não oferece login próprio para esses públicos. O acesso funcional se concentra em um único perfil administrativo.

## Delimitação da primeira versão

A versão acadêmica contempla conta administrativa demonstrativa, entrada e saída, manutenção de alunos, modalidades e instrutores, lançamento de mensalidades e registro de pagamentos integrais.

Ficam fora desse escopo: prescrição de treinos, avaliações físicas, controle de frequência, catracas, agendamento de aulas, folha de pagamento, emissão de boletos, pagamento por cartão ou Pix, notificações automáticas, múltiplos níveis de permissão e integração com sistemas externos.

A disponibilidade pública da aplicação corresponde à publicação da interface. O armazenamento no navegador não oferece sincronização entre dispositivos, gestão centralizada de contas ou proteção adequada para dados reais. Uma adoção operacional exigiria uma arquitetura com autenticação e autorização no servidor, além de persistência e procedimentos de proteção apropriados.
