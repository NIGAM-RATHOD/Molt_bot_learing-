# Data Engineering Skill

ETL pipelines, data warehousing, and real-time streaming.

## Data Pipeline Architecture

### ETL Pattern
```
Extract → Transform → Load
Sources → Processing → Storage
```

### Tools
| Layer | Technology |
|-------|-----------|
| Collection | Kafka, Kinesis, SQS |
| Processing | Spark, Flink, Pandas |
| Storage | S3, Delta, Iceberg |
| Warehouse | Snowflake, BigQuery, Redshift |
| Orchestration | Airflow, Dagster, Prefect |

## Real-time Streaming

### Apache Kafka
```python
from kafka import KafkaProducer, KafkaConsumer

producer = KafkaProducer(bootstrap_servers='localhost:9092')
producer.send('trades', b'BTC at 68000')

consumer = KafkaConsumer('trades', bootstrap_servers='localhost:9092')
for msg in consumer:
    print(msg.value)
```

### Apache Spark Streaming
```python
from pyspark.sql import SparkSession

spark = SparkSession.builder.appName("Trading").getOrCreate()
df = spark.readStream.format("kafka").option("subscribe", "trades").load()
```

## Data Warehousing

### Snowflake
```sql
CREATE TABLE trades (
    symbol VARCHAR(10),
    price DECIMAL(18,8),
    volume DECIMAL(18,8),
    timestamp TIMESTAMP
);
```

### BigQuery
```sql
SELECT symbol, AVG(price) as avg_price
FROM `project.dataset.trades`
WHERE timestamp > TIMESTAMP_SUB(CURRENT_TIMESTAMP(), INTERVAL 1 DAY)
GROUP BY symbol
```

## Commands

- `/etl` - Design ETL pipeline
- `/stream` - Real-time setup
- `/warehouse` - Data warehouse design
- `/pipeline` - Data pipeline
