# Sistema de Detecção de Intrusão com MLP

📓 **[Abra o notebook aqui](./Intrusion_detection_system_using_MLP.ipynb)**  

## 📚 Contexto Teórico

A segurança de redes de computadores é um dos desafios centrais da infraestrutura digital moderna. Ataques como negação de serviço (DoS), varredura de portas (Probe) e acesso remoto não autorizado (R2L) causam prejuízos bilionários anualmente e comprometem desde sistemas corporativos até infraestruturas críticas.

Os **Sistemas de Detecção de Intrusão (IDS)** são a principal linha de defesa ativa contra essas ameaças. Neste projeto, utilizamos uma **Rede Neural Multilayer Perceptron (MLP)**, que, com suas camadas ocultas e funções de ativação não lineares, é capaz de aprender fronteiras de decisão complexas e distinguir tráfego normal de ataques com alta precisão.

## 🎯 Objetivo

Desenvolver um modelo de **Rede Neural MLP** para classificar tráfego de rede como **normal** ou **ataque**, utilizando o conjunto de dados NSL‑KDD, demonstrando todas as etapas de um projeto de ciência de dados: exploração, pré-processamento, análise exploratória, treinamento e avaliação.

## 📊 Dataset

O projeto utiliza o **NSL‑KDD Dataset**, uma versão melhorada do KDD Cup 1999, amplamente utilizado como referência para sistemas de detecção de intrusão.

- **Arquivos utilizados:**
  - `KDDTrain+.txt` — 125.973 amostras para treino
  - `KDDTest+.txt` — 22.544 amostras para teste
- **Total de atributos:** 41 características e 1 rótulo (`attack_type`)
- **Tipos de ataque:** DoS, Probe, R2L, U2R, além do tráfego normal
- **Domínio:** Features contínuas, discretas e categóricas (protocolo, serviço, flag)

## 📁 Estrutura do Projeto

```
Intrusion_detection_MLP/
├── Intrusion_detection_system_using_MLP.ipynb   # Notebook principal
├── README.md                                    # Instruções
└── data/
    └── archive/                                 # Pasta com os datasets NSL‑KDD
        ├── KDDTrain+.txt
        └── KDDTest+.txt
```

## 🔍 O que o Notebook Contém

1. **Carregamento e inspeção dos dados** — Visualização das primeiras linhas, tipos de dados e estatísticas descritivas.
2. **Codificação one‑hot** — Conversão das variáveis categóricas (`protocol_type`, `service`, `flag`) para formato binário.
3. **Binarização do rótulo** — Transformação da coluna `attack_type` em 0 (normal) e 1 (ataque).
4. **Verificação da qualidade dos dados** — Análise de valores ausentes, atributos constantes e linhas duplicadas.
5. **Análise univariada** — Histogramas e boxplots para cada atributo numérico, identificação de outliers.
6. **Análise bivariada / multivariada** — Matriz de correlação de Pearson e pares com alta multicolinearidade.
7. **Pré‑processamento** — Normalização/padronização e divisão treino‑teste (embora os conjuntos já sejam separados).
8. **Construção do MLP** — Rede neural com camadas ocultas implementada em PyTorch.
9. **Treinamento e avaliação** — Acurácia, precisão, recall, F1‑score, matriz de confusão e relatório de classificação.

## 🚀 Como Executar

### 1. Instale as Dependências

```bash
pip install pandas numpy matplotlib seaborn scikit-learn torch
```

### 2. Inicie o Jupyter

```bash
jupyter lab
# ou
jupyter notebook
```

### 3. Abra e Execute o Notebook

Navegue até `Intrusion_detection_system_using_MLP.ipynb` e execute as células sequencialmente.

## 📦 Requisitos

- Python 3.8+
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- torch (PyTorch)

## 💡 Dicas e Boas Práticas

- Os arquivos de dados já estão na pasta `data/archive/` — nenhum download externo é necessário.
- A codificação one‑hot aumenta a dimensionalidade do conjunto (de 42 para 123 colunas). Certifique‑se de alinhar as colunas de treino e teste.
- A normalização (StandardScaler) é essencial para o bom desempenho da MLP.
- A análise de correlação revela pares com alta multicolinearidade (ex.: `num_compromised` e `num_root`). Em projetos mais avançados, essas features poderiam ser removidas ou combinadas.
- O notebook utiliza PyTorch para construir a rede. Ajuste o número de neurônios e camadas para melhorar os resultados.

## 📚 Referências

- [NSL‑KDD Dataset – University of New Brunswick](https://www.unb.ca/cic/datasets/nsl.html)
- [PyTorch Documentation](https://pytorch.org/docs/stable/index.html)
- [Scikit‑learn: Preprocessing](https://scikit-learn.org/stable/modules/preprocessing.html)

## 🎓 Próximos Passos

- Aplicar técnicas de seleção de atributos (ex.: eliminar features altamente correlacionadas) para reduzir a dimensionalidade e possível overfitting.
- Experimentar arquiteturas mais profundas ou diferentes funções de ativação.
- Implementar *early stopping* e *dropout* para regularização.
- Comparar o MLP com outros classificadores (Random Forest, XGBoost).
- Criar um script `train.py` para reproduzir o fluxo de forma automatizada.

---

**Disciplina:** Sistemas Inteligentes — 2026