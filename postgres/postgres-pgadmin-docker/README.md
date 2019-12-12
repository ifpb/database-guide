# Postgres + pgAdmin4

## Code

---

```yaml
{% include_relative docker-compose.yml %}
```

```
{% include_relative .env %}
```

## Commands

---

```
$ docker-compose up -d
$ docker-compose ps
```

```
$ docker-compose exec pg psql -h pg -U postgres
# 
```

## References

---

- [https://hub.docker.com/_/postgres](https://hub.docker.com/_/postgres)
- [https://hub.docker.com/r/dpage/pgadmin4/](https://hub.docker.com/r/dpage/pgadmin4/)