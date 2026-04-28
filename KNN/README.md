# KNN — Classificação de Qualidade de Vinho

Este diretório contém um notebook que usa o algoritmo k-Nearest Neighbors (k-NN) para classificar a qualidade do vinho com base em características físico-químicas.

Conteúdo
- `wine_classification_using_knn.ipynb`: Notebook Jupyter com preparação dos dados, análise exploratória, treino do modelo k-NN, validação e visualizações.
- `data/`: CSVs usados no notebook:
  - `p03_winequality-red.csv`
  - `p03_winequality-white.csv`

Pré-requisitos
- Python 3.8+ (recomendado)
- Instale as dependências listadas no `requirements.txt` do repositório raiz:

```bash
pip install -r requirements.txt
```

Como usar
1. Abra um terminal na raiz do repositório.
2. Instale as dependências (veja acima).
3. Inicie o Jupyter Notebook / Lab:

```bash
jupyter lab
# ou
jupyter notebook
```

4. Abra `KNN/wine_classification_using_knn.ipynb` no navegador.
5. Execute as células na ordem. O notebook está organizado nas seguintes seções:
   - Carregamento e mesclagem dos datasets (branco e vermelho);
   - Limpeza e tratamento de features;
   - Análise exploratória (estatísticas, histogramas, correlações);
   - Pré-processamento (normalização/scale, encoding, split treino/teste);
   - Treino do k-NN com validação cruzada e busca por hiperparâmetros (k);
   - Avaliação (acurácia, matriz de confusão, relatório de classificação) e visualizações.

Notas e dicas
- Os CSVs já estão na pasta `data/`; não é necessário baixar datasets externos.
- Para reprodutibilidade, fixe `random_state` nas células que fazem split/aleatoriedade.
- Experimente normalizar as features antes de aplicar k-NN (ex.: `StandardScaler`).

Referências
- UCI Wine Quality Dataset — artigo e descrição das features.

Próximos passos sugeridos
- Comparar com outros classificadores (Logistic Regression, Random Forest).
- Implementar pipeline do scikit-learn e salvar o modelo com `joblib`.
- Adicionar um script `train.py` que reproduza o fluxo do notebook para execução automatizada.

Se quiser, eu posso abrir o notebook para você, gerar um script Python equivalente, ou rodar as células localmente (se você autorizar e o ambiente estiver pronto).
