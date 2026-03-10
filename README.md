# 📡 Telecom X: Predição de Evasão de Clientes (Churn)

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)

## 📖 Sobre o Projeto
Este projeto apresenta uma solução de ciência de dados de ponta a ponta para o problema de **Churn** (evasão de clientes) da Telecom X. O trabalho evoluiu de uma análise descritiva inicial para a construção de modelos preditivos capazes de antecipar o cancelamento de serviços, permitindo que a empresa tome decisões baseadas em dados para reter sua base de clientes.

---

## 🎯 Objetivos do Projeto
* **Explorar e Limpar:** Extrair dados de fontes complexas (JSON) e garantir a qualidade para análise.
* **Identificar Padrões:** Entender quais perfis de clientes e serviços estão mais propensos à evasão.
* **Prever o Churn:** Desenvolver modelos de Machine Learning para sinalizar clientes em risco com antecedência.

---

## 🛠️ Tecnologias Utilizadas
* **Python** (Linguagem principal)
* **Pandas & NumPy:** Manipulação e tratamento de dados estruturados.
* **Matplotlib & Seaborn:** Visualização de dados e matrizes de confusão.
* **Scikit-Learn:** Implementação de algoritmos de Machine Learning (Logistic Regression e Random Forest), Escalonamento (StandardScaler) e Métricas de Avaliação.

---

## 📂 Estrutura do Repositório
```text
telecom-x-churn-analysis
│
├── TelecomX_BR.ipynb           # Notebook completo (ETL, EDA e Machine Learning)
├── TelecomX_tratado.csv        # Dataset limpo e padronizado gerado na Parte 1
└── README.md                   # Documentação do projeto

```

---

## ⚙️ Etapas de Desenvolvimento

### 1️⃣ ETL e Limpeza (Parte 1)

* Achatamento de dados JSON aninhados via `json_normalize`.
* Tratamento de tipos de dados (conversão de `Total` para float).
* Padronização de strings e remoção de colunas irrelevantes (`customerID`).

### 2️⃣ Análise Exploratória e Correlação

* Identificação de desbalanceamento de classe (26% de Churn).
* Uso de Heatmaps para identificar que **Fibra Óptica** e **Mensalidades Altas** são os maiores preditores de saída.
* Constatação de que o **Tempo de Contrato (Tenure)** é o principal fator de retenção.

### 3️⃣ Modelagem Preditiva (Parte 2)

* **Pré-processamento:** Aplicação de *One-Hot Encoding* para variáveis categóricas e *StandardScaler* para normalização.
* **Divisão de Dados:** Separação em 80% treino e 20% teste com estratificação.
* **Treinamento:** Comparação entre **Regressão Logística** (Modelo Linear) e **Random Forest** (Modelo de Árvores).

---

## 📊 Resultados e Performance

Avaliamos os modelos focando no **Recall**, pois para o negócio é mais custoso perder um cliente não identificado do que gerar um "falso alarme".

| Modelo | Acurácia | Recall (Sensibilidade) | F1-Score |
| --- | --- | --- | --- |
| **Regressão Logística** | **79,3%** | **52,1%** | **0.57** |
| Random Forest | 78,5% | 45,4% | 0.53 |

**Conclusão Técnica:** A **Regressão Logística** foi selecionada como o modelo final devido à sua melhor capacidade de generalização e superioridade em identificar clientes em evasão (melhor Recall), sem apresentar o *overfitting* observado no Random Forest.

---

## 🧠 Insights e Estratégia de Negócio

Com base na inteligência do modelo, as recomendações para a Telecom X são:

* **Foco no Onboarding:** Ações de retenção devem ser intensificadas nos primeiros 12 meses, onde o risco de churn é crítico.
* **Plano de Ação para Fibra Óptica:** Investigar a estabilidade do serviço de fibra, que apresenta correlação anormal com cancelamentos.
* **Incentivo à Fidelidade:** Converter clientes "mês a mês" para contratos anuais, utilizando o modelo para oferecer descontos preventivos aos clientes sinalizados com alto risco.

---

## 🚀 Melhorias Futuras

* Implementação de técnicas de balanceamento de carga (SMOTE) para melhorar o Recall.
* Teste de algoritmos de Boosting (como XGBoost ou LightGBM).
* Criação de um dashboard interativo para monitoramento em tempo real dos clientes em risco.

---

## 👩‍💻 Autora

Projeto desenvolvido por **Nicole Marcondes** como parte do desafio de Analista de Machine Learning da Telecom X.

