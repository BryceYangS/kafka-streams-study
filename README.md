# Kafka Streams 
- 

## 0.Introduction
```shell
# Source Topic Produce
kafka-console-producer.sh \
	--bootstrap-server localhost:9092 \
	--topic sentences

# Target Topic Consume : Word-Count(Kafka Streams 결과)
kafka-console-consumer.sh \
    --bootstrap-server localhost:9092 \
    --from-beginning \
    --topic word-count \
    --property print.key=true \
    --property key.separator=" : " \
    --key-deserializer "org.apache.kafka.common.serialization.StringDeserializer" \
    --value-deserializer "org.apache.kafka.common.serialization.LongDeserializer" 
```