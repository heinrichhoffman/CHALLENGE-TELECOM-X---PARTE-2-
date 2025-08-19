# CHALLENGE-TELECOM-X---PARTE-2-
Análise e Modelagem Preditiva de Churn de Clientes 
Análise e Modelagem Preditiva de Churn de Clientes
Descrição do Projeto

Este repositório apresenta a segunda etapa do projeto da Telecom X, cujo foco foi o desenvolvimento de modelos de Machine Learning para prever a evasão de clientes (churn). O trabalho contempla desde o pré-processamento e análise dos dados até a avaliação e interpretação dos modelos, sempre com o objetivo de gerar informações estratégicas que auxiliem a empresa a reduzir cancelamentos e aumentar a retenção.

Objetivos

O projeto tem como principais metas:

-Identificar variáveis que influenciam diretamente a evasão de clientes;
-Criar modelos preditivos capazes de antecipar quais clientes possuem maior risco de cancelar o serviço;
-Fornecer insights práticos para apoiar decisões de negócio voltadas à fidelização.

Etapas Desenvolvidas

-Exploração dos Dados
-Carregamento do arquivo dados_tratados.csv;
-Análise inicial da estrutura e consistência das variáveis.
-Tratamento de Dados
-Remoção de registros com valores ausentes na coluna Cancelou;
-Salvamento do dataset limpo em dados_tratados.csv.
-Balanceamento de Classes
-Cálculo da proporção entre clientes que cancelaram (Yes) e os que permaneceram (No);
-Identificação de desbalanceamento entre as classes.
-Codificação de Variáveis Categóricas
-Aplicação do One-Hot Encoding (pd.get_dummies);
-Exclusão da coluna ID_Cliente por não agregar valor ao modelo.
-Análise de Correlação
-Geração da matriz de correlação entre variáveis numéricas e a variável alvo (Cancelou_Yes);

Destaque para variáveis relevantes como:

Tipo_Internet_Fiber optic

Metodo_Pagamento_Electronic check

Cobranca_Mensal

Fatura_Digital_Yes

Meses_Permanencia (com correlação negativa).

Análise Exploratória

Visualização com boxplots de Meses_Permanencia e Cobranca_Total em relação à evasão;


Conclusão: 
clientes que cancelam tendem a permanecer menos tempo e gerar menor faturamento total.

Preparação dos Dados para Modelagem

Separação de variáveis explicativas (X) e alvo (y);

Divisão em treino (70%) e teste (30%) com estratificação;

Aplicação do SMOTE para balancear as classes no conjunto de treino.

Modelagem Preditiva

Algoritmos utilizados:

Random Forest Classifier (sem normalização);

KNeighbors Classifier (KNN) (com normalização via StandardScaler).

Avaliação com métricas de precision, recall e f1-score, além de matrizes de confusão.

Ajuste de Hiperparâmetros (Random Forest)

Uso do GridSearchCV com otimização para f1-macro;

Melhores parâmetros encontrados:

{'class_weight': 'balanced', 'max_depth': 15, 'min_samples_split': 2, 'n_estimators': 100}


Importância das Variáveis (Random Forest)

Fatores mais relevantes para previsão de churn:

Meses_Permanencia

Cobranca_Total

Cobranca_Mensal

Tipo_Contrato_Two year

Tipo_Contrato_One year

Suporte_Tecnico_Yes

OnlineSecurity_Yes

Resultados Obtidos

O modelo Random Forest apresentou desempenho superior ao KNN, especialmente no recall da classe positiva (Cancelou_Yes).

Foram identificados como principais determinantes da evasão: tempo de permanência, tipo de contrato, valor da cobrança e adesão a serviços adicionais.

Estratégias Recomendadas

Investir em ações de retenção durante os primeiros meses de relacionamento;

Incentivar contratos de maior duração;

Ampliar a adesão a serviços agregados (como suporte técnico e segurança online);

Investigar causas de insatisfação em clientes de internet via fibra óptica;

Utilizar o modelo de Random Forest para prever clientes em risco e oferecer abordagens personalizadas.

Tecnologias Utilizadas

Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Imbalanced-learn)

Jupyter Notebook

SMOTE para balanceamento de classes

GridSearchCV para otimização de modelos

Estrutura de Arquivos
|-- dados_tratados.csv      # Base de dados tratada
|-- notebook_projeto.ipynb  # Análises e modelagem
|-- README.md               # Documentação do projeto

