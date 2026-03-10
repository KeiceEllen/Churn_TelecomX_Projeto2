Churn_TelecomX_Projeto2


📊 Previsão de Churn de Clientes | Projeto de Machine Learning
🚀 Problema de Negócio

O churn de clientes é um dos principais desafios em empresas de telecomunicações, pois impacta diretamente a receita recorrente e aumenta o custo de aquisição de novos clientes.

Este projeto tem como objetivo identificar clientes com alta probabilidade de cancelamento, permitindo que a empresa atue de forma preventiva com estratégias de retenção baseadas em dados.

🎯 Objetivos

Construir um modelo preditivo para classificar clientes com risco de churn

Identificar os principais fatores que levam à evasão

Garantir um pipeline robusto e sem vazamento de dados (data leakage)

Traduzir resultados técnicos em insights estratégicos para o negócio

🛠️ Tecnologias Utilizadas

Python

Pandas

NumPy

Scikit-Learn

Pipeline & ColumnTransformer

Regressão Logística

Random Forest

🔍 Metodologia

1️⃣ Preparação dos Dados

Conversão da variável TotalCharges para formato numérico

Tratamento de valores ausentes com SimpleImputer

Separação de treino e teste com stratify

Aplicação de StandardScaler para variáveis numéricas

One-Hot Encoding para variáveis categóricas

2️⃣ Construção do Pipeline

Todo o pré-processamento foi encapsulado em um Pipeline, garantindo:

Reprodutibilidade

Ausência de vazamento de dados

Facilidade para deploy futuro

Código mais organizado e escalável

3️⃣ Treinamento do Modelo

Modelos avaliados:

Regressão Logística (class_weight='balanced')

Random Forest

📊 Importância das Variáveis (Principais Fatores de Churn)

Variável	Importância

customer_tenure	0.196
account_Charges.Total	0.161
account_Charges.Monthly	0.118
internet_InternetService_Fiber optic	0.091
account_PaymentMethod_Electronic check	0.073
account_Contract_Two year	0.068
account_Contract_One year	0.041
internet_InternetService_No	0.032
account_PaperlessBilling	0.029
internet_TechSupport	0.028

📈 Principais Insights

🔹 1. Tempo de permanência (Tenure) é o maior preditor de churn

Clientes nos primeiros meses apresentam maior risco de cancelamento.

➡ Estratégia: criar campanhas de retenção nos primeiros 90 dias.

🔹 2. Valor da mensalidade influencia diretamente o churn

Mensalidades mais altas aumentam a probabilidade de cancelamento.

➡ Estratégia: oferecer planos personalizados ou descontos.

🔹 3. Contratos de longo prazo reduzem a evasão

Clientes com contratos de 1 ou 2 anos possuem menor risco de churn.

➡ Estratégia: incentivar contratos anuais com benefícios.

🔹 4. Método de pagamento impacta a retenção

Clientes que utilizam electronic check apresentam maior risco de cancelamento.

➡ Estratégia: incentivar débito automático ou cartão.

📉 Avaliação do Modelo

O modelo foi avaliado em um conjunto de teste não balanceado, para simular um cenário real.

Métricas utilizadas:

Accuracy

Precision

Recall

F1-score

Matriz de confusão

💡 Impacto para o Negócio

Com a implementação deste modelo, a empresa pode:

Reduzir churn com ações direcionadas

Diminuir o CAC (Custo de Aquisição de Clientes)

Melhorar a previsibilidade de receita

Priorizar clientes com maior risco de cancelamento

Criar campanhas de retenção baseadas em dados

⚡ Melhorias Futuras

Cross-validation

Ajuste de hiperparâmetros (GridSearch / RandomSearch)

Uso de XGBoost / LightGBM

SHAP values para maior interpretabilidade

Deploy do modelo via API (FastAPI ou Flask)

Criação de dashboard para monitoramento do churn
