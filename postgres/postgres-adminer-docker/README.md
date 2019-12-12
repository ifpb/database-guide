# Postgres + Adminer

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

- [https://hub.docker.com/_/adminer](https://hub.docker.com/_/adminer)
- [https://hub.docker.com/_/postgres](https://hub.docker.com/_/postgres)