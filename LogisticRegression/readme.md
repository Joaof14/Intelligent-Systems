# ❤️ Diagnóstico de Doenças Cardíacas com Regressão Logística

## 📚 Contexto Teórico

**Regressão Logística** é um modelo de classificação que estima a probabilidade de um evento binário ocorrer. Apesar do nome, é um classificador e não um regressor, amplamente usado em medicina, biologia e ciências sociais. Sua força está na interpretabilidade probabilística e na capacidade de lidar com dados desbalanceados.

Doenças cardiovasculares são a **principal causa de morte no mundo** — cerca de 18 milhões de óbitos anuais (OMS). O diagnóstico precoce é essencial para o sucesso do tratamento. ML pode estimar o risco cardíaco usando dados clínicos simples, coletáveis em consulta de rotina — democratizando acesso a ferramentas de diagnóstico auxiliar.

## 🎯 Objetivo

Desenvolver um modelo de **Regressão Logística** para diagnosticar a presença de doenças cardíacas com base em dados clínicos, ilustrando aplicação prática de ML em medicina preventiva.

📓 **[Abra o notebook aqui](./Heart-Disease_Logistic_Regression.ipynb)**

## 📊 Dataset

O projeto utiliza o **UCI Heart Disease Cleveland Dataset**:
- **303 pacientes** com diagnósticos confirmados por cateterismo cardíaco
- **13 variáveis clínicas** diversas
- **Classificação binária** (com/sem doença)

**Variáveis Clínicas:**
- **age** — Idade em anos
- **sex** — Sexo biológico (1=masculino, 0=feminino)
- **cp** — Tipo de dor no peito (1-4: típica a assintomática)
- **trestbps** — Pressão arterial em repouso (mmHg)
- **chol** — Colesterol sérico total (mg/dl)
- **fbs** — Glicemia em jejum > 120 mg/dl (1=sim, 0=não)
- **restecg** — Resultado do ECG em repouso (0-2)
- **thalach** — Frequência cardíaca máxima no teste de esforço
- **exang** — Angina induzida por exercício (1=sim, 0=não)
- **oldpeak** — Depressão do segmento ST (indicador de isquemia)
- **slope** — Inclinação do ST (1-3: ascendente a descendente)
- **ca** — Artérias coronárias obstruídas (0-3)
- **thal** — Cintilografia de tálio (3=normal, 6=infarto, 7=isquemia)

**Alvo:** Presença de doença cardíaca (0=não, 1=sim)

## 📁 Estrutura do Projeto

```
LogisticRegression/
├── Heart-Disease_Logistic_Regression.ipynb   # Notebook principal
├── readme.md
└── requirements.txt
```

## 🔍 O que o Notebook Contém

1. **Carregamento e Limpeza** — Tratamento de dados clínicos reais
2. **Análise Exploratória (EDA)** — Distribuições de variáveis por diagnóstico
3. **Pré-processamento** — Normalização, encoding e tratamento de desbalanceamento
4. **Divisão Treino/Teste** — Estratégia com stratificação
5. **Treinamento da Regressão Logística** — Com validação cruzada
6. **Avaliação** — Acurácia, precisão, recall, F1-score, ROC-AUC
7. **Matriz de Confusão** — Análise de falsos positivos/negativos
8. **Curva ROC** — Visualização de trade-offs sensibilidade/especificidade

## 🚀 Como Executar

### 1. Instale as Dependências

```bash
# A partir da raiz do repositório
pip install -r requirements.txt
```

### 2. Inicie o Jupyter

```bash
jupyter lab
# ou
jupyter notebook
```

### 3. Abra e Execute o Notebook

Navegue para `LogisticRegression/Heart-Disease_Logistic_Regression.ipynb` e execute as células sequencialmente.

## 📦 Requisitos

- Python 3.8+
- pandas
- numpy
- matplotlib
- scikit-learn
- seaborn (opcional, para visualizações avançadas)

## 💡 Métricas Importantes em Medicina

Para problemas clínicos, é crítico considerar:
- **Sensibilidade (Recall)** — Evitar falsos negativos (não perder casos)
- **Especificidade** — Evitar alarmes falsos
- **ROC-AUC** — Desempenho geral balanceado

Este notebook enfatiza essas métricas.

## 📚 Referências

- [UCI Machine Learning Repository: Heart Disease Dataset](https://archive.ics.uci.edu/dataset/45/heart+disease)
- [scikit-learn Logistic Regression](https://scikit-learn.org/stable/modules/linear_model.html#logistic-regression)

## 🎓 Próximos Passos

- Explorar dados desbalanceados com técnicas como SMOTE
- Comparar com outros classificadores (Random Forest, SVM, Neural Networks)
- Implementar interpretabilidade com SHAP ou LIME
- Criar API de predição com Flask/FastAPI para uso clínico
- Validar com dados de novos hospitais (generalização)

---

**Disciplina:** Sistemas Inteligentes — 2026
