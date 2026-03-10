# 📡 Telecom X: Predição de Evasão de Clientes (Churn)

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)

## 📖 Sobre o Projeto
Este projeto apresenta uma solução completa de ciência de dados para o problema de **Churn** (evasão de clientes) da empresa fictícia Telecom X. O trabalho foi dividido em duas fases principais:
1. **Análise Exploratória (EDA):** Identificação de padrões e comportamentos dos clientes.
2. **Machine Learning:** Desenvolvimento de modelos preditivos para antecipar cancelamentos.

---

## 🎯 O Problema de Negócio
A Telecom X identificou uma perda significativa de receita devido ao cancelamento de assinaturas. O objetivo deste projeto foi descobrir **por que** os clientes saem e criar uma ferramenta que avise **quem** tem maior probabilidade de sair, permitindo ações preventivas de retenção.

---

## 🛠️ Tecnologias e Ferramentas
* **Linguagem:** Python 3.x
* **Manipulação de Dados:** Pandas, NumPy
* **Visualização:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn (Logistic Regression, Random Forest, StandardScaler)

---

## 📂 Estrutura do Repositório
* `TelecomX_BR.ipynb`: Notebook contendo todo o código, desde a limpeza até o modelo final.
* `TelecomX_tratado.csv`: Dataset limpo e padronizado após a Fase 1.
* `README.md`: Documentação do projeto.

---

## 📊 Fase 1: Descobertas Principais (EDA)
Durante a análise exploratória, identificamos os "sinais de alerta" da empresa:
* **Fibra Óptica:** Clientes com esta tecnologia cancelam muito mais do que os de planos DSL.
* **Contratos Mensais:** A ausência de fidelidade facilita a saída imediata.
* **O "Vale do Churn":** A maior parte das desistências ocorre nos primeiros 12 meses de contrato.

---

## 🤖 Fase 2: Inteligência Preditiva
Preparamos os dados com *One-Hot Encoding* e *Standard Scaling* para treinar dois modelos de classificação.

### Comparativo de Performance
| Modelo | Acurácia | Recall (Foco no Churn) | F1-Score |
| :--- | :---: | :---: | :---: |
| **Regressão Logística** | **79%** | **52%** | **0.57** |
| Random Forest | 78% | 45% | 0.53 |

**Decisão Técnica:** Optamos pela **Regressão Logística**. Para o negócio, o *Recall* é a métrica mais valiosa, pois indica nossa capacidade de identificar o cliente em risco. A Regressão Logística conseguiu identificar 52% dos casos de Churn real, superando o Random Forest.



---

## 💡 Insights e Recomendações Estratégicas
Com base nos coeficientes do modelo e na importância das variáveis, recomendamos:

1. **Retenção Imediata:** Focar em clientes com menos de 1 ano de casa (baixo `tenure`).
2. **Revisão de Produto:** Investigar a qualidade do serviço de Fibra Óptica, que é o principal preditor positivo de evasão.
3. **Incentivo à Fidelidade:** Criar benefícios para migração de planos "mês a mês" para contratos anuais.
4. **Alerta Financeiro:** Clientes com mensalidades muito acima da média devem receber ofertas personalizadas de "downgrade preventivo" para evitar o cancelamento total.

---

## 👩‍💻 Autora
**Nicole Marcondes** Analista de Machine Learning Júnior  
*Projeto desenvolvido como desafio prático de análise de dados e modelagem preditiva.*

---