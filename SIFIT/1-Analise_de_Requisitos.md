# 📦 Documentação Funcional e Requisitos - Sistema SIFIT (Gestão de Academias)

---

## 📌 Visão Geral
O **SIFIT** é uma plataforma integrada de gestão para academias, estúdios e boxes de CrossFit. O sistema abrange desde a operação de recepção, controle de acesso e agendamentos, até a gestão financeira, prescrição de treinos, retenção por inteligência artificial e comunicação móvel com os alunos.

---

## 🔐 Requisitos Funcionais Detalhados

### 🔐 **RF01 - Autenticação e Acesso ao Sistema**
**Descrição**: Tela inicial de login para autenticação e acesso dos usuários autorizados à plataforma SIFIT.
- **Funcionalidades esperadas**:
  * Formato de formulário centralizado com campos para inserção de **Login** e **Senha**.
  * Caixa de seleção (*checkbox*) **"Manter conectado"** para persistência da sessão no navegador.
  * Link de atalho **"Esqueci minha senha"** para fluxo de recuperação de credenciais.
  * Botão de ação **"Entrar"** para validação das credenciais e redirecionamento à página inicial.

---

### 🏠 **RF02 - Página Inicial e Visão Geral da Operação**
**Descrição**: Painel principal que consolida alertas em tempo real e atalhos operacionais para a rotina diária da academia.
- **Funcionalidades esperadas**:
  * Exibição de cards explicativos com métricas de alunos em risco de evasão, valores em aberto, pico de movimento e avaliações pendentes.
  * Painel de ações recomendadas do dia (cobrança de inadimplentes, contato com inativos e agendamento de avaliações).
  * Widgets com contagem de clientes ativos, ausentes, sem matrícula, matrículas no período e desistências.
  * Visualização gráfica do movimento da academia por horário e dia da semana.
  * Módulo de saúde da academia com índice percentual de retenção.
  * Lista das últimas entradas na academia via catraca/biometria e aniversariantes do dia.
  * Agenda do dia para turmas e horários.
  * Alternância dinâmica entre tema claro (*Light Mode*) e tema escuro (*Dark Mode*).

---

### 📊 **RF03 - Dashboard Analítico**
**Descrição**: Central de visualização gráfica de indicadores operacionais e financeiros da academia.
- **Funcionalidades esperadas**:
  * Gráficos demográficos de clientes por Frequência, Idade e Sexo.
  * Indicadores de Matrículas mensais e distribuição por Plano.
  * Análise financeira de Contas a Receber por Método de Pagamento e faturamento por Mês.

---

### 📲 **RF04 - Gestão de Check-in e Controle de Entrada**
**Descrição**: Monitoramento e execução do acesso dos alunos ao estabelecimento em tempo real.
- **Funcionalidades esperadas**:
  * Exibição de estatísticas diárias: Check-ins hoje, Presentes agora, Meta do dia, Média diária (30 dias) e Taxa de frequência.
  * Abas de navegação por status: Todos, Presentes agora, Não compareceram e Check-in pendente.
  * Módulo de "Entrada Rápida" para digitar o código do cliente ou realizar leitura de QR Code.
  * Modal/Botão para realização de Check-in Manual.
  * Bloqueio automático do acesso via catraca em caso de parcelas vencidas (após o prazo de tolerância de 2 dias).
  * Gráfico de pico de movimento por faixa horária.

---

### 📅 **RF05 - Histórico de Presenças**
**Descrição**: Registro detalhado e filtragem das passagens dos alunos pela academia.
- **Funcionalidades esperadas**:
  * Filtro por nome do cliente e intervalo de datas (Hoje, Esta semana, Este mês).
  * Indicadores do período: Total de presenças, Alunos distintos, Média por dia e Dias no período.
  * Listagem cronológica dos registros de acesso.

---

