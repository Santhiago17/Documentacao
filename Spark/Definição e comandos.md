### Spark

Spark é uma plataforma de computação distribuída de código aberto, projetada para realizar processamento de dados em grande escala de forma rápida e eficiente. PySpark é a interface Python para o Spark, que permite aos desenvolvedores utilizar a linguagem Python para interagir com o Spark e realizar suas análises de dados.

### Conceitos fundamentais

* RDDs (Resilient Distributed Datasets): A unidade básica de dados no Spark. São coleções imutáveis de dados distribuídos em vários nós de um cluster.

* Transformações: Operações que criam um novo RDD a partir de um RDD existente, como map, filter, reduceByKey, etc.

* Ações: Operações que retornam um resultado após a execução, como count, collect, saveAsTextFile, etc.

* DataFrames: Uma abstração de dados semelhante a um DataFrame em SQL, otimizada para processamento de dados estruturados.

* Spark SQL: Um módulo para trabalhar com dados estruturados usando SQL ou a API DataFrame.

* Structured Streaming: Um motor de processamento de streaming que permite processar dados em tempo real.

* MLlib: Uma biblioteca de aprendizado de máquina integrada ao Spark para construir modelos de machine learning em grande escala.

### Comandos e Funcionalidades Essenciais

* Criando RDDs:
```python
sc.textFile("meu_arquivo.txt"): Cria um RDD a partir de um arquivo de texto.
sc.parallelize([1, 2, 3]): Cria um RDD a partir de uma lista
```

* Operações básicas:
map: Aplica uma função a cada elemento de um RDD.
filter: Filtra elementos de um RDD com base em uma condição.
reduce: Reduz os elementos de um RDD a um único valor.
groupBy: Agrupa elementos de um RDD com base em uma chave.

* DataFrames:
```python
spark.read.csv("meu_arquivo.csv"): Carrega um arquivo CSV em um DataFrame.
df.select("coluna1", "coluna2"): Seleciona colunas de um DataFrame.
df.filter(df.idade > 30): Filtra linhas de um DataFrame com base em uma condição.
df.groupBy("pais").count(): Agrupa por país e conta o número de registros.
```

* Spark SQL:
```python
df.createOrReplaceTempView("minha_tabela"): Cria uma tabela temporária.
spark.sql("SELECT * FROM minha_tabela"): Executa uma consulta SQL.
```
* MLlib:
LinearRegression: Regressão linear.
LogisticRegression: Regressão logística.
RandomForestClassifier: Floresta aleatória para classificação.