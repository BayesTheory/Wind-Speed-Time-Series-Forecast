# Previsão de Velocidade do Vento com Séries Temporais

Este repositório contém um Jupyter Notebook (`Cópia_de_PREVISAO_DO_VENTO.ipynb`) que explora diferentes métodos estatísticos e de Machine Learning para a previsão da velocidade do vento a 10 metros (`WS10m [m.s-1]`) utilizando dados meteorológicos.

## Objetivo

O objetivo principal é analisar uma série temporal de velocidade do vento, identificar suas características (tendência, sazonalidade, estacionariedade) e aplicar diferentes modelos de previsão para comparar suas abordagens.

## Dados Utilizados

O notebook utiliza um arquivo CSV (`SBLB_WRF_AZUL_00-24h.csv`) contendo dados meteorológicos, incluindo:
*   `Date`: Data e hora da observação/previsão.
*   `T2m [°C]`: Temperatura do ar a 2m.
*   `Td2m [°C]`: Ponto de orvalho a 2m.
*   `RH2m [%]`: Umidade relativa a 2m.
*   `SLP [hPa]`: Pressão ao nível do mar.
*   **`WS10m [m.s-1]`**: Velocidade do vento a 10m (variável alvo principal).
*   `WD10m [°]`: Direção do vento a 10m.
*   `Prec [mm]`: Precipitação.
*   `SWDN`, `SWUP`, `LWDN`, `LWUP`: Componentes de radiação.

## Métodos Explorados

1.  **Análise Exploratória de Dados (EDA):**
    *   Visualização da série temporal original.
    *   Matriz de correlação entre variáveis.
    *   Decomposição da série (tendência, sazonalidade, resíduos) usando `statsmodels.tsa.seasonal.seasonal_decompose`.
    *   Boxplots mensais para análise de sazonalidade.
2.  **Identificação da Série Temporal:**
    *   Análise de autocorrelação (ACF) e autocorrelação parcial (PACF).
    *   Teste de estacionariedade (Augmented Dickey-Fuller - ADF).
3.  **Modelagem Estatística (`statsmodels`):**
    *   ARIMA (Autoregressive Integrated Moving Average).
    *   ARIMAX (ARIMA com variáveis exógenas).
    *   SARIMA (Seasonal ARIMA).
    *   SARIMAX (Seasonal ARIMA com variáveis exógenas).
    *   Avaliação dos modelos usando AIC, BIC, HQIC e análise de resíduos (Jarque-Bera, Ljung-Box).
    *   Busca por parâmetros ótimos usando `itertools`.
4.  **Modelagem com Machine Learning (`tensorflow`/`keras`):**
    *   Rede Neural Recorrente com camadas LSTM (Long Short-Term Memory).
    *   Utilização de outras variáveis meteorológicas como features.
    *   Normalização dos dados usando `StandardScaler`.
    *   Treinamento e avaliação do modelo LSTM.

