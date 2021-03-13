# PySpark
## Spark — Обзор
Apache Spark — это молниеносная среда обработки в реальном времени. 
Он выполняет вычисления в памяти для анализа данных в режиме реального времени.
Это стало очевидным, поскольку Apache Hadoop MapReduce выполнял только пакетную обработку и не имел функции обработки в реальном времени. Поэтому был представлен Apache Spark, поскольку он может выполнять потоковую обработку в режиме реального времени, а также может выполнять пакетную обработку

## PySpark

Apache Spark написан на языке программирования Scala . Для поддержки Python с помощью Spark сообщество Apache Spark выпустило инструмент PySpark. Используя PySpark, вы также можете работать с RDD на языке программирования Python. Именно благодаря библиотеке под названием Py4j они могут достичь этого.

PySpark предлагает PySpark Shell, который связывает Python API с ядром искры и инициализирует контекст Spark. Большинство исследователей данных и аналитиков сегодня используют Python из-за его богатого набора библиотек. Интеграция Python с Spark является благом для них.

## PySpark — настройка среды

Примечание. Это означает, что на вашем компьютере установлены Java и Scala.

Давайте теперь загрузим и настроим PySpark со следующими шагами.

### Шаг 1 — Перейдите на официальную страницу загрузки Apache Spark и загрузите последнюю версию Apache Spark, доступную там. Мы используем spark-2.1.0-bin-hadoop2.7 .

### Шаг 2 — Теперь распакуйте скачанный файл Spark tar. По умолчанию он будет загружен в каталог загрузок.

### tar -xvf Downloads/spark-2.1.0-bin-hadoop2.7.tgz
Это создаст каталог spark-2.1.0-bin-hadoop2.7 . Перед запуском PySpark необходимо установить следующие среды, чтобы задать путь Spark и путь Py4j .

export SPARK_HOME = /home/hadoop/spark-2.1.0-bin-hadoop2.7
export PATH = $PATH:/home/hadoop/spark-2.1.0-bin-hadoop2.7/bin
export PYTHONPATH = $SPARK_HOME/python:$SPARK_HOME/python/lib/py4j-0.10.4-src.zip:$PYTHONPATH
export PATH = $SPARK_HOME/python:$PATH
Или, чтобы установить вышеуказанные среды глобально, поместите их в файл .bashrc . Затем выполните следующую команду, чтобы среды работали.

### source .bashrc
Теперь, когда все среды установлены, давайте перейдем в каталог Spark и вызовем оболочку PySpark, выполнив следующую команду:

### ./bin/pyspark
Это запустит вашу оболочку PySpark.