### 🧘 **RF06 - Gestão SifitBox (Aulas e Crossfit)**
**Descrição**: Agendamento e gerenciamento de aulas coletivas e modalidade Box/Crossfit.
- **Funcionalidades esperadas**:
  * Filtro e busca de aulas por período de datas.
  * Botão para geração automática de aulas conforme a grade semanal.
  * Cadastro de Categorias Crossfit (Barbell, Endurance, Gymnastic, BodyBuilder, Cardio).
  * Gerenciamento de Modalidades e Turmas Recorrentes com limitação de vagas e dias da semana.

---

### 👥 **RF07 - Cadastro e Gestão de Clientes**
**Descrição**: Módulo central de manutenção do cadastro de alunos e clientes da academia.
- **Funcionalidades esperadas**:
  * Filtros de busca por Código, Nome, Status (Ativo/Inativo), Situação (Adimplente/Inadimplente), Plano e Personal Trainer.
  * Métrica geral de Clientes Cadastrados, Clientes Ativos, Sem Matrícula e Ausentes.
  * Cadastro de novos clientes com inclusão de dados pessoais e biometria.
  * Vínculo de dependentes à matrícula principal.

---

### 📝 **RF08 - Gestão de Matrículas e Contratos**
**Descrição**: Controle dos contratos vigentes, renovações e cancelamentos dos alunos.
- **Funcionalidades esperadas**:
  * Indicadores de Matrículas Ativas, Recorrentes, Não Renovadas e Cadastradas no Mês.
  * Busca por código e nome do aluno.
  * Ações de visualização, cancelamento, renovação e exclusão de matrículas.
  * Cálculo automático de parcelas e datas de vencimento com base no plano escolhido.

---

### 🩺 **RF09 - Avaliações Físicas**
**Descrição**: Acompanhamento da evolução física e composição corporal dos alunos.
- **Funcionalidades esperadas**:
  * Agendamento e cadastro de novas avaliações físicas vinculadas a um Personal Evaluator.
  * Filtros por código, nome do aluno e status (Realizado / Pendente).
  * Registro de dobras cutâneas e medidas corporais.
  * Cálculo automático do percentual de gordura corporal e composição física do indivíduo.
  * Impressão e geração de relatórios de avaliação física em PDF.

---

### 💰 **RF10 - Contas a Receber**
**Descrição**: Gestão dos recebíveis, faturamento e controle de inadimplência.
- **Funcionalidades esperadas**:
  * Filtros por Tipo de Data (Vencimento/Pagamento), intervalo de datas, nome do cliente e status.
  * Métricas de Entradas, Saídas, Líquido, Previsto para o Mês, Recebido no Mês, Pendentes e Contas Atrasadas.
  * Registro de pagamentos via Gateway ou métodos manuais (Cartão de Débito, Crédito, Coras, Pix).
  * Ação de cobrança direta via integração com WhatsApp.

---

### 💳 **RF11 - Contas a Pagar e Despesas Fixas**
**Descrição**: Controle do fluxo de saídas financeiras, despesas operacionais e fornecedores.
- **Funcionalidades esperadas**:
  * Lançamento de novas contas a pagar com data de vencimento, valor e fornecedor/colaborador.
  * Cadastro e controle de Despesas Fixas com recorrência parametrizável (Mensal, Diária, Personalizada).
  * Filtros por código, nome da despesa, status (Ativo/Inativo) e tipo de recorrência.

---

### 🏋️ **RF12 - Fichas de Treino e Prescrição de Exercícios**
**Descrição**: Montagem, organização e prescrição de rotinas de treino para os alunos.
- **Funcionalidades esperadas**:
  * **Fichas de Treino**: Criação, busca e vinculação de fichas aos alunos com período de validade.
  * **Biblioteca de Exercícios**: Organização por grupos musculares (Bíceps, Pernas, Peito, etc.) com inclusão de instruções e mídias.
  * **Grupos Musculares**: Classificação por tipos de membro (Superiores, Inferiores, Aeróbio).
  * **Objetivos de Treino**: Definição e categorização de metas de treino (ex: Hipertrofia, Emagrecimento).
  * **Grupos e Turmas de Treino**: Associação de alunos a grupos de treino (Treino Livre, Personal, Turma dos Bodybuilders) e parametrização de caixa interno/externo.

