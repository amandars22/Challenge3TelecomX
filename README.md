Análise Preditiva de Evasão de Clientes (Churn) na TelecomX
1. Introdução
Este projeto consiste em uma análise de dados completa para identificar e prever a evasão de clientes (churn) de uma empresa de telecomunicações fictícia, a TelecomX. O objetivo principal é entender os fatores que levam os clientes a cancelar seus serviços e, a partir daí, construir modelos de Machine Learning capazes de prever quais clientes têm maior probabilidade de evadir. Os insights gerados servem para que a empresa possa criar estratégias de retenção mais eficazes.

2. Metodologia
O projeto seguiu um fluxo de trabalho padrão em Ciência de Dados, executado em um ambiente Google Colab utilizando Python e as bibliotecas Pandas, Matplotlib e Scikit-learn.

As etapas principais foram:

Carregamento e Pré-processamento de Dados:

Dados carregados diretamente de um arquivo JSON.

Colunas complexas (com dicionários aninhados) foram "achatadas" para facilitar a manipulação.

Dados faltantes foram tratados, e a coluna de faturamento (TotalMensal) foi convertida para o tipo numérico.

Colunas irrelevantes (como o ID do cliente) foram removidas para otimizar a modelagem.

Análise Exploratória de Dados (EDA):

Análise descritiva para entender a distribuição e o comportamento dos clientes.

Visualização da proporção de clientes que evadiram vs. os que permaneceram.

Exploração da relação entre a evasão e variáveis categóricas (tipo de contrato, método de pagamento) e numéricas (tempo de contrato, total gasto).

Engenharia de Features e Modelagem:

Variáveis categóricas foram transformadas em formato numérico utilizando One-Hot Encoding para serem compatíveis com os modelos.

A variável-alvo (Churn) foi analisada para verificar desequilíbrio de classes.

O conjunto de dados foi dividido em treino e teste (80/20).

Dois modelos de Machine Learning foram construídos:

Regressão Logística: Modelo linear, simples e interpretável, que exigiu a normalização dos dados.

Random Forest: Modelo mais complexo e robusto, que não exigiu normalização.

Avaliação e Conclusões:

Os modelos foram avaliados usando métricas como Acurácia, Precisão, Recall e F1-score, além da Matriz de Confusão.

As variáveis mais importantes para a previsão de churn foram identificadas em cada modelo.

3. Principais Insights e Resultados
A análise e a modelagem preditiva revelaram os seguintes pontos-chave:

Desempenho dos Modelos: Ambos os modelos, Regressão Logística e Random Forest, apresentaram um desempenho comparável, com acurácias acima de 79%. Isso sugere que a Regressão Logística, por ser mais simples e interpretável, é uma ótima candidata para a implementação.

Fatores de Churn: As variáveis com maior impacto na previsão de evasão foram:

Contrato Mensal: Clientes com esse tipo de contrato são os mais propensos a evadir.

Tempo de Contrato: A maioria das evasões ocorre nos primeiros meses de serviço.

Método de Pagamento (Cheque Eletrônico): Clientes que utilizam este método de pagamento têm uma alta taxa de churn.

Serviços Online: A ausência de serviços online também foi um fator relevante.

4. Recomendações Estratégicas
Com base nos resultados, as seguintes ações podem ser tomadas pela TelecomX para reduzir a evasão de clientes:

Incentivar Contratos de Longo Prazo: Oferecer descontos e benefícios para clientes que optarem por planos anuais ou bianuais.

Programa de Boas-Vindas: Implementar um acompanhamento ativo de clientes nos primeiros seis meses para garantir a satisfação e resolver problemas de forma proativa.

Análise do Método de Pagamento: Investigar a experiência do usuário que utiliza o cheque eletrônico para identificar e corrigir possíveis problemas.
