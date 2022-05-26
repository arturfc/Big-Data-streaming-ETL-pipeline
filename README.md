
# Big Data streaming usando ETL pipeline

Este projeto computa o resultado contínuo de um ambiente que simula a chegada de novos dados a cada momento, correspondentes à estrutura esperada. Este processo também é chamado de *Structured Streaming*.

A base de dados é composta por informações de companhias aéreas. O **objetivo** é, a partir da ingestão de dados, aplicar transformações para rankear a média do tempo de atraso de chegada dos voos das respectivas companhias aéreas, dentro da mesma categoria origem-destino.

## Requisitos para rodar o código

Para rodar o código, será necessário efetuar o download dos datasets localizados em [airlines-datasets](airlines-datasets). Após o download, é aconselhável que seja efetuado um upload dos arquivos para uma conta do google drive, pois ao decorrer do código será requisitado o diretório dos arquivos para suas devidas utilizações.
## Configurando variáveis do ambiente no Google Colab

Instale o java dentro da Virtual Machine

```python
!apt-get install openjdk-8-jdk-headless -qq > /dev/null
```

Escolha a versão mais recente do [spark](https://spark.apache.org/downloads.html) para download

```python
!wget -q https://downloads.apache.org/spark/spark-3.1.2/spark-3.1.2-bin-hadoop2.7.tgz
!tar xf /content/spark-3.1.2-bin-hadoop2.7.tgz
```

Crie as variáveis do ambiente

```python
import os
os.environ["JAVA_HOME"] = "/usr/lib/jvm/java-8-openjdk-amd64"
os.environ["SPARK_HOME"] =  "/content/spark-3.1.2-bin-hadoop2.7"
```


## Documentação

[PySpark documentation](https://sparkbyexamples.com/pyspark/)

