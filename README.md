# 🎬 YouTube US Videos ETL Pipeline with PySpark
Building a scalable data processing workflow to clean, aggregate and optimize YouTube US video data using PySpark.

## 🎯 Objetivos
- Praticar técnicas de ETL (Extract, Transform, Load) com PySpark
- Demonstrar habilidades em tratamento de dados em larga escala
- Preparar dados para análises subsequentes

## 📁 Estrutura do Projeto
exercicio1-tratamento-dados/
├── notebooks/
│ └── 01_data_cleaning_pyspark.ipynb
  └── 02_aggregations_analysis.ipynb.ipynb
├── data/
│ ├── videos-stats.csv
│ ├── comments.csv
│ └── USvideos.csv
├── output/
│ ├── videos-tratados-parquet/
│ └── videos-comments-tratados-parquet/
├── requirements.txt
└── README.md

## 🛠️ Tecnologias Utilizadas
- **Apache Spark 3.4.0**
- **PySpark**
- **Python 3.8+**
- **Jupyter Notebook**

## 📈 Conjuntos de Dados
### Fontes de Dados:
1. **videos-stats.csv**: Estatísticas de vídeos (visualizações, likes, comentários)
2. **comments.csv**: Comentários e sentimentos dos usuários
3. **USvideos.csv**: Metadados de vídeos dos EUA

### Tamanho dos Dados:
- Total de registros processados: ±50,000 registros
- Colunas processadas: 15+ colunas

## 🔧 Técnicas de Tratamento Aplicadas

### 1. Tratamento de Valores Nulos
```python
# Substituição de nulos por 0 em colunas numéricas
df_video.na.fill({'Likes': 0, 'Comments': 0, 'Views': 0})



### 2. Análise de Agregações - [`02_aggregations_analysis.ipynb`](notebooks/02_aggregations_analysis.ipynb)

Análise estatística e agregações avançadas com PySpark.

### 📊 Métricas Calculadas:
- **Estatísticas por Keyword**: contagem, médias, valores máximos
- **Análise temporal**: distribuição por ano e mês
- **Window functions**: médias acumulativas
- **Qualidade de dados**: análise de duplicatas

### 🛠️ Técnicas Utilizadas:
- `groupBy()` com múltiplas agregações
- `Window functions` para cálculos acumulativos
- `countDistinct()` para análise de unicidade
- Ordenação e formatação de resultados

## 3. Otimização de Performance - [`03_spark_optimization.ipynb`](notebooks/03_spark_optimization.ipynb)

Técnicas avançadas de otimização e tuning de performance no Spark.

### 🚀 Técnicas de Otimização:
- **Repartition vs Coalesce**: Balanceamento de partições
- **Análise de Planos de Execução**: Explain plans detalhados
- **Join Optimization**: Estratégias para joins eficientes
- **Filtros Inteligentes**: Predicate pushdown
- **Compressão**: Snappy compression para armazenamento

### 📊 Métricas de Performance:
- Comparativo de tempos de execução
- Análise de ganhos de performance
- Monitoramento de utilização de recursos

### ⚡ Resultados Obtidos:
- Melhoria de performance: 50-70% mais rápido
- Redução de armazenamento: 60% com compressão
- Join eficiente entre grandes datasets
