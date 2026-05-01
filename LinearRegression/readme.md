# ⚡ Previsão de Potência em Usinas de Ciclo Combinado com Regressão Linear

## 📚 Contexto Teórico

**Regressão Linear** é um modelo fundamental de aprendizado supervisionado que estabelece uma relação linear entre variáveis independentes e uma variável alvo contínua. É amplamente utilizado em engenharia, economia e ciências naturais pela sua simplicidade, interpretabilidade e eficiência computacional.

Usinas de ciclo combinado (UTCC) integram dois ciclos termodinâmicos distintos:
- **Ciclo Brayton** (turbina a gás)
- **Ciclo Rankine** (turbina a vapor)

Nessa configuração a potência de saída é altamente sensível às condições ambientais, tornando a previsão uma meta a ser alcançada.

## 🎯 Objetivo

Desenvolver um modelo de **Regressão Linear** para prever a potência elétrica gerada por uma usina de ciclo combinado com base em variáveis ambientais reais, demonstrando aplicação prática de ML em engenharia energética.

📓 **[Abra o notebook aqui](./Power_Plant_Linear_Regression.ipynb)**

## 📊 Dataset

O projeto utiliza o **UCI CCPP Dataset**, coletado ao longo de 6 anos:
- **9.568 amostras** de plantas em operação real
- **4 variáveis ambientais** de entrada
- **1 variável alvo** (potência elétrica)

**Variáveis:**
- **AT** (Ambient Temperature) — Temperatura em °C
- **V** (Exhaust Vacuum) — Vácuo de escape em cm Hg
- **AP** (Ambient Pressure) — Pressão atmosférica em mbar
- **RH** (Relative Humidity) — Umidade relativa em %
- **PE** (Power Output) — Potência elétrica em MW ⭐ **(alvo)**

## 📁 Estrutura do Projeto

```
LinearRegression/
├── Power_Plant_Linear_Regression.ipynb   # Notebook principal
├── readme.md
└── requirements.txt
```

## 🔍 O que o Notebook Contém

1. **Análise Exploratória (EDA)** — Distribuições, correlações e estatísticas
2. **Pré-processamento** — Normalização e preparação de dados
3. **Divisão Treino/Teste** — Estratégia apropriada para regressão
4. **Treinamento do Modelo** — Regressão Linear com scikit-learn
5. **Avaliação** — R², MAE, RMSE e visualizações de desempenho
6. **Interpretação** — Análise dos coeficientes e impacto de variáveis

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

Navegue para `LinearRegression/Power_Plant_Linear_Regression.ipynb` e execute as células sequencialmente.

## 📦 Requisitos

- Python 3.8+
- pandas
- numpy
- matplotlib
- scikit-learn

## 💡 Resultados Esperados

- Identificar quais variáveis ambientais mais afetam a potência
- Avaliar qualidade da previsão linear em contexto energético real
- Comparar performance com modelos não-lineares em trabalhos futuros

## 📚 Referências

- [UCI Machine Learning Repository: Combined Cycle Power Plant](https://archive.ics.uci.edu/dataset/294/combined+cycle+power+plant)
- [scikit-learn Linear Regression](https://scikit-learn.org/stable/modules/linear_model.html#ordinary-least-squares)
- [Pinar Tüfekci, 2014 — Prediction of full load electrical power of a base load operated combined cycle power plant](https://www.sciencedirect.com/science/article/abs/pii/S0142061513002111)

## 🎓 Próximos Passos

- Testar modelos não-lineares (Random Forest, Gradient Boosting)
- Implementar validação cruzada para estimativas mais robustas
- Criar pipeline completo com pré-processamento automatizado
- Salvar modelo treinado com `joblib` para uso em produção
- Explorar feature engineering para melhorar desempenho

---

**Disciplina:** Sistemas Inteligentes — 2026
