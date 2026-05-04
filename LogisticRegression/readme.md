# Diagnóstico de Doenças Cardíacas com Regressão Logística

📓 **[Abra o notebook aqui]([./Heart-Disease_Logistic-Regression.ipynb])**
The Jupyter notebook in this repository is bilingual (Portuguese/English).[Click here]([./https://github.com/Joaof14/Intelligent-Systems/blob/main/LogisticRegression/Heart-Disease_Logistic-Regression.ipynb]) to view the analysis.

## 📚 Contexto Teórico

Doenças cardiovasculares são a principal causa de morte no mundo, responsáveis por cerca de 18 milhões de óbitos por ano segundo a OMS. O diagnóstico precoce é determinante para o sucesso do tratamento. Existe, portanto, uma necessidade real de ferramentas capazes de estimar o risco de um paciente com base em dados clínicos simples, coletados em consulta de rotina. É nesse contexto que o aprendizado de máquina pode contribuir. Um modelo de classificação treinado com dados históricos de pacientes diagnosticados é capaz de aprender quais combinações de variáveis clínicas estão associadas à presença de doença cardíaca e aplicar esse aprendizado a novos pacientes.

A **Regressão Logística**, que utilizamos aqui, é um modelo de classificação que estima a probabilidade de um evento binário ocorrer, sendo um classificador amplamente usado em medicina, biologia e ciências sociais.

## 🎯 Objetivo

Construir um modelo de **Regressão Logística** para prever a presença de doença cardíaca utilizando dados clínicos, demonstrando análise exploratória, pré-processamento, treinamento e avaliação com métricas adequadas ao contexto médico.

## 📊 Dataset

O projeto utiliza o **Heart Disease Cleveland Dataset** (UCI Machine Learning Repository), com registros de **303 pacientes** e **13 variáveis clínicas**. Os diagnósticos foram confirmados por cateterismo cardíaco, o que garante rótulos confiáveis.

**Variáveis:**
- **age** — idade do paciente em anos
- **sex** — sexo biológico (1 = masculino, 0 = feminino)
- **cp** — tipo de dor no peito: angina típica (1), atípica (2), não anginosa (3) ou assintomático (4)
- **trestbps** — pressão arterial em repouso em mmHg
- **chol** — colesterol sérico total em mg/dl
- **fbs** — glicemia em jejum acima de 120 mg/dl (1 = sim, 0 = não)
- **restecg** — resultado do ECG em repouso: normal (0), alteração na onda ST-T (1) ou hipertrofia ventricular (2)
- **thalach** — frequência cardíaca máxima atingida no teste de esforço
- **exang** — angina induzida por exercício (1 = sim, 0 = não)
- **oldpeak** — depressão do segmento ST durante o esforço, indicador de isquemia
- **slope** — inclinação do segmento ST no pico do esforço: ascendente (1), plano (2) ou descendente (3)
- **ca** — número de artérias coronárias com obstrução visível na fluoroscopia (0 a 3)
- **thal** — cintilografia de tálio: normal (3), defeito fixo / infarto prévio (6) ou defeito reversível / isquemia ativa (7)

A saída é a variável **target**, que indica o diagnóstico original de 0 a 4, binarizado para **0 (sem doença)** e **1 (com doença)** antes do treinamento.

## 📁 Estrutura do Projeto

```
LogisticRegression/
├── Heart-Disease_Logistic_Regression.ipynb   # Notebook principal
├── README.md                                 # Instruções
```

## 🔍 O que o Notebook Contém

1. **Carregamento e Limpeza** — Leitura do dataset e tratamento de dados
2. **Análise Exploratória (EDA)** — Estatísticas, distribuições e correlações
3. **Pré-processamento** — Binarização do target, normalização e divisão treino/teste
4. **Treinamento do Modelo** — Regressão Logística com scikit-learn
5. **Avaliação** — Acurácia, matriz de confusão, relatório de classificação, ROC-AUC
6. **Visualizações** — Curva ROC, matriz de confusão e análise de métricas

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
