# Case de Estágio – Engenharia de Dados / Machine Learning

## Contexto
Uma startup de tecnologia financeira precisa criar uma solução simples para **analisar dados de transações de clientes** e prever a probabilidade de **inadimplência**.  
O objetivo é testar conhecimentos práticos em **engenharia de dados** e **machine learning**, utilizando a plataforma **Databricks (Free Edition)**.

---

## Objetivos do Case
1. **Ingestão de dados**: Carregar dados de transações (fornecidos em formato CSV).
2. **Transformação e limpeza**: Tratar valores nulos, duplicados e inconsistências.
3. **Análise exploratória**: Gerar estatísticas descritivas e visualizações.
4. **Feature Engineering**: Criar novas variáveis relevantes para o modelo.
5. **Treinamento de modelo (opcional)**: Criar um modelo simples de classificação (ex.: regressão logística ou árvore de decisão).
6. **Avaliação**: Medir a performance com métricas adequadas (AUC, F1, Precision/Recall).
7. **Entrega**: Organizar o código em **notebooks Databricks** e gerar um **relatório final** com os achados.

---

## Dataset
Será fornecido um dataset fictício de transações de clientes com as seguintes colunas:

- `id_cliente`: Identificador único do cliente.  
- `valor_transacao`: Valor monetário da transação.  
- `data_transacao`: Data da transação.  
- `categoria`: Categoria do gasto (ex.: mercado, transporte, lazer).  
- `inadimplente`: Variável alvo (0 = não inadimplente, 1 = inadimplente).  

---

## Tarefas Detalhadas

### 1. Ingestão de Dados
- Carregar o dataset CSV em um **Delta Table** no Databricks.
- Garantir que os tipos de dados estão corretos (`date`, `float`, `string`, `int`).

### 2. Qualidade e Transformação
- Tratar valores ausentes em `categoria` e `valor_transacao`.
- Remover duplicatas.
- Criar colunas derivadas, como:
  - **Média de gasto mensal por cliente**
  - **Número de transações por cliente**

### 3. Análise Exploratória
- Estatísticas descritivas (média, desvio padrão, valores mínimos/máximos).
- Distribuição de valores (`valor_transacao`).
- Visualização de inadimplência por categoria.

### 4. Feature Engineering
- Criar variáveis agregadas por cliente (ex.: total gasto no último mês).
- Codificar variáveis categóricas (`categoria` → One Hot Encoding).

### 5. Machine Learning (opcional)
- Separar os dados em treino (70%) e teste (30%).
- Treinar um modelo de classificação simples.
- Avaliar a performance do modelo com métricas adequadas.

### 6. Relatório Final
- Criar um notebook final explicando:
  - As transformações realizadas.
  - Insights dos dados.
  - Performance do modelo.
  - Limitações e sugestões de melhorias.

---

## Critérios de Avaliação
- Clareza e organização do código.
- Qualidade do tratamento de dados.
- Raciocínio analítico nas transformações e modelagem.
- Justificativa para escolhas de técnicas e métricas.
- Qualidade da comunicação no relatório final.

---

## Entregáveis
- Link para o **workspace no Databricks Free Edition** com os notebooks.
- Relatório final (Markdown no Databricks ou PDF exportado).
- Prazo de entrega é de até 7 dias após o recebimento do case.

---

## Extras (Opcional)
- Criar um job no Databricks para rodar o pipeline automaticamente.
- Utilizar MLflow para versionar experimentos de modelos.
- Implementar gráficos interativos para a análise exploratória.
