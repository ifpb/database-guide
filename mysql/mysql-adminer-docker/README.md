# MySQL + Adminer

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
$ docker-compose exec mysql mysql -u root -p
# 
```

## References

---

- [https://hub.docker.com/_/adminer](https://hub.docker.com/_/adminer)
- [https://hub.docker.com/_/mysql](https://hub.docker.com/_/mysql)