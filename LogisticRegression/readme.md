# Prática: Regressão Logística — Diagnóstico de Doenças Cardíacas

## Introdução

Doenças cardiovasculares são a principal causa de morte no mundo, responsáveis por cerca de 18 milhões de óbitos por ano segundo a OMS. O diagnóstico precoce é determinante para o sucesso do tratamento. Existe, portanto, uma necessidade real de ferramentas capazes de estimar o risco de um paciente com base em dados clínicos simples, coletados em consulta de rotina. É nesse contexto que o aprendizado de máquina pode contribuir. Um modelo de classificação treinado com dados históricos de pacientes diagnosticados é capaz de aprender quais combinações de variáveis clínicas estão associadas à presença de doença cardíaca e aplicar esse aprendizado a novos pacientes.

## Objetivo

Construir um modelo de regressão logística para prever a presença de doença cardíaca utilizando dados clínicos.

## Conjunto de Dados

O projeto utiliza o dataset Heart Disease Cleveland (UCI Machine Learning Repository – disponível em https://archive.ics.uci.edu/dataset/45/heart+disease), com registros de 303 pacientes e 13 variáveis clínicas. Os diagnósticos foram confirmados por cateterismo cardíaco, o que garante rótulos confiáveis. As variáveis incluem:

- **age** — idade do paciente em anos;
- **sex** — sexo biológico (1 = masculino, 0 = feminino);
- **cp** — tipo de dor no peito: angina típica (1), atípica (2), não anginosa (3) ou assintomático (4);
- **trestbps** — pressão arterial em repouso em mmHg;
- **chol** — colesterol sérico total em mg/dl;
- **fbs** — glicemia em jejum acima de 120 mg/dl (1 = sim, 0 = não);
- **restecg** — resultado do ECG em repouso: normal (0), alteração na onda ST-T (1) ou hipertrofia ventricular (2);
- **thalach** — frequência cardíaca máxima atingida no teste de esforço;
- **exang** — angina induzida por exercício (1 = sim, 0 = não);
- **oldpeak** — depressão do segmento ST durante o esforço, indicador de isquemia;
- **slope** — inclinação do segmento ST no pico do esforço: ascendente (1), plano (2) ou descendente (3);
- **ca** — número de artérias coronárias com obstrução visível na fluoroscopia (0 a 3);
- **thal** — cintilografia de tálio: normal (3), defeito fixo / infarto prévio (6) ou defeito reversível / isquemia ativa (7);

A saída é a variável target, que indica o diagnóstico original de 0 a 4, binarizado para 0 (sem doença) e 1 (com doença) antes do treinamento.

## Descrição

O notebook `Heart-Disease_Logistic_Regression.ipynb` contém todo o passo a passo, desde a análise exploratória até a avaliação do modelo.

## Como executar

1. Abra o notebook `Heart-Disease_Logistic_Regression.ipynb` no Jupyter Notebook ou Jupyter Lab.
2. Execute as células sequencialmente, seguindo as instruções e comentários.
3. Analise os resultados e gráficos gerados ao final.

## Requisitos

- Python 3.x
- Jupyter Notebook
- Bibliotecas: pandas, numpy, matplotlib, scikit-learn

Para instalar as dependências, execute:

```bash
pip install pandas numpy matplotlib scikit-learn
```

## Referências

- [UCI Machine Learning Repository: Heart Disease Dataset](https://archive.ics.uci.edu/dataset/45/heart+disease)

---

Disciplina: Sistemas Inteligentes — 2026

# Practice: Logistic Regression — Heart Disease Diagnosis

## Introduction

Cardiovascular diseases are the leading cause of death worldwide, responsible for about 18 million deaths per year according to the WHO. Early diagnosis is crucial for successful treatment. Therefore, there is a real need for tools capable of estimating a patient's risk based on simple clinical data collected during routine consultations. It is in this context that machine learning can contribute. A classification model trained with historical data from diagnosed patients is able to learn which combinations of clinical variables are associated with the presence of heart disease and apply this learning to new patients.

## Objective

Build a logistic regression model to predict the presence of heart disease using clinical data.

## Dataset

The project uses the Heart Disease Cleveland dataset (UCI Machine Learning Repository – available at https://archive.ics.uci.edu/dataset/45/heart+disease), with records from 303 patients and 13 clinical variables. The diagnoses were confirmed by cardiac catheterization, which ensures reliable labels. The variables include:

- **age** — patient's age in years;
- **sex** — biological sex (1 = male, 0 = female);
- **cp** — type of chest pain: typical angina (1), atypical (2), non-anginal (3) or asymptomatic (4);
- **trestbps** — resting blood pressure in mmHg;
- **chol** — serum cholesterol total in mg/dl;
- **fbs** — fasting blood sugar > 120 mg/dl (1 = yes, 0 = no);
- **restecg** — resting ECG result: normal (0), ST-T wave abnormality (1) or left ventricular hypertrophy (2);
- **thalach** — maximum heart rate achieved during exercise test;
- **exang** — exercise-induced angina (1 = yes, 0 = no);
- **oldpeak** — ST segment depression during exercise, indicator of ischemia;
- **slope** — slope of the ST segment at peak exercise: upsloping (1), flat (2) or downsloping (3);
- **ca** — number of major vessels colored by fluoroscopy (0-3);
- **thal** — thalassemia: normal (3), fixed defect / previous infarct (6) or reversible defect / active ischemia (7);

The output is the target variable, which indicates the original diagnosis from 0 to 4, binarized to 0 (no disease) and 1 (with disease) before training.

## Description

The notebook `Heart-Disease_Logistic_Regression.ipynb` contains the full workflow, from exploratory analysis to model evaluation.

## How to run

1. Open the notebook `Heart-Disease_Logistic_Regression.ipynb` in Jupyter Notebook or Jupyter Lab.
2. Run the cells sequentially, following the instructions and comments.
3. Analyze the results and generated plots at the end.

## Requirements

- Python 3.x
- Jupyter Notebook
- Libraries: pandas, numpy, matplotlib, scikit-learn

To install the dependencies, run:

```bash
pip install pandas numpy matplotlib scikit-learn
```

## References

- [UCI Machine Learning Repository: Heart Disease Dataset](https://archive.ics.uci.edu/dataset/45/heart+disease)

---

Intelligent Systems Course — 2026
