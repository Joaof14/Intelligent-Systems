# Classificação de Qualidade de Vinho com k-NN

📓 **[Abra o notebook aqui](./wine_classification_using_knn.ipynb)**
The Jupyter notebook in this repository is bilingual (Portuguese/English).[Click here](./wine_classification_using_knn.ipynb) to view the analysis.

## 📚 Contexto Teórico

A classificação de qualidade de vinho é um desafio crítico na indústria vinífera, envolvendo análise complexa de múltiplas propriedades físico-químicas para determinar a qualidade do produto. Processos manuais de avaliação são caros, subjetivos e demorados. Existe, portanto, uma necessidade real de ferramentas automáticas capazes de classificar vinhos com precisão com base em dados laboratoriais. É nesse contexto que o aprendizado de máquina pode contribuir, desenvolvendo modelos que aprendem padrões nas características químicas para prever a qualidade de forma rápida e consistente.

O **k-Nearest Neighbors (k-NN)**, que aqui utilizamos, é um algoritmo de classificação não-paramétrico que prediz a classe de novos dados observando os k vizinhos mais próximos no espaço de features, sendo particularmente eficaz para capturar padrões complexos e não-lineares.

## 🎯 Objetivo

Implementar o algoritmo **k-NN** para classificar a qualidade de vinhos com base em suas características físico-químicas, demonstrando análise exploratória de dados, pré-processamento, validação cruzada e otimização de hiperparâmetros.

## 📊 Dataset

O projeto utiliza o **UCI Wine Quality Dataset**, contendo:
- **9 variáveis físico-químicas** (acidez, álcool, sulfatos, pH, etc.)
- **Vinhos tinto e branco** em arquivos separados
- **Classificação de qualidade** como alvo (0–10)

**Arquivos de dados:**
- `data/p03_winequality-red.csv` — 1.599 amostras de vinho tinto
- `data/p03_winequality-white.csv` — 4.898 amostras de vinho branco

## 📁 Estrutura do Projeto

```
KNN/
├── wine_classification_using_knn.ipynb    # Notebook principal
├── README.md                              # Instruções
└── data/
    ├── p03_winequality-red.csv
    └── p03_winequality-white.csv
```

## 🔍 O que o Notebook Contém

1. **Carregamento e Limpeza** — Integração dos datasets de vinho tinto e branco
2. **Análise Exploratória (EDA)** — Estatísticas, distribuições e correlações
3. **Pré-processamento** — Normalização, encoding e divisão treino/teste
4. **Treinamento do k-NN** — Validação cruzada e busca por hiperparâmetro k
5. **Avaliação** — Acurácia, matriz de confusão, relatório de classificação
6. **Visualizações** — Gráficos exploratórios e resultados do modelo

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

Navegue para `KNN/wine_classification_using_knn.ipynb` e execute as células sequencialmente.

## 📦 Requisitos

- Python 3.8+
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn (opcional, para visualizações avançadas)

## 💡 Dicas e Boas Práticas

- Os CSVs já estão incluídos na pasta `data/` — nenhum download externo necessário.
- Use `random_state` para garantir reprodutibilidade.
- Experimente normalizar as features com `StandardScaler` antes de aplicar k-NN.
- Teste diferentes valores de k para encontrar o melhor desempenho.

## 📚 Referências

- [UCI Machine Learning Repository: Wine Quality Dataset](https://archive.ics.uci.edu/dataset/109/wine+quality)
- [scikit-learn k-NN Documentation](https://scikit-learn.org/stable/modules/neighbors.html)

## 🎓 Próximos Passos

- Comparar k-NN com outros classificadores (Logistic Regression, Random Forest)
- Implementar pipeline do scikit-learn e salvar o modelo com `joblib`
- Criar um script `train.py` para reproduzir o fluxo de forma automatizada
- Testar outros métodos de validação (leave-one-out, stratified k-fold)

---

**Disciplina:** Sistemas Inteligentes — 2026