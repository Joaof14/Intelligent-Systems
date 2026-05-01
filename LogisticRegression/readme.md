# ❤️ Diagnóstico de Doenças Cardíacas com Regressão Logística

## 📚 Contexto Teórico

**Regressão Logística** é um modelo de classificação que estima a probabilidade de um evento binário ocorrer. Apesar do nome, é um classificador e não um regressor, amplamente usado em medicina, biologia e ciências sociais. Sua força está na interpretabilidade probabilística e na capacidade de lidar com dados desbalanceados.

Doenças cardiovasculares são a principal causa de morte no mundo, responsáveis por cerca de 18 milhões de óbitos por ano segundo a OMS. O diagnóstico precoce é determinante para o sucesso do tratamento. Existe, portanto, uma necessidade real de ferramentas capazes de estimar o risco de um paciente com base em dados clínicos simples, coletados em consulta de rotina. É nesse contexto que o aprendizado de máquina pode contribuir. Um modelo de classificação treinado com dados históricos de pacientes diagnosticados é capaz de aprender quais combinações de variáveis clínicas estão associadas à presença de doença cardíaca e aplicar esse aprendizado a novos pacientes.

## Objetivo

Construir um modelo de regressão logística para prever a presença de doença cardíaca utilizando dados clínicos.

## Descrição

O notebook `Heart-Disease_Logistic_Regression.ipynb` contém todo o passo a passo, desde a análise exploratória até a avaliação do modelo.

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
