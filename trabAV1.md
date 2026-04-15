Parte 1: Documentação do Pré-Projeto de BI (Padrão ABNT)
(Lembrete para os alunos sobre a formatação ABNT: Fonte Arial/Times 12, espaçamento 1,5, margens 3cm sup/esq e 2cm inf/dir. O documento deve conter Capa, Folha de Rosto, Resumo e Sumário antes da introdução).

1. Contexto sobre o Projeto e Problema de Negócio
Contexto: A empresa atua no varejo físico e online, mas seus dados estão em silos (o sistema do e-commerce não se comunica em tempo real com o ERP das lojas físicas).

Justificativa: A falta de consolidação dos dados gera relatórios manuais demorados, resultando em rupturas de estoque (faltam produtos que vendem muito) e excesso de produtos parados.

Objetivo: Desenvolver uma solução de BI que integre as bases de dados e forneça painéis gerenciais (Dashboards) diários para a diretoria, focando no cruzamento de vendas por região e giro de estoque.

2. Engenharia de Requisitos Aplicada a BI e Casos de Uso
Em projetos de dados, a engenharia de requisitos foca menos em "ações" de sistema e mais nas perguntas de negócio que precisam ser respondidas e nos KPIs (Indicadores Chave de Performance).

Requisitos Funcionais (Métricas e Dimensões):

O sistema deve apresentar o Faturamento Total diário, filtrável por Loja, Região e Canal (Online/Físico).

O sistema deve alertar sobre produtos com estoque abaixo de 15 dias de cobertura.

Atores Principais: Diretor Comercial, Gerente de Loja, Analista de Suprimentos.

Caso de Uso (UC01 - Analisar Performance de Vendas):

Ator: Diretor Comercial.

Fluxo: O diretor acessa o dashboard executivo; visualiza o KPI de Faturamento Mensal; clica no canal "E-commerce" para realizar um drill-down (detalhamento) e identifica qual categoria de produtos teve maior margem de lucro na última semana.

3. Diagramas (Arquitetura de Dados)
Na documentação de BI, os diagramas tradicionais de software dão lugar aos diagramas de dados. Os alunos devem incluir e referenciar no texto:

Diagrama de Arquitetura de Dados (Pipeline ETL/ELT): Mostrando a extração (E) dos dados do ERP e E-commerce, a transformação (T) com regras de negócio, e o carregamento (L) no Data Warehouse.

Modelagem Multidimensional (Star Schema): O diagrama fundamental do BI. Deve mostrar a Tabela Fato no centro (ex: Fato_Vendas, contendo valores, quantidades, descontos) ligada às Tabelas Dimensão ao redor (ex: Dim_Tempo, Dim_Produto, Dim_Loja, Dim_Cliente).

4. Interface (Telas e Dashboards)
Em vez de telas de aplicativos, os alunos devem prototipar as visões dos painéis.

Tela 1: Dashboard Executivo (Visão Macro): Focado em High-level KPIs (Receita Bruta, Ticket Médio, Custo de Aquisição de Clientes) com gráficos de linha mostrando tendências e mapas de calor de vendas por região.

Tela 2: Dashboard Operacional de Estoque: Tabelas dinâmicas detalhadas, destacando em vermelho SKUs (produtos) com risco de ruptura e gráficos de barras com o giro de estoque por categoria.

5. Tecnologias Utilizadas
A justificativa técnica do stack de dados:

Extração e Transformação (ETL): Python (com bibliotecas como Pandas) ou ferramentas low-code como Apache Hop / Talend para limpar e unificar os dados do e-commerce e ERP.

Armazenamento (Data Warehouse): Bancos de dados colunares ou em nuvem voltados para análise, como PostgreSQL, ou soluções Cloud (BigQuery).

Visualização de Dados (Front-end): Power BI, Metabase ou Looker Studio para a criação dos dashboards interativos, justificado pela facilidade de compartilhamento seguro com os gestores.

Parte 2: Apresentação em Slide (Máximo de 15 min)
A apresentação deve ser um "Pitch de Dados", convencendo a diretoria do valor do projeto.

1. O Problema (0 a 3 minutos)

Slide 1: Capa (Título do Projeto, Equipe).

Slide 2 (A Dor do Negócio): "Atualmente, a empresa leva 5 dias úteis para fechar o relatório de vendas mensal. Até lá, já perdemos oportunidades de reposição de estoque. Os dados existem, mas não conversam entre si."

2. A Solução (3 a 8 minutos)

Slide 3 (Engenharia de Requisitos): Quais foram as 3 principais perguntas de negócio que descobrimos que a diretoria precisava responder urgentemente?

Slide 4 (A Arquitetura): Um diagrama visual e simplificado mostrando os dados saindo do "caos" (fontes diversas) passando pelo funil (ETL) e chegando organizados no Data Warehouse.

Slide 5 (Stack Tecnológico): Apresentação rápida das ferramentas (Python, SQL, Power BI) e como elas garantem atualização automática diária (processamento em batch noturno).

3. O Produto (8 a 13 minutos) - A Mágica Acontece Aqui

Slide 6 (O Dashboard Executivo): Mostrar o protótipo da tela principal. O aluno deve explicar a leitura de um gráfico específico. "Com este mapa de calor, o diretor vê na hora que a região Nordeste está sem estoque do produto X."

Slide 7 (O Dashboard Operacional): Mostrar a tela de detalhamento. Explicar como a modelagem (Star Schema) permite filtrar dados de anos inteiros em segundos.

4. Fechamento e Impacto (13 a 15 minutos)

Slide 8 (Retorno sobre o Investimento - ROI): O que a empresa ganha? (Ex: Redução de 90% do tempo de confecção de relatórios e aumento de vendas por evitar prateleiras vazias).

Slide 9: Espaço para perguntas da banca.
