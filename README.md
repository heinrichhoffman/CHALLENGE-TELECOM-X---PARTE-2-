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

Conclusão: 
clientes que cancelam tendem a permanecer menos tempo e gerar menor faturamento total.



Estrutura de Arquivos
|-- dados_tratados.csv      # Base de dados tratada
|-- notebook_projeto.ipynb  # Análises e modelagem
|-- README.md               # Documentação do projeto

