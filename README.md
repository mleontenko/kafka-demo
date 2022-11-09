# kafka-demo

1. Download Kafka: wget wget https://archive.apache.org/dist/kafka/2.8.0/kafka_2.12-2.8.0.tgz
2. Extract Kafka: tar -xzf kafka_2.12-2.8.0.tgz
3. MySQL: create database tolldata;
4. MySQL: 
    use tolldata;
    create table livetolldata(timestamp datetime,vehicle_id int,vehicle_type char(15),toll_plaza_id smallint);
5. Python: 
    python3 -m pip install kafka-python
    python3 -m pip install mysql-connector-python
    
6. Start Kafka Zookeeper: bin/zookeeper-server-start.sh config/zookeeper.properties
7. Start Kafka broker service: bin/kafka-server-start.sh config/server.properties
8. Create topic: bin/kafka-topics.sh --create --topic toll --bootstrap-server localhost:9092
9. python3 toll_traffic_generator.py
10. python3 streaming_data_reader.py
