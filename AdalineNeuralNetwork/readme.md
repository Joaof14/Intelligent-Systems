# Detecção da Ionosfera Utilizando Rede Neural Adaline / Ionosphere Detection using Adaline Neural Network

📓 **[Abra o notebook aqui](./Ionosphere-Detection-adaline-neural-network.ipynb)**
The Jupyter notebook in this repository is bilingual (Portuguese/English). [Click here](./Ionosphere-Detection-adaline-neural-network.ipynb) to view the analysis.

## 📚 Contexto Teórico 


O monitoramento contínuo da ionosfera é crucial para a confiabilidade de sistemas de telecomunicações, navegação GPS e previsão de tempestades geomagnéticas. Radares de alta frequência (HF) emitem pulsos e analisam os sinais refletidos para verificar a existência de estruturas eletrônicas coerentes na ionosfera. O Brasil ocupa uma posição estratégica e desafiadora, situado sobre a Anomalia de Ionização Equatorial, onde a ionosfera apresenta irregularidades intensas e fenômenos como bolhas de plasma — fatores que afetam diretamente o desempenho de sinais de comunicação e posicionamento.

A **Rede Neural Adaline (Adaptive Linear Neuron)** é um modelo clássico de aprendizado supervisionado que utiliza a regra Delta para ajustar iterativamente seus pesos. Ao contrário do perceptron, a Adaline minimiza o erro quadrático médio (MSE), tornando-a mais adequada para problemas com relações aproximadamente lineares entre preditores e target.


## 🎯 Objetivo 

Construir uma rede Adaline para classificar automaticamente os retornos de radar ionosférico em "good" (estrutura ionosférica detectada, +1) ou "bad" (ausência de estrutura coerente, −1), utilizando 34 atributos contínuos derivados de autocorrelação de pulsos. O projeto demonstra as etapas completas de modelagem: exploração de dados, validação de premissas, seleção de atributos, normalização, ajuste do modelo, e avaliação de desempenho.


## 📊 Dataset 

O projeto utiliza o **UCI Ionosphere Dataset**, contendo:
- **351 retornos de radar** coletados via antenas de alta frequência
- **34 atributos contínuos** derivados de autocorrelação de pulsos
- **Classificação binária**: "g" (good) e "b" (bad), convertidas para bipolar (+1, −1)
- **Classes**: 225 amostras good, 126 amostras bad (desbalanceamento moderado)

