# Dicionário de Dados: Monitoramento Agrícola

Este documento detalha a estrutura, os tipos de dados e o significado de cada variável contida no arquivo `dataset_agronomia_completo.csv`. O conjunto de dados foi projetado para análises de agricultura de precisão e correlação entre variáveis ambientais e rendimento de safra.

## Estrutura do Arquivo

| Nome da Coluna | Tipo de Dado | Descrição | Unidade de Medida |
| --- | --- | --- | --- |
| **Data** | Date | Data da coleta do registro no formato AAAA-MM-DD. | N/A |
| **Talhao** | String | Identificador da unidade de produção (divisão da área de plantio). | N/A |
| **Cultura** | String | Espécie vegetal cultivada na área (Soja, Milho, Algodão ou Trigo). | N/A |
| **Umidade_Solo_Pct** | Float | Nível de umidade presente no solo no momento da leitura. | Porcentagem (%) |
| **Precipitacao_mm** | Float | Volume de chuva acumulado no período de registro. | Milímetros (mm) |
| **Temperatura_C** | Float | Temperatura média registrada no ambiente durante o ciclo. | Graus Celsius (°C) |
| **Fertilizante_kg_ha** | Float | Quantidade de insumo (fertilizante) aplicado por unidade de área. | Quilogramas por Hectare () |
| **Produtividade_kg_ha** | Float | Rendimento total da colheita final obtido na unidade de área. | Quilogramas por Hectare () |

## Detalhes Técnicos e Observações

### 1. Granularidade dos Dados

A unidade mínima de análise é o **Talhão** por **Data**. Cada linha representa o estado consolidado de uma área de plantio específica em um determinado dia do ciclo produtivo.

### 2. Variáveis Derivadas

Embora não estejam presentes no arquivo bruto, o dashboard utiliza as seguintes métricas calculadas via DAX:

* **Eficiência do Fertilizante**: Razão entre a produtividade total e a quantidade de fertilizante aplicada.
* **Umidade Normalizada**: Ajuste escalar da umidade para visualização comparativa com a produtividade no mesmo eixo gráfico.

### 3. Integridade dos Dados

* Os valores de **Produtividade_kg_ha** sofrem influência direta das variáveis **Precipitacao_mm** e **Temperatura_C**, simulando o comportamento biológico real das culturas sob estresse hídrico ou térmico.
* Campos numéricos utilizam o ponto (.) como separador decimal, seguindo o padrão internacional de arquivos CSV.
