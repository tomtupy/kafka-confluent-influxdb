#FROM confluentinc/cp-kafka-connect-base:5.2.1
FROM cnfldemos/kafka-connect-datagen:0.1.3-5.3.1
RUN wget https://github.com/lensesio/stream-reactor/releases/download/1.2.3/kafka-connect-influxdb-1.2.3-2.1.0-all.tar.gz
RUN tar xvf kafka-connect-influxdb-1.2.3-2.1.0-all.tar.gz -C /usr/share/java
COPY confluentinc-kafka-connect-jdbc-5.3.1/lib /usr/share/java/kafka-connect-jdbc/
RUN echo "schema.registry.url=http://localhost:8081" >> /etc/schema-registry/connect-avro-standalone.properties
RUN echo "schema.registry.url=http://localhost:8081" >> /etc/schema-registry/connect-avro-distributed.properties
