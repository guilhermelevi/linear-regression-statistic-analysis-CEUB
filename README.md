# Regressão Linear "do Zero" com Dados de Erupção

## 📖 Descrição do Projeto

Este projeto implementa um modelo de Regressão Linear Simples para analisar a relação entre a duração das erupções de um gêiser e o intervalo de tempo até a próxima erupção.

O principal objetivo é demonstrar o cálculo e a visualização de uma regressão linear **sem o uso de bibliotecas de machine learning ou estatística prontas**, como `scikit-learn` ou `statsmodels`. Todos os coeficientes e métricas são calculados manualmente usando apenas operações básicas de Python.

## ✨ Destaque Principal: Cálculo Manual

A regressão linear, representada pela equação $y = a + bx$, foi totalmente calculada "do zero":

* **Coeficiente Angular ($b$ ou $\beta_1$):** Calculado usando a fórmula dos mínimos quadrados:
    $$b = \frac{n(\sum xy) - (\sum x)(\sum y)}{n(\sum x^2) - (\sum x)^2}$$

* **Intercepto ($a$ ou $\beta_0$):** Calculado a partir das médias e do coeficiente $b$:
    $$a = \bar{y} - b\bar{x}$$

## 📊 Funcionalidades

O código-fonte realiza as quatro etapas da atividade:

1.  **Cálculo dos Coeficientes:** Determina os valores de $a$ (intercepto) e $b$ (slope) da reta de regressão (Item 1).
2.  **Gráfico de Dispersão:** Plota os dados brutos ($x, y$) para visualizar a distribuição (Item 2).
3.  **Plotagem da Reta:** Sobrepõe a reta de regressão ($y = a + bx$) ao gráfico de dispersão (Item 3).
4.  **Cálculo do $R^2$:** Calcula o Coeficiente de Determinação ($R^2$) para avaliar a qualidade do ajuste do modelo (Item 4).

## 🎯 Avaliação do Modelo (R²)

Para medir a eficácia do modelo, o **Coeficiente de Determinação ($R^2$)** também foi calculado manualmente.

O $R^2$ indica a proporção da variância na variável $y$ (Intervalo) que é previsível a partir da variável $x$ (Duração).

**Fórmula Manual Utilizada:**
$$R^2 = 1 - \frac{SQ_{res}}{SQ_{tot}}$$

Onde:
* **$SQ_{tot}$ (Soma dos Quadrados Total):** $\sum (y_i - \bar{y})^2$. Mede a variação total dos dados $y$ em torno da média $\bar{y}$.
* **$SQ_{res}$ (Soma dos Quadrados dos Resíduos):** $\sum (y_i - \hat{y}_i)^2$. Mede o erro (variação não explicada) entre os pontos reais ($y_i$) e os pontos previstos pela reta ($\hat{y}_i$).

Um $R^2$ próximo de 1 indica um ajuste excelente, mostrando que o modelo explica uma grande parte da variação dos dados.

## 🛠️ Tecnologias Utilizadas

* **Python 3:** Linguagem principal.
* **Matplotlib:** Usada exclusivamente para a visualização dos dados (gráfico de dispersão e reta).
* **NumPy:** Utilizado para facilitar operações em vetores ao gerar os pontos da reta para plotagem.