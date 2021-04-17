# Docker Compose `depends_on` examples

`depends_on` can be used in the following formats.

- List
- Object

## List

```bash
depends_on:
  - service_a
```

- `docker-compose.list-chained.yml`
- `docker-compose.list-simple.yml`

## Object

### `service_started`

```bash
depends_on:
  service_a:
    condition: service_started
```

- `docker-compose.object-service_started-problematic.yml`
- `docker-compose.object-service_started.yml`

### `service_healthy`

```bash
depends_on:
  service_a:
    condition: service_healthy
```

- `docker-compose.object-service_healthy-failure.yml`
- `docker-compose.object-service_healthy.yml`

### `service_completed_successfully`

```bash
depends_on:
  service_a:
    condition: service_completed_successfully
```

- `docker-compose.object-service_completed_successfully-failure.yml`
- `docker-compose.object-service_completed_successfully.yml`

## Links

- Japanese post: [Docker Compose の depends_on の使い方まとめ | gotohayato.com](https://gotohayato.com/content/533/)
