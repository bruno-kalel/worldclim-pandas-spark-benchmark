![Static Badge](https://img.shields.io/badge/python-%233776AB?style=for-the-badge&logo=python&logoColor=white)
![Static Badge](https://img.shields.io/badge/pandas-%23150458?style=for-the-badge&logo=pandas&logoColor=white)
![Static Badge](https://img.shields.io/badge/google%20colab-%23F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)
![Static Badge](https://img.shields.io/badge/apache%20spark-%23E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)
![Static Badge](https://img.shields.io/badge/apache%20parquet-%2350ABF1?style=for-the-badge&logo=apacheparquet&logoColor=white)

# Benchmark de Carregamento e Consulta de Dados Climáticos com Pandas e Spark
Este projeto tem como objetivo realizar um benchmark de carregamento da base e de consulta de dados climáticos da WorldClim utilizando Pandas e Apache Spark para processamento de dados em diferentes escalas de resolução.

## Contexto
A WorldClim disponibiliza dados climáticos globais em diferentes resoluções espaciais. Neste projeto, foram utilizados dados de precipitação em resoluções de 10m, 5m e 2.5m. A análise é conduzida comparando o desempenho e a escalabilidade entre Pandas DataFrame (processamento não-distribuído) e Spark DataFrame (processamento distribuído) no carregamento da base e na execução de consultas.

## Funcionalidades
* *Download e Conversão de Dados*: Os dados da WorldClim foram baixados em formato raster e convertidos para arquivos CSV utilizando a ferramenta raster2xyz.
* *Benchmark de Carregamento*: Avaliou-se o tempo de carregamento dos dados utilizando Pandas e Spark DataFrame.
* *Benchmark de Consulta*: Avaliou-se o tempo de execução de consultas simples nos dados carregados utilizando Pandas e Spark DataFrame.
* *Exportação para Parquet*: Os dados foram exportados para o formato Parquet, para, finalmente, testar um formato de armazentamento colunar.

## Resultados
Os resultados do benchmark indicam claramente a superioridade do processamento distribuído em relação ao não-distribuído em termos de desempenho e escalabilidade para consultas em grandes conjuntos de dados, climáticos ou não. A escolha do formato de armazenamento Parquet, com armazenamento colunar, também contribuiu significativamente para a eficiência das consultas. Essas conclusões destacam a importância do processamento distribuído e do armazenamento adequado na análise de dados em larga escala.