**Fonte:** [UCI Machine Learning Repository: Ionosphere Dataset](https://archive.ics.uci.edu/dataset/52/ionosphere)

## 📁 Estrutura do Projeto 

```
AdalineNeuralNetwork/
├── Ionosphere-Detection-adaline-neural-network.ipynb   # Notebook principal
├── README.md                                            # Instruções

```

## 🔍 O que o Notebook Contém 

1. **Etapa 1 – Exploração e Verificação de Qualidade** — Carregamento do dataset UCI, inspeção estrutural, recodificação do target para bipolar, verificação de valores ausentes/constantes, análise univariada (histogramas, boxplots) e análise multivariada (matriz de correlação, correlação preditor–target, boxplots por classe).

2. **Etapa 2 – Validação de Premissas do Modelo** — Verificação da linearidade via regressão Ridge, análise de multicolinearidade entre preditores, validação do balanceamento de classes, e avaliação da qualidade da relação preditor–target.

3. **Etapa 3 – Seleção de Atributos** — Remoção de features constantes identificadas na Etapa 1, ranking de features por correlação absoluta com o target, e documentação do conjunto final de preditores.

4. **Etapa 4 – Divisão dos Dados** — Split estratificado 80% treino / 20% teste com `train_test_split`, preservação da proporção das classes em ambos os subconjuntos.

5. **Etapa 5 – Normalização/Padronização** — Aplicação de Z-score StandardScaler ajustado apenas no treino, justificativa algébrica (equalização de variância para convergência estável da regra Delta).

6. **Etapa 6 – Ajuste do Modelo (Adaline)** — Implementação via `SGDClassifier` com `loss='squared_error'`, testes de múltiplas taxas de aprendizagem (η = 10⁻⁴, 10⁻³, 10⁻², 5×10⁻², 10⁻¹), 5-fold Stratified CV, plotagem de curvas de convergência (MSE vs épocas), e seleção do melhor η.

7. **Etapa 7 – Avaliação** — Classificação do conjunto de teste com o melhor modelo, cálculo da matriz de confusão, acurácia, precisão, recall, F1-score, análise de erros críticos (False Positives vs False Negatives no contexto ionosférico).

8. **Etapa 8 – Relatório Final**.

## 🚀 Como Executar 

### 1. Instale as Dependências 

```bash
# A partir da raiz do repositório / From the repository root
pip install -r requirements.txt
```

### 2. Inicie o Jupyter 

```bash
jupyter lab
# ou / or
jupyter notebook
```

### 3. Abra e Execute o Notebook 

Navegue para `AdalineNeuralNetwork/Ionosphere-Detection-adaline-neural-network.ipynb` e execute as células sequencialmente.

Navigate to `AdalineNeuralNetwork/Ionosphere-Detection-adaline-neural-network.ipynb` and run the cells sequentially.

## 📦 Requisitos 

- Python 3.8+
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- ucimlrepo (para carregamento automático do dataset)

## 💡 Dicas e Boas Práticas 

- O dataset é carregado **automaticamente** via `ucimlrepo` — nenhum download manual necessário.
- Use `random_state=42` em todas as operações estocásticas para garantir reprodutibilidade.
- A **normalização Z-score é obrigatória**: sem ela, a superfície de erro fica alongada, exigindo η muito pequeno e convergência lenta.
- Teste **múltiplos valores de η** e inspecione as **curvas de convergência**: a escolha afeta significativamente a estabilidade do treinamento.
- Utilize **Stratified K-Fold** para validação cruzada quando há desbalanceamento de classes (mesmo que moderado).
- Inspecione a **matriz de correlação** para detectar multicolinearidade; se houver pares com |r| > 0.9, considere regularização (Ridge/Lasso).
- Considere o **contexto aplicado**: para monitoramento ionosférico, False Positives podem ser mais críticos que False Negatives — adapte a métrica de desempenho conforme necessário.

## 📚 Referências 

- [UCI Machine Learning Repository: Ionosphere Dataset](https://archive.ics.uci.edu/dataset/52/ionosphere)
- [scikit-learn SGDClassifier Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.SGDClassifier.html)
- [Adaline Neural Networks Theory](https://en.wikipedia.org/wiki/ADALINE)
- Widrow, B., & Hoff, M. E. (1960). Adaptive switching circuits. *IRE WESCON Convention Record*, 4, 96–104.

## 🎓 Próximos Passos 

- Comparar a Adaline com outros classificadores lineares (Logistic Regression, SVM) e não-lineares (MLP, Random Forest).
- Implementar **regularização L1/L2** (Ridge, Lasso) para melhorar generalização e reduzir False Positives.
- Explorar **feature engineering**: criar interações, polinômios ou transformações não-lineares.
- Aplicar **técnicas de balanceamento** (SMOTE, class_weight='balanced') para reduzir viés em classes desbalanceadas.
- Implementar um **pipeline scikit-learn** completo e salvar o modelo com `joblib`.
- Testar **métodos de validação alternativa**: Leave-One-Out CV, Time Series CV (se dados tiverem ordem temporal).
- Desenvolver um **script de treinamento** (`train.py`) para reproduzir o fluxo de forma automatizada e escalável.
- Investigar **explainability**: plotar os pesos aprendidos e correlacioná-los com as features para interpretação do modelo.

---

**Disciplina:** Sistemas Inteligentes — 2026  
**Autores:** [João Pedro Fernandes de Aquino](https://github.com/Joaof14) & [Anderson Carlos da Silva Morais](https://github.com/AndersonCSM)