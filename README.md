# Rossmann_DS_project

## [English] Rossmann - Sales Forecast

This repository contains a data science project for forecasting sales of Rossmann pharmacy chain stores. The objective is to provide insights to the company's CFO, allowing strategic decisions regarding investments in store renovations based on the sales forecasts for the next 6 weeks.

### Project Objective

The Rossmann chain operates more than 3,000 drug stores across 7 European countries, being responsible for managing inventory and daily sales with precision. Aiming to increase staff productivity, Rossmann store managers have been tasked with predicting daily sales up to six weeks in advance. Additionally, these forecasts will enable the company's CFO to make strategic decisions about store renovation investments, directing resources to those stores with the highest sales potential.

However, these forecasts are influenced by several factors such as promotions, competition, school and state holidays, seasonality, and regional specifics. This leads to sales predictions that can vary greatly in terms of accuracy across different managers. Therefore, the goal of this project is to develop a robust machine-learning model capable of predicting daily sales for 1,115 Rossmann stores located in Germany, for the next 6 weeks.

### Data
The data used in this project was obtained from Kaggle (https://www.kaggle.com/c/rossmann-store-sales/data) and includes information such as:

- Id - an Id that represents a (Store, Date) duple within the test set
- Store - a unique Id for each store
- Sales - the turnover for any given day (this is what you are predicting)
- Customers - the number of customers on a given day
- Open - an indicator for whether the store was open: 0 = closed, 1 = open
- StateHoliday - indicates a state holiday. Normally all stores, with few exceptions, are closed on state holidays. Note that all schools are closed on public holidays and weekends. a = public holiday, b = Easter holiday, c = Christmas, 0 = None
- SchoolHoliday - indicates if the (Store, Date) was affected by the closure of public schools
- StoreType - differentiates between 4 different store models: a, b, c, d
- Assortment - describes an assortment level: a = basic, b = extra, c = extended
- CompetitionDistance - distance in meters to the nearest competitor store
- CompetitionOpenSince[Month/Year] - gives the approximate year and month of the time the nearest competitor was opened
- Promo - indicates whether a store is running a promo on that day
- Promo2 - Promo2 is a continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating
- Promo2Since[Year/Week] - describes the year and calendar week when the store started participating in Promo2
- PromoInterval - describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store

### Repository Structure

- data/: Folder containing the datasets (not included in the repository due to size, available on Kaggle).
- notebooks/: Contains Jupyter Notebooks with exploratory data analysis, feature engineering, and the prediction model development.

### Models and Tools Used

Prediction Models:

Several machine learning models were tested, such as Linear Regression, Decision Trees, and other advanced models to improve the accuracy of the forecasts.

Libraries:

- pandas for data manipulation.
- scikit-learn for model building and evaluation.
- Flask for building an API that serves the predictions (https://github.com/jessicanadalete/test_API_rossmann.git).
- Telegram API for sending real-time predictions (https://github.com/jessicanadalete/API_bot_telegram.git).

## Results

The sales forecasts are provided for each individual store, allowing Rossmann's CFO to identify which stores will perform better in the coming months and decide where to invest in renovations. The final result can be checked directly via the Telegram bot by providing the store code (Store).


## [Portuguese] Rossmann - Previsão de Vendas 

Este repositório contém um projeto de ciência de dados para previsão de vendas das lojas da rede de farmácias Rossmann, com o objetivo de fornecer insights para o CFO da empresa, permitindo decisões estratégicas sobre investimentos em reformas de lojas, com base nas previsões de vendas dos próximos 6 semanas.

### Objetivo do Projeto

A rede Rossmann opera mais de 3.000 lojas de drogarias em 7 países europeus, sendo responsável por gerenciar o estoque e as vendas diárias de forma precisa. Visando aumentar a produtividade da equipe, os gerentes das lojas da Rossmann foram encarregados de prever as vendas diárias com até seis semanas de antecedência. Além disso, essas previsões permitirão que o CFO da empresa seja capaz de tomar decisões estratégicas sobre investimentos em reformas das lojas, direcionando os recursos para aquelas com maior potencial de vendas.

Essas previsões, no entanto, são influenciadas por diversos fatores, como promoções, competição, feriados escolares e estaduais, sazonalidade e particularidades regionais. Isso resulta em previsões de vendas que podem variar bastante em termos de precisão entre os diferentes gerentes. Dessa forma, o objetivo deste projeto é desenvolver um modelo de machine learning robusto que seja capaz de prever as vendas diárias para 1.115 lojas da Rossmann localizadas na Alemanha, para as próximas 6 semanas.

### Dados
Os dados utilizados neste projeto foram obtidos do Kaggle (https://www.kaggle.com/c/rossmann-store-sales/data) e incluem informações como:

- Id - um Id que representa Loja e Data, respectivamente, dentro do conjunto de teste.
- Store - um Id exclusivo para cada loja.
- Sales - o faturamento em um determinado dia.
- Customers - o número de clientes em um determinado dia.
- Open - um indicador de se a loja estava aberta: 0 = fechada, 1 = aberta.
- StateHoliday - indica um feriado estadual. Normalmente, todas as lojas, com poucas exceções, estão fechadas em feriados estaduais: a = feriado público, b = feriado de Páscoa, c = Natal, 0 = Nenhum.
- SchoolHoliday - indica se a (Loja, Data) foi afetada pelo fechamento de escolas públicas.
- StoreType - tipos de modelos de loja: a, b, c, d.
- Assortment - descreve o nível do sortimento: a = básico, b = extra, c = estendido.
- CompetitionDistance - distância em metros até a loja concorrente mais próxima.
- CompetitionOpenSince[Mês/Ano] - indica o ano e o mês aproximados em que a loja concorrente mais próxima foi aberta.
- Promo - indica se uma loja está realizando uma promoção naquele dia.
- Promo2 - Promo2 é uma promoção contínua e consecutiva para algumas lojas: 0 = a loja não está participando, 1 = a loja está participando.
- Promo2Since[Ano/Semana] - descreve o ano e a semana do calendário em que a loja começou a participar do Promo2.
- PromoInterval - descreve os intervalos consecutivos em que a Promo2 é iniciada, nomeando os meses em que a promoção começa novamente. Exemplo: "Fev, Mai, Ago, Nov" significa que cada rodada começa em fevereiro, maio, agosto e novembro de qualquer ano para aquela loja.

### Estrutura do Repositório

- data/: Pasta contendo os datasets (não incluídos no repositório devido ao tamanho, disponíveis no Kaggle).
- notebooks/: Contém os Jupyter Notebooks com a análise exploratória dos dados, engenharia de features e construção do modelo de previsão.

### Modelos e Ferramentas Utilizadas

Modelos de Previsão: 

Foram testados diferentes modelos de machine learning, como Regressão Linear, Árvore de Decisão, e outros modelos avançados para melhorar a precisão das previsões.

Bibliotecas:

- pandas para manipulação de dados.
- scikit-learn para construção e avaliação dos modelos.
- Flask para a construção de uma API que serve as previsões (https://github.com/jessicanadalete/test_API_rossmann.git).
- Telegram API para envio de previsões em tempo real (https://github.com/jessicanadalete/API_bot_telegram.git).

## Resultados
As previsões de vendas são fornecidas para cada loja individualmente, permitindo ao CFO da Rossmann identificar quais lojas terão um desempenho melhor nos próximos meses e, assim, decidir onde investir em reformas. O resultado final pode ser verificado diretamente via bot do Telegram, fornecendo o código da loja (Store).
