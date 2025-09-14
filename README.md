# Tesla Stock Price Prediction - RNN/LSTM

Atividade ponderada de implementação de Rede Neural Recorrente para predição de preços de ações da Tesla.

## 📊 Dataset

**Fonte**: [Tesla Stock Price Dataset 2010-2024 (Kaggle)](https://www.kaggle.com/datasets/hussainnasirkhan/tesla-stock-price-dataset-2010-2024?resource=download)

### Colunas

- `Date`: Data da negociação
- `Close`: Preço de fechamento (target)
- `Open`, `High`, `Low`: Preços de abertura, máximo e mínimo
- `Volume`: Volume de negociações

## 🎯 Métrica Selecionada: RMSE

**Justificativa**: RMSE é ideal para regressão em séries financeiras pois penaliza erros grandes, mantém unidade monetária e é sensível a outliers.

## 🚀 Como Executar

### Google Colab (Recomendado)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/11h6HVsWCyhjsKl82oyr44rc2sWWxj6gS?usp=sharing)

### Local

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/tesla-stock-prediction-rnn

# Instale dependências
pip install pandas numpy matplotlib scikit-learn tensorflow

# Execute o notebook
jupyter notebook ponderada_rnn_mauro_das_chagas_junior.ipynb
```

## 📁 Estrutura do Projeto

```
├── ponderada_rnn_mauro_das_chagas_junior.ipynb  # Notebook principal
├── tesla_stock_price_14_years.csv               # Dataset
└── README.md                                    # Documentação
```

## 🧠 Arquitetura do Modelo

- **Input**: Sequências de 20 dias
- **LSTM 1**: 50 neurônios + Dropout (0.2)
- **LSTM 2**: 25 neurônios + Dropout (0.2)  
- **Output**: 1 neurônio (Dense)
- **Otimizador**: Adam (lr=0.001)
- **Loss**: MSE

## ⚙️ Pré-processamento

1. Transformação logarítmica nos preços
2. Normalização MinMaxScaler
3. Criação de sequências temporais
4. Split temporal em 2019

## 🛠️ Tecnologias

- Python 3.x
- TensorFlow/Keras
- Pandas & NumPy
- Scikit-learn
- Matplotlib

## 👨‍💻 Autor

**Mauro das Chagas Junior**