---

### 🏦 **RF13 - Gestão Financeira Avançada (Caixas, Gateway e Relatórios)**
**Descrição**: Administração de caixas diários, faturamento via gateway e emissão de relatórios.
- **Funcionalidades esperadas**:
  * **Caixas**: Abertura, fechamento e histórico de caixas com validação por chaves compostas.
  * **Pagar.me (Gateway)**: Dashboard de integração mostrando saldo disponível para saque, recebíveis futuros, métodos de pagamento e solicitações de repasse.
  * **Relatórios**: Geração e exportação em PDF de relatórios consolidados de Avaliações, Clientes, Colaboradores, Matrículas, Contas a Receber, Contas a Pagar e Caixas.

---

### 🎯 **RF14 - Módulo Comercial (CRM Prospecção e Planos)**
**Descrição**: Funil de vendas de novos alunos e estruturação da esteira de produtos e contratos.
- **Funcionalidades esperadas**:
  * **Prospecção (CRM)**: Gestão de Leads por estágios (Novo Contato, Interessado, Proposta, Fez Aula Experimental, Fechado).
  * **Planos**: Cadastro de planos com parametrização de valor, duração, mensalidade e ranking de adesão.
  * **Modelos de Contrato**: Cadastro de minutas e termos contratuais para assinatura.
  * **Tipos de Pagamento e Bandeiras**: Configuração de meios de pagamento aceitos e bandeiras de cartão.

---

### ⚙️ **RF15 - Gestão de Pessoas, Fornecedores e Utilidades**
**Descrição**: Administração do quadro de colaboradores, fornecedores e engajamento interno.
- **Funcionalidades esperadas**:
  * **Colaboradores e Funções**: Cadastro da equipe, atribuição de cargos (Treinador, Personal, Avaliador, Recepção) e identificação biométrica.
  * **Fornecedores e Tipos de Documento**: Mapeamento de parceiros comerciais e categorização de comprovantes fiscais/trabalhistas.
  * **Gamificação (Atividades e Pontuação)**: Definição de tarefas que geram pontos para os alunos (ex: postar treino nas redes sociais).
  * **Loja de Produtos**: Venda de itens e resgate por pontos acumulados.
  * **Enquetes**: Criação de pesquisas de satisfação internas.

---

### 📋 **RF16 - Módulo de Saúde e Fichas de Anamnese**
**Descrição**: Aplicação de questionários de saúde e antecedentes médicos.
- **Funcionalidades esperadas**:
  * Cadastro de modelos de anamnese estruturados por categorias (Alimentação, Energia, Lesões).
  * Banco de Perguntas personalizadas com formatos de resposta (Sim/Não, Múltipla escolha, Texto complementar).
  * Aplicação e vinculação da ficha de anamnese durante ou após o processo de matrícula do aluno.

---

### 🤖 **RF17 - Inteligência e Automação**
**Descrição**: Motor de regras e inteligência voltado para a retenção de alunos e comunicação automática.
- **Funcionalidades esperadas**:
  * **Central de Automações**: Monitoramento de regras ativas (Risco de Evasão, Mensagens de Aniversariantes) via WhatsApp.
  * **Resultados de IA**: Painel consolidado com contagem de automações executadas, relatórios enviados, alunos monitorados e métrica de frequência média.

---

### 🛠️ **RF18 - Configurações Gerais do Sistema e Aplicativo Mobile**
**Descrição**: Parametrização global do comportamento do software e central de comunicação móvel.
- **Funcionalidades esperadas**:
  * **Configurações Globais**: Definição do plano contratado, liberação de acesso desktop, tipo de controle de presença, prazos para considerar cliente inativo, percentual de juros/multa por atraso e obrigatoriedade de anamnese na matrícula.
  * **Modelos de Ficha**: Customização do layout impresso e digital das fichas de treino.
  * **Comunicação no App Mobile**: Envio de Notificações Push aos alunos, publicação de avisos na linha do tempo e painel de moderação de denúncias.
