# 🧪 Plano de Testes Mestre - Sistema SIFIT (Gestão de Academias)

---

## 📌 1. Identificação

- **Nome do Projeto**: Sistema SIFIT - Gestão Integrada de Academias, Estúdios e Boxes
- **Versão Avaliada**: 1.0 (Ambiente Web / Multi-módulo)
- **Documento de Origem**: `1-Analise_de_Requisitos.md`
- **Suíte de Testes Relacionada**: `CT_RF01.md` ao `CT_RF18.md` (18 Módulos Funcionais)
- **Tipo de Teste**: Teste Funcional Manual (BDD / Cenários de Fronteira / Fluxos Críticos)
- **Data do Documento**: 22/10/2026
- **Responsável**: Kaiki Teles de Andrade

---

## 🎯 2. Objetivo

Realizar a verificação funcional completa e sistemática da plataforma SIFIT, garantindo que os 18 requisitos funcionais identificados cumpram as regras de negócio operacionais, financeiras e de controle de acesso. O plano assegura a validação dos fluxos de cadastro, parametrizações globais, rotinas de caixa, controle biométrico/catraca, regras de inadimplência, cálculos de saúde/retenção via IA e integrações com WhatsApp e Pagar.me.

---

## 🧩 3. Escopo

### **Incluído (Escopo Funcional do SIFIT):**
- **Autenticação & Sessão**: Login, recuperação de credenciais e persistência de sessão (`RF01`).
- **Painel Operacional & Navegação**: Métricas em tempo real, cartões de alertas, temas claro/escuro e saúde da academia (`RF02`).
- **Análise Gráfica & Dashboard**: Indicadores demográficos, gráficos contratuais e balanço financeiro (`RF03`).
- **Controle de Acesso em Tempo Real**: Check-in manual/QR Code, catraca, bloqueios por inadimplência e pico de movimento (`RF04`).
- **Rastreabilidade & Frequência**: Histórico detalhado de presenças, filtros por período e atalhos rápidos (`RF05`).
- **Gestão Box & Aulas**: Geração automática da grade de aulas, categorias CrossFit e turmas (`RF06`).
- **Administração de Clientes**: Cadastro completo, biometria, dependentes e pesquisa avançada (`RF07`).
- **Contratos & Matrículas**: Emissão de planos, liquidação de parcelas e renovações/cancelamentos (`RF08`).
- **Saúde & Avaliações Físicas**: Agendamento, dobras cutâneas, antropometria e exportação de laudos (`RF09`).
- **Recebimentos Financeiros**: Baixa manual/gateway, conciliação de títulos e cobrança via WhatsApp (`RF10`).
- **Saídas Financeiras**: Lançamento de obrigações, fornecedores e despesas fixas recorrentes (`RF11`).
- **Prescrição Músculo-Esquelética**: Biblioteca de exercícios, objetivos, turmas e montagem de treinos (`RF12`).
- **Operação de Caixa & Gateway**: Abertura/fechamento diário, integração Pagar.me e geração de relatórios consolidados em PDF (`RF13`).
- **Módulo Comercial (CRM)**: Funil de prospecção de leads, tabela de planos e minutas contratuais (`RF14`).
- **Gestão Institucional**: Equipe, funções, fornecedores, loja de resgate por pontos, tarefas e pesquisas (`RF15`).
- **Histórico Clínico**: Banco de perguntas, modelos de anamnese e alertas de restrições na matrícula (`RF16`).
- **Automações & IA**: Regras de envio automático de mensagens e dashboard de prevenção de evasão (`RF17`).
- **Parametrização Global & App Mobile**: Abas operacionais de configurações, modelos de fichas e moderador mobile (`RF18`).

### **Excluído:**
- Testes de carga e estresse de infraestrutura de servidores cloud.
- Testes de penetração/segurança em nível de sistema operacional do servidor.
- Testes físicos com componentes de hardware reais não emulados (ex: validações mecânicas da catraca física fora do ambiente web).

---

## 🔧 4. Ferramentas Utilizadas

