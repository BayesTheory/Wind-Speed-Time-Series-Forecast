# Previsao-do-Vento-xsar
Previsão do vento apesar de não ser o melhor metodo, estou usando metodo estatistico de séries temporais:

    AR
    ARMA
    ARIMA
    ARIMAX
    SARIMAX


Significado das colunas:

    T2m [°C]: Temperatura do ar a 2 metros acima do solo, medida em graus Celsius.
    Td2m [°C]: Ponto de orvalho a 2 metros acima do solo, também em graus Celsius. O ponto de orvalho é a temperatura na qual o ar precisa ser resfriado para se tornar saturado com vapor de água.
    RH2m [%]: Umidade relativa do ar a 2 metros acima do solo, expressa em porcentagem. Indica a quantidade de vapor de água presente no ar em relação à quantidade máxima que o ar pode conter naquela temperatura.
    SLP [hPa]: Pressão atmosférica ao nível do mar, medida em hectopascals. É ajustada para o nível do mar para permitir comparações entre diferentes altitudes. WS10m [m.s-1]: Velocidade do vento a 10 metros acima do solo, medida em metros por segundo.
    WD10m [°]: Direção do vento a 10 metros acima do solo, medida em graus, onde um valor de 0° indica vento vindo do norte e valores aumentam no sentido horário.
    Prec [mm]: Precipitação acumulada, medida em milímetros. Refere-se à quantidade total de precipitação que caiu durante um determinado período de tempo.
    SWDN: Radiação solar direta incidente na superfície, medida em watts por metro quadrado. É a quantidade de radiação solar que chega diretamente do sol.
    SWUP: Radiação solar refletida pela superfície, também medida em watts por metro quadrado. É a quantidade de radiação solar que é refletida de volta para o espaço.
    LWDN: Radiação de onda longa incidente na superfície, medida em watts por metro quadrado. É a radiação emitida pela atmosfera que é absorvida pela superfície terrestre.
    LWUP: Radiação de onda longa emitida pela superfície e que escapa para o espaço, medida em watts por metro quadrado. É a radiação térmica emitida pela superfície da Terra.



Requeriments:

    tensorflow 
    pandas
    matplotlib
    numpy 
    seaborn 
    sklearn.model_selection
    statsmodels.tsa.seasonal
    sklearn.preprocessing
