# System Design Skill

Design scalable, reliable, and maintainable systems.

## Design Principles

### CAP Theorem
- **C**onsistency: All nodes see same data
- **A**vailability: Every request gets response
- **P**artition tolerance: System works despite network failures

Trade-off: CA (databases), CP (ZK, etcd), AP (Cassandra)

### Scalability Patterns
- Horizontal scaling (add nodes)
- Vertical scaling (bigger nodes)
- Caching (Redis, CDN)
- Load balancing (round-robin, least connections)
- Database sharding
- Read replicas

## Architecture Patterns

### Microservices
```
API Gateway → Service A
          → Service B
          → Service C
          → Auth Service
```

- Pros: Scalability, team autonomy
- Cons: Complexity, distributed debugging

### Event-Driven
```
Producer → Event Bus → Consumer A
                     → Consumer B
                     → Consumer C
```

- Async processing
- Loose coupling
- Replay capability

### Serverless
- Functions: Lambda, Cloud Functions
- Event triggers
- Pay per use
- Cold start considerations

## System Components

| Component | Options |
|-----------|---------|
| Cache | Redis, Memcached |
| Message Queue | RabbitMQ, Kafka, SQS |
| Database | PostgreSQL, MongoDB, DynamoDB |
| Search | Elasticsearch, Algolia |
| CDN | CloudFront, Fastly |
| Rate Limit | Redis, token bucket |

## Trade-off Analysis

```
Question: Should we use SQL or NoSQL?

SQL when:
- ACID transactions needed
- Complex joins
- Structured data

NoSQL when:
- Massive scale
- Flexible schema
- Eventual consistency OK
```

## Commands

- `/design` - System design
- `/scale` - Scalability approach
- `/arch` - Architecture review
- `/bottleneck` - Find bottlenecks
