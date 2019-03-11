# Flyway - Getting Started

## 참고
[Flyway - Getting Started](https://dev.to/drminnaar/flyway---getting-started-3emm)

## volume issue 처리

volume 생성
```
docker volume create --name postgresql-volume -d local
```

volumes 부분 참고
```
version: '2'

services:

  postgres:
    image: postgres
    volumes:
      -  postgresql-volume:/var/lib/postgresql/data
    environment:
      - POSTGRES_PASSWORD=rw_dev
      - POSTGRES_USER=rw_dev
      - POSTGRES_DB=rw_development
    ports:
      - "5432:5432"

  redis:
    image: redis
    ports:
      - "6379:6379"

volumes:
    postgresql-volume:
      external: true
```

참고 : [Run PostgreSQL using Docker with persistent data on Windows 10](http://www.lukaszewczak.com/2016/09/run-postgresql-using-docker-with.html)
