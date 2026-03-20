# Avaliação de Turbinas Eólicas

Análise de desempenho de uma turbina eólica com base em dados reais de geração ao longo de 2018, comparando a potência ativa gerada com a curva de potência teórica.

## Objetivo

Identificar e classificar os registros operacionais da turbina em três categorias:
- **Dentro** — geração dentro de ±5% da curva teórica (operação eficiente)
- **Fora** — geração fora do intervalo aceitável
- **Zero** — geração nula (parada ou vento insuficiente)

## Dataset

| Campo | Descrição |
|---|---|
| `Date/Time` | Data e hora (intervalo de 10 minutos) |
| `LV ActivePower (kW)` | Potência ativa gerada pela turbina |
| `Wind Speed (m/s)` | Velocidade do vento no momento da medição |
| `Theoretical_Power_Curve (KWh)` | Potência esperada conforme curva teórica |

- **Fonte:** [Kaggle — Wind Power Forecasting](https://www.kaggle.com/datasets/theforcecoder/wind-power-forecasting)
- **Período:** Janeiro a Dezembro de 2018
- **Volume:** 50.530 registros

## Estrutura do Projeto

```
├── Avaliação turbinas.ipynb   # Notebook principal com a análise
├── T1.csv                     # Dataset da turbina
└── README.md
```

## Metodologia

1. **Carregamento e pré-processamento** — renomeação de colunas, conversão de tipos, remoção de variável não utilizada
2. **Análise exploratória** — estatísticas descritivas, visualização da relação vento × potência
3. **Classificação de desempenho** — tolerância de ±5% sobre a curva teórica
4. **Análise mensal** — variação de eficiência ao longo do ano

## Principais Resultados

- ~**37%** dos registros operam dentro do limite de eficiência estabelecido
- A maioria dos pontos "Fora" concentra-se em velocidades intermediárias de vento
- Existe variação sazonal relevante na eficiência ao longo dos meses

## Como executar

```bash
# Clone o repositório
git clone https://github.com/vianakaique12/avaliacao-turbinas.git
cd avaliacao-turbinas

# Instale as dependências
pip install pandas matplotlib seaborn jupyter

# Execute o notebook
jupyter notebook "Avaliação turbinas.ipynb"
```

## Tecnologias

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-orange)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-red)
