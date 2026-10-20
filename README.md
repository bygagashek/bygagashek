### Pavel Makarov — PHP backend developer

I build and maintain the backend of a large SaaS product: sharded MariaDB, background jobs,
payment and messaging integrations, Docker-based infrastructure and monitoring.

**Stack:** PHP · Laravel · Symfony · RabbitMQ · Kafka · MariaDB / MySQL · PostgreSQL · Redis · nginx + php-fpm · Docker · Prometheus + Grafana · Linux · GitLab CI

#### Projects

| | |
|---|---|
| [**event-ledger**](https://github.com/bygagashek/event-ledger) | Symfony 7.4 + PostgreSQL + Kafka account ledger: row-locked writes with idempotency keys, transactional outbox, single relay via advisory lock, per-account ordering, projection that drops duplicates and stops on gaps. |
| [**notification-hub**](https://github.com/bygagashek/notification-hub) | Laravel 12 + RabbitMQ message delivery: transactional outbox, publisher confirms, TTL retry queues, dead-lettering, idempotent consumer. |
| [**php-infra-stack**](https://github.com/bygagashek/php-infra-stack) | nginx → php-fpm → MariaDB primary with a GTID replica, Redis, Prometheus + Grafana with alerts. One `docker compose up`, end-to-end smoke test in CI. |
| [**booking-api**](https://github.com/bygagashek/booking-api) | Table booking API: idempotency keys, row locking against double booking, HMAC-signed payment webhooks with replay protection. |
| [**php-shard-router**](https://github.com/bygagashek/php-shard-router) | Routing PDO connections across shards: consistent hashing, replica failover, read-your-writes, transaction retries on deadlock. |

Each project has tests and static analysis running in GitHub Actions.
