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

O código-fonte realiza as seguintes etapas:

1.  **Cálculo dos Somatórios:** Calcula $\sum x$, $\sum y$, $\sum xy$, e $\sum x^2$ usando loops `for` básicos.
2.  **Cálculo dos Coeficientes:** Determina os valores de $a$ (intercepto) e $b$ (slope) da reta de regressão.
3.  **Gráfico de Dispersão:** Plota os dados brutos ($x, y$) para visualizar a distribuição (Item 2 da atividade).
4.  **Plotagem da Reta:** Sobrepõe a reta de regressão ($y = a + bx$) ao gráfico de dispersão (Item 3 da atividade).
5.  **Coeficiente de Determinação ($R^2$):** (Opcional, mas recomendado) Calcula o $R^2$ para avaliar a qualidade do ajuste do modelo (Item 4 da atividade).

## 🛠️ Tecnologias Utilizadas

* **Python 3:** Linguagem principal.
* **Matplotlib:** Usada exclusivamente para a visualização dos dados (gráfico de dispersão e reta).
* **(Opcional) NumPy:** Utilizado para facilitar operações em vetores ao gerar os pontos da reta para plotagem.
    ```