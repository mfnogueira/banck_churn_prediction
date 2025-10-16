# Bank Customer Churn Prediction

Projeto de análise e predição de churn (evasão) de clientes bancários utilizando técnicas de Machine Learning.

## 📋 Descrição

Este projeto realiza uma análise exploratória completa de dados bancários e implementa modelos de Machine Learning para prever a probabilidade de um cliente deixar o banco. O objetivo é identificar padrões que possam indicar a evasão de clientes, permitindo ações preventivas.

## 🎯 Objetivo

Desenvolver modelos preditivos capazes de identificar clientes com alta probabilidade de churn, auxiliando o banco na retenção de clientes através de estratégias direcionadas.

## 📊 Dataset

O dataset contém informações de clientes bancários, incluindo:

- **Dados Demográficos**: Idade, Geografia, Gênero
- **Dados Financeiros**: Score de Crédito, Saldo, Salário Estimado
- **Dados Comportamentais**: Posse de Cartão de Crédito, Membro Ativo, Número de Produtos
- **Target**: Churned (Cliente saiu ou permaneceu no banco)

## 🔧 Tecnologias Utilizadas

- **Python 3.x**
- **Pandas & NumPy**: Manipulação e análise de dados
- **Matplotlib & Seaborn**: Visualização de dados
- **Scikit-learn**: Modelos de Machine Learning
- **XGBoost, LightGBM, CatBoost**: Algoritmos de Gradient Boosting
- **SMOTE**: Balanceamento de classes
- **SciPy**: Análises estatísticas

## 📦 Instalação

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost lightgbm scipy catboost imbalanced-learn openpyxl
```

## 🚀 Como Usar

1. Clone o repositório:
```bash
git clone https://github.com/mfnogueira/banck_churn_prediction.git
cd banck_churn_prediction
```

2. Instale as dependências:
```bash
pip install -qU pandas numpy matplotlib seaborn scikit-learn xgboost lightgbm scipy catboost imbalanced-learn openpyxl
```


## 🔍 Análise Exploratória

O projeto inclui uma análise exploratória detalhada:

### Limpeza de Dados
- Renomeação de colunas para melhor legibilidade
- Remoção de features irrelevantes (RowNumber, CustomerId, Surname)
- Verificação de valores nulos e duplicados

### Visualizações
- Distribuição de produtos por cliente
- Análise geográfica dos clientes
- Distribuição por posse de cartão de crédito
- Status de membro ativo
- Distribuição de gênero
- **KDE (Kernel Density Estimation)** para Age e Balance

### Insights Principais
- **Correlação Positiva (0.3)**: Entre Idade e Churn
- **Correlação Negativa (-0.3)**: Entre Saldo e Número de Produtos
- **Distribuição de Saldo**: Bimodal com picos em ~0 e ~120.000
- **Distribuição de Idade**: Assimetria positiva com pico aos 40 anos

## 🧠 Feature Engineering

Criação de novas features categóricas:

- **Age Group**: Young Adults, Middle-Aged Adults, Senior Adults
- **Balance Category**: Empty account, Funded account, Overdrawn account
- **Is Active Member**: Active account, Dormant account
- **Has Credit Card**: Has a card, No card
- **Credit Score Category**: Poor, Fair, Good, Very Good, Exceptional
- **Estimated Salary Category**: Low, Medium, High, Very High
- **BalanceSalaryRatio**: Proporção entre saldo e salário

## 🤖 Modelos de Machine Learning

O projeto implementa múltiplos algoritmos:

- K-Nearest Neighbors (KNN)
- Logistic Regression
- Support Vector Machine (SVM)
- Decision Tree
- Random Forest
- Naive Bayes
- XGBoost
- LightGBM
- CatBoost

### Técnicas de Balanceamento
- **SMOTE**: Synthetic Minority Over-sampling Technique para lidar com desbalanceamento de classes

## 📈 Avaliação

Os modelos são avaliados utilizando:
- Classification Report (Precision, Recall, F1-Score)
- Confusion Matrix
- Métricas de performance

## 📁 Estrutura do Projeto

```
bankChurn_prediction/
├── bank customer churn dataset.csv
├── analysis/
│   └── bank customer churn new dataset.xlsx
├── .gitignore
└── README.md
```

## 📊 Outputs

O projeto gera:
- Dataset processado com novas features (`analysis/bank customer churn new dataset.xlsx`)
- Visualizações exploratórias
- Modelos treinados (pickle files)
- Relatórios de classificação

## 🤝 Contribuindo

Contribuições são bem-vindas! Sinta-se à vontade para:

1. Fazer um Fork do projeto
2. Criar uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abrir um Pull Request

## 📝 Licença

Este projeto está sob licença aberta para fins educacionais.

## 👤 Autor

**mfnogueira**

- GitHub: [@mfnogueira](https://github.com/mfnogueira)
- Repositório: [banck_churn_prediction](https://github.com/mfnogueira/banck_churn_prediction.git)

## 🙏 Agradecimentos

- Dataset de Customer Churn
- Comunidade de Data Science e Machine Learning

---

Desenvolvido com foco em aprendizado e aplicação prática de técnicas de Machine Learning para problemas de negócio.