- **Navegadores Homologados**: Google Chrome, Mozilla Firefox e Microsoft Edge.
- **Ferramentas de Inspeção**: Chrome DevTools (Aba Network para inspecionar requisições da Evolution API e Pagar.me, Aba Console para erros de scripts).
- **Leitores de Documentos**: Visualizador nativo de PDF para relatórios exportados.
- **Gestão de Documentação de QA**: Ficheiros de Casos de Teste (`.md`), `3-Relatorio_de_Bugs.md` e `4-Relatorio_de_Testes.md`.

---

## 🧪 5. Técnicas de Teste Aplicadas

- **Desenvolvimento Guiado por Comportamento (BDD)**: Estruturação dos cenários em sintaxe **Dado / Quando / Então**.
- **Particionamento por Classes de Equivalência**: Validação de intervalos de datas, idades e faixas horárias.
- **Análise de Valor Limite**: Verificação dos limites de tolerância para bloqueio de inadimplentes.
- **Caminho Feliz (Happy Path)**: Conclusão completa de fluxos principais sem interrupções.
- **Testes de Exceção e Negativos**: Validação de formulários com campos em branco, credenciais inválidas e duplicidade de dados.

---

## 📄 6. Critérios de Aceitação

- 100% dos Casos de Teste Mapeados (`RF01` a `RF18`) executados.
- Nenhum bug de severidade **Crítica** ou **Alta** sem resolução ou plano de mitigação aprovado.
- Exibição consistente das telas operacionais tanto em modo claro quanto em modo escuro.
- Rastreabilidade total dos registros gravados em abas e modais com a listagem das tabelas do sistema.

---

## 🚦 7. Critérios de Saída (Exit Criteria)

- Conclusão da execução de todos os 18 módulos funcionais.
- Emissão e preenchimento completo do documento **`4-Relatorio_de_Testes.md`**.
- Mapeamento, categorização e registro formal de todas as anomalias identificadas no ficheiro **`3-Relatorio_de_Bugs.md`**.

---

## ⏱️ 8. Cronograma Estimado

| Atividade | Data Início | Data Fim |
| :--- | :--- | :--- |
| **Análise de Requisitos & Escopo (`1-Analise_de_Requisitos.md`)** | 01/10/2026 | 05/10/2026 |
| **Criação das Suítes BDD (`CT_RF01.md` ao `CT_RF18.md`)** | 06/10/2026 | 15/10/2026 |
| **Elaboração do Plano Mestre (`2-Plano_de_Testes.md`)** | 16/10/2026 | 22/10/2026 |
| **Execução dos Testes Funcionais Manuais** | 23/10/2026 | 10/11/2026 |
| **Documentação de Falhas (`3-Relatorio_de_Bugs.md`)** | 23/10/2026 | 12/11/2026 |
| **Compilação e Encerramento (`4-Relatorio_de_Testes.md`)** | 13/11/2026 | 15/11/2026 |

---

## 📋 9. Módulos e Priorização de Testes

