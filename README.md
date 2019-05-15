# Docker compose para criação de containers úteis para criação de soluções Big Data

<h3> Substituir no arquivo docker-compose.yml o diretório '/home/iurimaia/Documents/docker_data' pelo diretório local</h3>
<b>OBS: Caso sua máquina não tenha mais 8GB de RAM é recomendado comentar todo o hadoop cloudera antes de rodar o docker compose.</b><br>
<h3> Para executar todos os containers o docker compose utilize o comando: </h3>
    
    docker-compose -f docker-compose.yml up 

============================================================================

<h1> Portainer </h1>
Ferramenta web para gerenciar seu Docker. </br>
https://www.portainer.io/ </br>
http://localhost:9000 </br>

    docker-compose -f docker-compose.yml up portainer

============================================================================

<h1> MongoDB </h1>
Banco de dados de documentos (NoSql). </br>
https://www.mongodb.com/ </br>
Porta:27017 </br>
Usuário: root </br>
Senha: root </br>

    docker-compose -f docker-compose.yml up mongo

============================================================================

<h1> Mongo Express </h1>
Ferramenta Web para utilizar o Banco MongoDB. </br>
http://localhost:8081 </br>
Usuário: root </br>
Senha: root </br>

    docker-compose -f docker-compose.yml up mongo-express

============================================================================

<h1> Neo4j </h1>
Banco de dados de grafos (NoSql). </br>
http://localhost:7474 </br>
Porta:7687 </br>
Usuário: neo4j </br>
Senha: neo4j </br>

    docker-compose -f docker-compose.yml up neo4j

============================================================================

<h1> Redis </h1>
Banco de dados chave valor (NoSql). </br>
https://redis.io/ </br>
porta:6379 </br>

    docker-compose -f docker-compose.yml up redis

============================================================================

<h1> Cassandra </h1>
Banco de dados colunar (NoSql). </br>
http://cassandra.apache.org/ </br>
porta:7000 </br>

    docker-compose -f docker-compose.yml up cassandra

============================================================================

<h1> Jupyter Notebook (All Spark)  </h1>
Jupyter Notebook com todos as iinguagens para programar com spark. </br>
Python 3 / Scala / R </br>
https://github.com/jupyter/docker-stacks </br>
http://localhost:8888 </br>

    docker-compose -f docker-compose.yml up jupyter_all_spark

============================================================================

<h1> R-studio  </h1>
R-studio para acesso web. </br>
https://github.com/rocker-org/rocker-versioned/tree/master/rstudio </br>
Porta original é 8787, porem foi trocada pois já estava em uso, para modificar basta substituir no arquivo 8788 por 8787 <br>
http://localhost:8788 </br>
Usuário: rstudio </br>
Senha: root </br>

    docker-compose -f docker-compose.yml up rstudio

============================================================================

<h1> Hadoop Cloudera  </h1>
Hadoop cloudera quickstart </br>
https://www.cloudera.com/documentation/enterprise/5-6-x/topics/quickstart_docker_container.html#cloudera_docker_container </br>

http://localhost:8889  # <b>Hue</b> </br>
Usuário: cloudera </br>
Senha: cloudera </br>

porta: 8020  # HDFS </br> 
porta: 8022  # SSH </br>
http://localhost:7180  # Cloudera Manager </br>
http://localhost:11000 # Oozie </br>
http://localhost:50070 # HDFS Rest Namenode </br>
http://localhost:50075 # HDFS Rest Datanode </br>
porta: 2181  # Zookeeper </br>
http://localhost:8088  # YARN Resource Manager </br>
http://localhost:19888 # MapReduce Job History </br>
porta: 50030 # MapReduce Job Tracker </br>
http://localhost:8983  # Solr </br>
porta: 16000 # Sqoop Metastore </br>
http://localhost:8042  # YARN Node Manager </br>
http://localhost:60010 # HBase Master </br>
http://localhost:60030 # HBase Region </br>
porta: 9090  # HBase Thrift </br>
porta: 8080  # HBase Rest </br>
porta: 7077  # Spark Master</br>

    docker-compose -f docker-compose.yml up hadoop_cloudera

============================================================================

<h1> Apache Airflow  </h1>
Workflow para agendar e orquestrar ETL dentre outros </br>
https://github.com/puckel/docker-airflow </br>
http://localhost:8089 </br>

    docker-compose -f docker-compose.yml up airflow

============================================================================
