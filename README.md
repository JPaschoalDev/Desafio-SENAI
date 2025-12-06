# 🛫 Análise Exploratória de Atrasos em Voos

> Projeto do Desafio 01 - Curso de Inteligência Artificial Industrial (SENAI)

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-1.5+-green.svg)](https://pandas.pydata.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## 📊 Sobre o Projeto

Análise exploratória de dados (EDA) completa de um dataset com **539.383 voos** para identificar padrões e fatores que influenciam atrasos de aeronaves. O projeto aplica técnicas de Data Science para preparação de dados e feature engineering.

### 🎯 Objetivos

- Realizar análise exploratória completa do dataset
- Identificar outliers e anomalias nos dados
- Criar features para futura modelagem de Machine Learning
- Gerar insights sobre fatores que afetam atrasos

---

## 🗂️ Estrutura do Dataset

| Variável | Tipo | Descrição |
|----------|------|-----------|
| `Airline` | Categórica | Código da companhia aérea |
| `Flight` | Numérica | Número do voo |
| `AirportFrom` | Categórica | Aeroporto de origem (código IATA) |
| `AirportTo` | Categórica | Aeroporto de destino (código IATA) |
| `DayOfWeek` | Numérica | Dia da semana (1-7) |
| `Time` | Numérica | Horário de partida (formato HHMM) |
| `Length` | Numérica | Duração do voo (minutos) |
| `Delay` | Binária | **Target** - 0 = sem atraso, 1 = com atraso |

**Total:** 539.383 registros | **Balanceamento:** 44,54% de atrasos

---

## 🔍 Análises Realizadas

### 1. Exploração Inicial
- ✅ Inspeção da estrutura dos dados
- ✅ Classificação de variáveis (numéricas × categóricas)
- ✅ Análise de valores ausentes (0% de nulos!)

### 2. Estatísticas Descritivas
- 📊 Medidas de tendência central e dispersão
- 📈 Análise de quartis e amplitude interquartil (IQR)
- 🔢 Coeficiente de variação

### 3. Análise da Variável-Alvo
- 🎯 Distribuição de atrasos
- 🚦 Taxa de atrasos por categoria
- 🔴 Identificação de outliers (Regra 1.5×IQR)

### 4. Feature Engineering
- `Atraso_Absoluto`: Magnitude do desvio
- `Categoria_Atraso`: Classificação em 4 níveis
- Preparação para modelagem futura

---

## 📈 Principais Insights

### 🔑 Descobertas

1. **Dataset balanceado:** 55% sem atraso vs 45% com atraso
2. **Top 3 companhias por volume:**
   - WN (Southwest): 17,45%
   - DL (Delta): 11,30%
   - OO (SkyWest): 9,32%

3. **Aeroportos mais movimentados:**
   - ATL (Atlanta): 34.449 voos
   - ORD (Chicago): 24.822 voos
   - DFW (Dallas): 22.154 voos

4. **Anomalias identificadas:**
   - Voos com duração = 0 minutos (investigar)
   - Distribuição assimétrica em `Length` (cauda à direita)

### 💡 Hipóteses para Investigação Futura

- Sazonalidade por dia da semana
- Impacto de horários de pico (6-9h, 18-21h)
- Diferenças entre companhias aéreas
- Influência da distância do voo
- Rotas origem-destino específicas

---

## 📊 Visualizações

<p align="center">
  <img src="outputs/distribuicao_atrasos.png" width="45%" />
  <img src="outputs/heatmap_correlacoes.png" width="45%" />
</p>

<p align="center">
  <img src="outputs/distribuicao_categorias.png" width="45%" />
  <img src="outputs/top_companhias_atrasos.png" width="45%" />
</p>

---

## 🛠️ Tecnologias Utilizadas

- **Python 3.8+**
- **Pandas** - Manipulação de dados
- **NumPy** - Operações numéricas
- **Matplotlib** - Visualizações básicas
- **Seaborn** - Visualizações estatísticas
- **Jupyter Notebook** - Ambiente de desenvolvimento

---

## 🚀 Como Executar

### Pré-requisitos

pip install pandas numpy matplotlib seaborn jupyter


### Executar o Notebook

Clone o repositório
git clone https://github.com/JPaschoalDev/desafio-senai-aed.git

Entre na pasta
cd desafio-senai-aed

Abra o Jupyter Notebook
jupyter notebook Predicting_Airplane_Delays.ipynb

---

## 🎓 Próximos Passos

- [ ] Feature Engineering avançado (one-hot encoding, target encoding)
- [ ] Seleção de features (correlação, importância)
- [ ] Treinamento de modelos (Logistic Regression, Random Forest, XGBoost)
- [ ] Otimização de hiperparâmetros
- [ ] Deploy do modelo

---

## 👨‍💻 Autor

**[João Victor Paschoal]**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](www.linkedin.com/in/joao-paschoal-dev)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com/JPaschoalDev)

---

## 🙏 Agradecimentos

- **SENAI** - Curso de Inteligência Artificial Industrial
- **Kaggle** - Dataset Airlines
- Comunidade Data Science Brasil

---

<p align="center">
  <i>Desenvolvido com 💙 durante o Desafio do SENAI</i>
</p>
