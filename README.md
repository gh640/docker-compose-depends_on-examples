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

- [`compose-spec/spec.md` at master · `compose-spec/compose-spec` · GitHub](https://github.com/compose-spec/compose-spec/blob/master/spec.md#depends_on)
- [`depends_on` | Compose file version 3 reference | Docker Documentation](https://docs.docker.com/compose/compose-file/compose-file-v3/#depends_on)
- [`depends_on` | Compose file version 2 reference | Docker Documentation](https://docs.docker.com/compose/compose-file/compose-file-v2/#depends_on)
- Japanese post: [Docker Compose の depends_on の使い方まとめ | gotohayato.com](https://gotohayato.com/content/533/)
