# Criar topico

```bash
    docker exec -it kafka /opt/bitnami/kafka/bin/kafka-topics.sh \
        --create \
        --bootstrap-server localhost:9092 \
        --replication-factor 1 \
        --partitions 1 \
        --topic test
```

# Listar topicos

```bash
    docker exec -it kafka /opt/bitnami/kafka/bin/kafka-topics.sh \
        --list \
        --bootstrap-server localhost:9092
```

# Consumer
```bash
    docker exec -it kafka /opt/bitnami/kafka/bin/kafka-console-consumer.sh \
        --bootstrap-server localhost:9092 \
        --topic test \
        --from-beginning
```

# Gerando arquivos

```bash
    for i in 1 2 3 ; do curl http://metaphorpsum.com/sentences/3 >> file$i;done
```

# Executando 
```bash
    docker exec -it flume /bin/bash
```

```bash
    flume-ng agent --conf-file /opt/flume-config/flume.conf/spool-to-kafka.properties --name agent2 -Dflume.root.logger=WARN.console
```
