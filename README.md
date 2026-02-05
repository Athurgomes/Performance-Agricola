# Agro-Intelligence: Performance e Rendimento Agrícola

## 1. Visão Geral do Projeto

Este projeto foi desenvolvido como parte de um plano de evolução pessoal e aperfeiçoamento técnico em Business Intelligence e Ciência de Dados. O dashboard simula um cenário de agricultura de precisão para explorar a análise de correlação entre variáveis climáticas, manejo de insumos e produtividade agrícola, aplicando conceitos de engenharia de software e inteligência artificial.


## 2. Arquitetura de Dados e Indicadores (KPIs)

O painel consolida métricas de desempenho para monitorar a saúde da operação em uma escala de milhares de quilogramas por hectare:

* **Eficiência do Fertilizante**: Representa a taxa de conversão do insumo em produção final, calculada em **22.42** no modelo atual.
* **Produtividade Média (Geral)**: Estabelece o rendimento médio por hectare através da base histórica, fixada em **3.66 Mil kg/ha**.
* **Status de Alerta de Umidade**: Processamento qualitativo da umidade do solo para rápida identificação de estresse hídrico ou saturação.


## 3. Detalhamento das Visualizações

### 3.1 Correlação: Investimento em Insumos vs. Resultado de Safra

Análise estatística visual para validar a resposta das culturas ao manejo de fertilizantes.

* **Eixos**: O eixo horizontal quantifica o uso de fertilizante () e o vertical a produtividade obtida ().
* **Tendência**: A inclusão de uma linha de regressão linear permite visualizar a eficiência da correlação positiva entre as variáveis.
* **Unidade de Análise**: O uso do **Talhão** como categoria de dados permite identificar variações de performance em diferentes áreas de plantio.

### 3.2 Impacto da Pluviosidade na Saúde do Solo e Rendimento

Gráfico de eixo duplo que correlaciona fatores ambientais com o rendimento temporal.

* **Precipitação**: Representada por colunas para visualização do volume acumulado mensal em milímetros.
* **Desempenho**: Linhas sobrepostas indicam a flutuação da umidade do solo e da produtividade, permitindo diagnosticar perdas em períodos de baixa pluviosidade.

### 3.3 Matriz de Desempenho (Heatmap)

Visualização em grade para monitoramento granular de produtividade.

* **Formatação Condicional**: Aplicação de gradiente cromático (verde ao vermelho) para destacar talhões com rendimento abaixo da média histórica.
* **Sazonalidade**: Permite a observação direta da performance mensal por unidade de produção.

### 3.4 Diagnóstico de IA (Árvore de Decomposição)

Implementação de recursos de Machine Learning nativos para análise de causa raiz.

* **Lógica**: O modelo decompõe a produtividade média para explicar quais dimensões (Cultura, Talhão ou Temperatura) possuem maior peso estatístico no resultado.


## 4. Implementação Técnica e DAX

A lógica de cálculo foi implementada utilizando a linguagem DAX para garantir dinamismo aos filtros e segmentações:

### 4.1 Eficiência do Fertilizante

Fórmula para cálculo do retorno sobre o insumo aplicado:


### 4.2 Ajuste de Escala para Umidade

Cálculo de normalização para permitir a comparação visual direta entre umidade e produtividade no gráfico de linhas:



## 5. Objetivos de Aprendizado Alcançados

O desenvolvimento deste projeto permitiu o aprofundamento em competências de engenharia de dados, visualização de informações e lógica aplicada ao agronegócio. A estrutura foca na transformação de dados brutos em insights acionáveis, respeitando os requisitos de clareza e precisão técnica necessários para o campo da inteligência artificial aplicada.