| Código RF | Módulo do Sistema | Foco do Teste | Prioridade |
| :--- | :--- | :--- | :--- |
| **RF01** | Autenticação e Acesso | Login, senha, recuperação e sessão | **Alta** |
| **RF02** | Página Inicial | Métricas diárias, atalhos, modo claro/escuro | **Média** |
| **RF03** | Dashboard Analítico | Gráficos demográficos e consolidação gráfica | **Média** |
| **RF04** | Gestão de Check-in | Acesso em tempo real, trava por inadimplência | **Alta** |
| **RF05** | Histórico de Presenças | Filtros por período, atalhos e contadores | **Média** |
| **RF06** | Gestão SifitBox | Grade de aulas, turmas e categorias CrossFit | **Média** |
| **RF07** | Cadastro de Clientes | Gestão de alunos, biometria e dependentes | **Alta** |
| **RF08** | Matrículas e Contratos | Emissão de planos, débitos e cancelamentos | **Alta** |
| **RF09** | Avaliações Físicas | Protocolos, dobras cutâneas e laudos | **Média** |
| **RF10** | Contas a Receber | Baixa de mensalidades, faturamento e cobrança | **Alta** |
| **RF11** | Contas a Pagar | Saídas financeiras, despesas fixas e fornecedores | **Alta** |
| **RF12** | Fichas de Treino | Biblioteca de exercícios, objetivos e montagem | **Média** |
| **RF13** | Gestão Financeira Avançada | Caixas diários, Pagar.me e relatórios PDF | **Alta** |
| **RF14** | Módulo Comercial (CRM) | Funil de leads, tabelas de planos e contratos | **Média** |
| **RF15** | Pessoas e Utilidades | Equipe, loja de pontos, tarefas e enquetes | **Baixa** |
| **RF16** | Saúde e Anamnese | Fichas clínicas, perguntas e alertas | **Média** |
| **RF17** | Inteligência e Automação | Motor de disparo de mensagens e métricas IA | **Alta** |
| **RF18** | Configurações Globais | Parametrização em abas e moderação mobile | **Alta** |

---

## 🐞 10. Gestão de Defeitos e Estrutura do `3-Relatorio_de_Bugs.md`

Toda e qualquer inconsistência ou erro encontrado durante a execução do plano será devidamente padronizado e consolidado no ficheiro **`3-Relatorio_de_Bugs.md`**.

Os defeitos registrados deverão conter obrigatoriamente a seguinte estrutura:
1. **ID do Bug**: Identificador único (ex: `BUG-RF04-01`).
2. **Título do Defeito**: Resumo claro e objetivo do problema.
3. **Módulo Afetado**: Código do Requisito Funcional (ex: `RF04 - Gestão de Check-in`).
4. **Severidade**: 
   - **Crítica**: Impede totalmente o uso do sistema ou causa perda/corrupção de dados.
   - **Alta**: Falha em funcionalidade principal sem contorno simples.
   - **Média**: Comportamento incorreto em funcionalidade secundária com contorno disponível.
   - **Baixa**: Erro estético, problema de alinhamento visual ou texto incorreto.
5. **Passos para Reprodução**: Sequência exata de ações executadas para gerar o erro.
6. **Resultado Esperado**: O comportamento previsto pelas regras de negócio.
7. **Resultado Obtido**: O comportamento real e defeituoso apresentado pelo sistema.
8. **Evidência**: Captura de tela, gravação ou log da requisição.

---

## 📌 11. Riscos Identificados e Planos de Mitigação

| Risco Identificado | Impacto | Plano de Mitigação |
| :--- | :--- | :--- |
| **1. Instabilidade no Gateway Pagar.me** | **Alto** | Utilizar chaves de sandbox/homologação e validar mensagens de tratamento de erro para transações recusadas. |
| **2. Bloqueio ou atraso nos disparos de mensagens automáticas (WhatsApp / Evolution API)** | **Médio** | Validar o comportamento do sistema com os logs de envio e verificar limites de requisição da API de mensagens. |
| **3. Inconsistência nos cálculos de métricas do motor de IA e prevenção de evasão** | **Médio** | Garantir massa de dados prévia simulada na base para validar os algoritmos de frequência e risco. |

---

## 📁 12. Documentos Entregáveis do Projeto

A documentação mestre do projeto de testes do SIFIT é composta por 5 pilares interligados:

1. **`1-Analise_de_Requisitos.md`**: Mapeamento detalhado das regras operacionais do sistema.
2. **`2-Plano_de_Testes.md`**: Este documento mestre com a estratégia, cronograma e diretrizes de teste.
3. **`3-Relatorio_de_Bugs.md`**: Registro formal de todas as inconsistências identificadas na execução.
4. **`4-Relatorio_de_Testes.md`**: Sumário executivo final compilando o percentual de aprovação, contagem de cenários e parecer de homologação.
5. **Suíte de Ficheiros BDD**: Arquivos individuais `CT_RF01.md` até `CT_RF18.md` contendo todos os casos de teste padronizados.
