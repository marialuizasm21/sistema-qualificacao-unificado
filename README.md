# Sistema Unificado de Qualificação de Leads

Sistema centralizado de qualificação desenvolvido com **engenharia de prompts e automação assistida por IA**, implementando 6 workflows integrados para eliminar descentralização, duplicidade e criar segmentação automática de leads.

**Desenvolvido utilizando Claude AI (Anthropic) para prompt engineering, arquitetura de código e otimização de workflows.**

---

## Skills Desenvolvidas

![Prompt Engineering](https://img.shields.io/badge/Prompt-Engineering-ff69b4?style=for-the-badge&logo=openai&logoColor=white)
![Claude AI](https://img.shields.io/badge/Claude%20AI-Anthropic-4A90E2?style=for-the-badge&logo=anthropic&logoColor=white)
![Workflows de Automação](https://img.shields.io/badge/Workflows-de%20Automação-green?style=for-the-badge)
![Segmentação de Leads](https://img.shields.io/badge/Segmentação-de%20Leads-blue?style=for-the-badge)
![JavaScript](https://img.shields.io/badge/JavaScript-Apps%20Script-yellow?style=for-the-badge&logo=javascript&logoColor=black)
![Processamento de Dados](https://img.shields.io/badge/Processamento-de%20Dados-orange?style=for-the-badge)
![Validação Multicamadas](https://img.shields.io/badge/Validação-Multicamadas-red?style=for-the-badge)
![Arquitetura de Sistemas](https://img.shields.io/badge/Arquitetura-de%20Sistemas-purple?style=for-the-badge)

---

## O Problema

O processo de qualificação operava através de **múltiplas planilhas descentralizadas** criadas individualmente para cada lista ou campanha.

### Fragmentação e Descentralização
- Múltiplas planilhas criadas sem padronização ou controle central
- Impossibilidade de acompanhamento geral consolidado
- Informações valiosas dispersas e inacessíveis para análises estratégicas
- Gestão do conhecimento comprometida pela falta de centralização

### Problemas de Acesso
- Nem todos os membros da equipe tinham permissão em todas as planilhas
- Dificuldade de compartilhamento entre áreas
- Barreiras operacionais causadas por restrições de acesso

### Alto Risco de Duplicidade
- Falta de visão integrada aumentava risco de qualificar o mesmo lead duas vezes
- Sem validação automática entre diferentes planilhas
- Retrabalho constante e perda de tempo

### Falta de Padronização e Segmentação
- Cada planilha com estrutura diferente
- Dossiês escritos de forma inconsistente
- Sem modelo de segmentação ou priorização automática
- Dificuldade de comparação e análise entre listas

**Impacto:** Operação ineficiente, tomada de decisões prejudicada, retrabalho constante, falta de visão estratégica.

### Solução
Desenvolvi **sistema unificado** que evoluiu progressivamente através de **4 versões** ao longo de 3 dias (12 horas total), implementando **6 automações integradas**.

**Diferencial:** Utilizei **Claude AI (Anthropic)** extensivamente durante todo o desenvolvimento para engenharia de prompts, arquitetura de código e otimização de workflows de automação.

### Versão 1: Protótipo - Estrutura Base

Implementação de 4 scripts fundamentais que estabeleceram a base do sistema:

**Timestamp Automático:**
- Registra data e hora automaticamente ao atribuir responsável
- Elimina necessidade de preenchimento manual
- Cria rastreabilidade temporal de qualificações

**Verificação de Duplicados:**
- Valida nome da empresa E email
- Aplica lógica temporal (mantém registro mais antigo)
- Ignora células vazias para evitar falsos positivos

**Geração de Dossiê:**
- Compila 14 campos em texto estruturado
- Cria contexto automatizado
- Padroniza formato de documentação

**Verificação em Base Master:**
- Cruza com base externa de leads já mapeados
- Normalização avançada de texto (remove acentos, sufixos corporativos)
- Identifica leads já processados anteriormente

**Funcionalidades implementadas:**
- Remoção automática de acentos
- Limpeza de sufixos corporativos (LTDA, SA, ME, Eireli)
- Validação por nome OU email
- Geração automática de contexto

### Versão 2: Produção - Dossiê Profissional

Transformação do dossiê simples em **documento profissional estruturado**:

**Estrutura em 4 Seções:**
- **Perfil e Operação** - Segmento, localização, formato de eventos
- **Cálculo de Valor Estimado** - Metodologia detalhada com margem de segurança
- **Análise de Concorrência** - Benchmark completo de taxas e plataformas
- **Históricos e Contatos** - Decisores, formas de contato, relacionamento

**Evoluções técnicas:**
- Expandiu mapeamento de **14 → 24 campos**
- Implementou gatilho de segurança (só executa em registros válidos)
- Criou função `validar()` para tratar campos vazios elegantemente
- Adicionou cálculo com margem de segurança de 60%
- Incluiu benchmark detalhado de concorrência

### Versão 3: Atual - Inteligência e Segurança

Adição de **camadas de inteligência e validação de contexto**:

**Validação de Ambiente:**
- Todos os scripts validam execução apenas na aba correta
- Previne erros de execução em contexto incorreto
- Aumenta confiabilidade do sistema

**Dossiê Expandido para 7 Seções:**
- Separação granular de informações
- Estrutura mais profissional e navegável
- Facilita leitura e análise

**Lógica Condicional Inteligente:**
- Constrói frases apenas com campos preenchidos
- Omite seções vazias automaticamente
- Gera narrativa fluida independente de dados faltantes
- Elimina menções a "não informado"

**Melhorias de UX:**
- Verificação silenciosa (sem pop-ups intrusivos)
- Retorna motivos específicos ao invés de categorias genéricas
- Adiciona campos para classificação comercial

### Versão Final: Sistema Completo com Segmentação Automática

Implementação de **modelo de segmentação automática** baseado em regras de negócio:

**Sistema de Flags Automáticas (Red/Yellow/Green):**
- **Red Flag**: Leads descartados (bad-fit definitivo)
- **Yellow Flag**: Aguardar timing (contratos ativos, timing específico)
- **Green Flag**: Pronto para ação (sem impeditivos)

**Trigger Unificado:**
- Consolida timestamp + sistema de flags em 1 função
- Reduz complexidade e melhora performance
- Facilita manutenção e debug

**Novas Funções:**
- `calcularFlag()`: Lógica hierárquica de prioridades para segmentação
- `atualizarEmLote()`: Processamento da base histórica completa

**Validações Adicionais:**
- Verifica status antes de gerar dossiê
- Identifica casos especiais automaticamente
- Adiciona linhas contextuais no dossiê quando aplicável

**Total de automações integradas: 6**

---

## Aplicação de IA no Projeto

### Prompt Engineering para Desenvolvimento

Utilizei **Claude AI (Anthropic)** extensivamente ao longo das 4 versões:

**Arquitetura de Código:**
- Engenharia de prompts para projetar estrutura de validação multicamadas
- Geração de lógica condicional complexa através de iterações com IA
- Otimização de funções de normalização de texto
- Code review e sugestões de melhoria assistidas por IA

**Exemplos de Aplicação:**

Prompt usado: "Preciso criar uma função que valide duplicados
por nome OU email, aplicando normalização de texto que remova
acentos, sufixos corporativos e mantenha o registro mais antigo.
Como estruturar essa lógica em Apps Script?"

Resultado: Função verificarDuplicados() com normalização NFD
e lógica temporal


**Workflows de Automação:**
- Design de triggers inteligentes via prompts estruturados
- Lógica hierárquica de segmentação desenvolvida com IA
- Otimização de processamento em lote

**Validação e Testes:**
- Identificação de edge cases através de prompts
- Sugestões de validações adicionais
- Debugging assistido

### Estruturação de Dados

**Extração e Normalização:**
- Algoritmos de normalização de texto (NFD, regex)
- Remoção de sufixos corporativos
- Limpeza de espaços e caracteres especiais

**Processamento de Informações:**
- Mapeamento de 27 campos estruturados
- Compilação automática de dossiês em 7 seções
- Lógica condicional para construção de narrativa

### Segmentação de Leads

**Modelo de Classificação Automática:**
- Sistema baseado em regras hierárquicas (Red/Yellow/Green)
- Lógica de priorização para direcionamento de leads
- Atualização em tempo real conforme dados são preenchidos

**Benefício para Time Comercial:**
- Priorização automática sem interpretação subjetiva
- Direcionamento claro: descartar (Red), aguardar (Yellow), contatar (Green)
- Base para estratégia de abordagem

---

## Tecnologias

**Plataforma e Linguagem:**
- Google Sheets - Interface e armazenamento de dados
- Google Apps Script - JavaScript server-side para automações
- Triggers automáticos (onEdit)

**Inteligência Artificial:**
- **Claude AI (Anthropic)** - Prompt engineering para desenvolvimento
- Code generation e otimização assistida por IA
- Arquitetura de workflows com IA

**Integrações:**
- API do Google Sheets para planilhas externas
- Conexão cross-sheet para base master

**Processamento de Dados:**
- Normalização de texto (NFD normalization)
- Regex para limpeza e validação
- Lógica temporal para deduplicação

**Validação e Segmentação:**
- Sistema multicamadas de validação
- Modelo de segmentação automática (flags)
- Lógica hierárquica de prioridades

**Funções Avançadas:**
- IFS, E, OU, CONT.SE, PROCX, ARRAYFORMULA
- Mapeamento estruturado de colunas
- Processamento em lote

**Arquitetura:**
- Design evolutivo (4 versões progressivas)
- Trigger unificado
- Workflows automatizados

---

## Resultados

### Quantitativos

- **6 automações** integradas funcionando em produção
- **27 campos** mapeados e processados automaticamente
- **7 seções** estruturadas no dossiê profissional
- **100%** das qualificações centralizadas em planilha única
- **0 duplicidades** através de validação automática
- **4 versões** progressivas desenvolvidas em 3 dias
- **3 categorias de segmentação** (Red/Yellow/Green flags)

### Qualitativos

- **Centralização total** - Uma única fonte de verdade para toda equipe
- **Zero retrabalho** - Validação automática elimina qualificação duplicada
- **Democratização de acesso** - Todos os membros trabalham na mesma base sem restrições
- **Padronização absoluta** - Qualidade consistente independente do operador
- **Segmentação automática** - Sistema de flags elimina interpretação subjetiva e prioriza leads
- **Escalabilidade** - Suporta crescimento de volume sem reengenharia
- **Onboarding simplificado** - Novos membros produzem desde o primeiro dia
- **Rastreabilidade completa** - Histórico auditável de todas as qualificações

### Em Produção

Sistema entregue e utilizado diariamente por toda equipe de qualificação, eliminando necessidade de criar e gerenciar múltiplas planilhas descentralizadas.

---

## Fluxo de Trabalho

### 1. Atribuição de Responsável
Qualificador preenche coluna de proprietário e o sistema:
- Registra automaticamente data e hora na coluna adjacente
- Cria timestamp imutável para rastreabilidade

### 2. Preenchimento de Dados
Durante o preenchimento dos campos:
- Sistema monitora edições em campos-chave
- Valida contexto (executa apenas na aba correta)
- Prepara dados para validação

### 3. Validação de Duplicados
Ao finalizar preenchimento:
- Sistema verifica nome da empresa (coluna T)
- Verifica email (coluna AD)
- Aplica normalização (remove acentos, sufixos, espaços)
- Compara com todos os registros existentes
- Marca como duplicado se encontrar match com data posterior

### 4. Verificação em Base Master
Automaticamente cruza dados com base externa:
- Busca por nome OU email normalizado
- Identifica se lead já foi mapeado anteriormente
- Retorna motivo específico de desqualificação (se aplicável)
- Execução silenciosa sem interromper operação

### 5. Segmentação Automática (Cálculo de Flags)
Ao preencher campos de outcome:
- Sistema avalia status (Bad-fit, Vendas, Fit Sympla)
- Aplica lógica hierárquica de prioridades
- Calcula flag automaticamente (Red/Yellow/Green)
- Atualiza status de importação
- **Direciona lead para time comercial conforme prioridade**

### 6. Geração de Dossiê
Quando status válido é definido:
- Sistema valida se deve gerar dossiê (Vendas/Bad-fit/Fit Sympla)
- Captura 27 campos via mapeamento de colunas
- Aplica lógica condicional para construir seções
- Compila texto estruturado em 7 seções
- Grava no campo de destino

### 7. Processamento em Lote (Opcional)
Para atualizar base histórica:
- Executa função `atualizarEmLote()` manualmente
- Processa todos os registros da linha 14 até o final
- Atualiza flags e status de importação em massa
- Exibe relatório de processamento

---

## Arquitetura de Scripts

### onEdit() - Trigger Unificado

Função principal que executa automaticamente a cada edição na planilha. Consolida múltiplas automações:

**Validação de Contexto:**
- Verifica se edição ocorreu na aba "NUTRIÇÃO"
- Interrompe execução se contexto incorreto
- Previne erros em outras abas

**Automação 1 - Timestamp:**
- Monitora coluna Q (Proprietário)
- Preenche coluna R com data/hora ao atribuir
- Limpa campo se proprietário for removido

**Automação 2 - Sistema de Flags:**
- Monitora colunas BF, BH, BI (Outcome, Motivos)
- Executa cálculo de flag quando campos são editados
- Atualiza status de importação automaticamente

### verificarDuplicados()

Validação de duplicidade com lógica temporal:

**Mapeamento:**
- Percorre todos os registros a partir da linha 14
- Mapeia valores de Nome (T) e Email (AD) com suas datas (R)
- Cria índice temporal para cada valor único

**Normalização:**
- Remove acentos via NFD normalization
- Remove sufixos corporativos (LTDA, SA, ME, Eireli, Serviços, Comercial)
- Remove espaços extras
- Converte para minúsculas

**Validação:**
- Compara cada registro com mapa temporal
- Identifica duplicados por nome OU email
- Mantém registro mais antigo como original
- Marca registros posteriores como duplicados
- Ignora células vazias

### gerarDossie()

Geração automática de dossiê profissional estruturado:

**Validação Prévia:**
- Verifica campo Outcome (BF)
- Só executa para: Vendas, Bad-fit, Fit Sympla
- Pula registros com status inválido

**Captura de Dados:**
- Mapeia 27 campos via índices de colunas
- Função `obterDado()` limpa espaços e valida valores
- Prepara dados para processamento

**Construção de Seções:**

1. **Perfil do Produtor e Operação**
   - Constrói frases apenas com campos preenchidos
   - Segmento, tema, subtema, localização, formatos
   - Sazonalidade e demandas ferramentais

2. **Identificação de Casos Especiais**
   - Adiciona linha de bad-fit com motivo (se aplicável)
   - Adiciona linha de fit sympla com motivo e data ideal (se aplicável)

3. **Cálculo Estimado de Valor**
   - GMV, carteira, range
   - Metodologia (Público × Ticket × Frequência)
   - Margem de segurança de 60%

4. **Plataforma Atual**
   - Plataforma concorrente
   - Taxas de serviço e processamento
   - Detalhes adicionais

5. **Histórico e Relacionamento**
   - Histórico Sympla (campo W)

6. **Histórico de Abordagens e Negociações**
   - Histórico Comercial (campo AA)

7. **Contato de Decisores**
   - Forma de contato, decisor, cargo, telefone, redes sociais

8. **Contexto Adicional**
   - Campo BJ com inteligência estratégica

**Compilação:**
- Une todas as seções em texto fluido
- Omite seções vazias
- Grava na coluna BK (destino)

### verificarBaseMaster()

Integração com planilha externa para verificação de leads já mapeados:

**Conexão:**
- Conecta com planilha master via ID
- Captura dados da aba específica
- Trata erros de conexão

**Normalização:**
- Aplica mesma normalização dos duplicados
- Remove acentos, sufixos, espaços
- Case insensitive

**Cruzamento:**
- Busca por nome (coluna T) OU email (coluna AD)
- Identifica categoria do lead (Bad-fit, Fit Sympla, Faixa F)
- Retorna motivo específico quando disponível

**Escrita:**
- Grava resultado na coluna J
- Execução silenciosa (log apenas no console)

### calcularFlag()

Função auxiliar com lógica hierárquica de prioridades baseada em regras de negócio:

**Regras de Segmentação:**

1. Bad-fit → Red Flag (descarte definitivo)

2. Vendas:
   - Sem data ideal → Green Flag (pronto para contato)
   - Com data ideal → Yellow Flag (aguardar timing)

3. Fit Sympla:
   - Timing ou Contrato ativo → Yellow Flag
   - Outros motivos impeditivos → Red Flag

**Normalização:**
- Converte outcome para lowercase
- Compara strings de forma case-insensitive

**Retorno:**
- String com flag calculada
- Vazio se nenhuma condição atender

### atualizarEmLote()

Processamento em massa da base histórica:

**Validação:**
- Verifica existência da aba "NUTRIÇÃO"
- Valida se há dados a partir da linha 14
- Exibe alertas se pré-condições não atendidas

**Processamento:**
- Loop de linha 14 até última linha preenchida
- Lê campos Outcome, Motivos, Data Ideal, Status atual
- Aplica `calcularFlag()` em cada linha
- Atualiza flag e status de importação

**Relatório:**
- Conta total de leads processados
- Conta flags atualizadas
- Conta status atualizados
- Exibe modal com resumo completo

---

## Diferenciais

### Uso Extensivo de IA no Desenvolvimento

**Prompt Engineering Aplicado:**
- Claude AI utilizado em todas as 4 versões do projeto
- Engenharia de prompts para arquitetar lógica complexa
- Iterações com IA para otimização de código
- Code generation assistida mantendo qualidade

**Workflows de Automação:**
- Design de triggers inteligentes
- Lógica hierárquica de segmentação
- Validação multicamadas

### Processamento e Estruturação de Dados

**Normalização Avançada:**
- NFD normalization para remoção de acentos
- Regex para limpeza de sufixos corporativos
- Validação case-insensitive
- Tratamento de edge cases

**Extração de Informações:**
- Mapeamento de 27 campos estruturados
- Compilação automática em 7 seções
- Lógica condicional para construção de narrativa

### Modelo de Segmentação de Leads

**Classificação Automática:**
- Sistema baseado em regras hierárquicas
- Priorização clara para time comercial
- Atualização em tempo real

**Direcionamento Estratégico:**
- Red Flag: Descarte (economia de tempo)
- Yellow Flag: Aguardar timing (nurturing)
- Green Flag: Contato imediato (prioridade máxima)

### Evolução Progressiva

Desenvolvimento em 4 versões permitiu:
- Ajustes baseados em feedback real da operação
- Implementação incremental de funcionalidades
- Redução de riscos de reengenharia
- Validação contínua de cada camada

### Arquitetura Unificada

Trigger único centraliza múltiplas automações:
- Reduz complexidade de manutenção
- Melhora performance (menos execuções)
- Facilita debug e troubleshooting
- Código mais limpo e organizado

### Validação de Contexto

Todos os scripts validam ambiente de execução:
- Previne erros de execução em abas incorretas
- Melhora confiabilidade do sistema
- Reduz tickets de suporte
- Aumenta robustez operacional

---

## Aprendizados

### Prompt Engineering e IA

- **Engenharia de Prompts Estruturados** - Prompts bem formulados aceleram desenvolvimento de lógica complexa significativamente
- **Iteração com IA** - Processo iterativo de refinamento com Claude AI gera soluções mais robustas
- **Code Generation Assistida** - IA como copiloto mantém produtividade sem sacrificar qualidade
- **Validação por IA** - Identificação de edge cases e sugestões de melhoria complementam experiência

### Automação e Workflows

- **Triggers Unificados** - Centralizar múltiplas automações em 1 função melhora manutenibilidade e performance
- **Validação de Contexto** - Prevenir execução em ambientes incorretos reduz drasticamente bugs em produção
- **Processamento em Lote** - Essencial para migração de bases históricas sem retrabalho manual

### Processamento de Dados

- **Normalização de Texto** - Remoção agressiva de acentos e sufixos aumenta significativamente taxa de match
- **Lógica Condicional** - Construir texto apenas com dados existentes melhora UX e percepção de qualidade
- **Validação Multicamadas** - Quanto mais cedo capturar erros, menor o custo de correção

### Segmentação e Priorização

- **Modelos Baseados em Regras** - Regras de negócio claras codificadas eliminam interpretação subjetiva
- **Classificação Hierárquica** - Prioridades bem definidas facilitam direcionamento de recursos
- **Atualização em Tempo Real** - Feedback imediato aumenta confiança no sistema

### De Produto

- **Desenvolvimento Incremental** - Versões progressivas permitem validação contínua e ajustes baseados em feedback real
- **Padronização vs Flexibilidade** - Automação aumenta consistência mas requer regras de negócio bem definidas
- **Adoção Gradual** - Equipe adota melhor quando evolução é progressiva ao invés de mudança radical

---

## Limitações & Próximos Passos

### Limitações Atuais

- Sistema depende de estrutura fixa de colunas (mudanças exigem atualização de índices)
- Validação de duplicados compara apenas nome exato e email (variações sutis podem passar)
- Processamento em lote pode ser lento em bases muito grandes (1000+ registros)
- Lógica de flags hardcoded (mudanças de regras exigem alteração de código)
- Modelo de segmentação baseado apenas em regras (não utiliza machine learning)

### Próximos Passos

**Melhorias de Arquitetura:**
- Implementar mapeamento dinâmico de colunas (reduzir dependência de índices fixos)
- Adicionar fuzzy matching na validação de duplicados (capturar variações sutis de nome)
- Otimizar processamento em lote com chunking (processar em blocos menores)
- Externalizar regras de flags para configuração (permitir ajustes sem alterar código)

**Expansão com IA:**
- Integrar APIs de LLMs (OpenAI/Anthropic) para enriquecimento automático de dados
- Implementar análise de texto para extração de informações de fontes não estruturadas
- Adicionar modelo de ML para scoring preditivo de leads
- Criar sugestões de abordagem comercial personalizadas via IA

**Análise e Monitoramento:**
- Adicionar log de auditoria (rastrear quem fez qual alteração e quando)
- Implementar dashboard de métricas (visualização de KPIs em tempo real)
- Criar relatórios automáticos de performance de segmentação

---

## Autor

**Maria Luiza Moraes**  
Estagiária • Estratégia, Gestão e M&A @ Sympla

[LinkedIn](https://www.linkedin.com/in/maria-luiza-moraes-98a6b22a8/) • [GitHub](https://github.com/marialuizasm21)

---

**Nota:** O código completo dos scripts não está disponível publicamente por conter lógica de negócio proprietária. Este repositório serve como documentação do projeto para fins de portfólio.
