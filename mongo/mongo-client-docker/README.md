# Mongo Client (Mongo)

## Code

---

> [docker-compose.yml](docker-compose.yml):

```yaml
{% include_relative docker-compose.yml %}
```

> [.env](.env):

```
{% include_relative .env %}
```

> Load database:

```
$ docker-compose up -d
$ docker-compose ps   
    Name                   Command               State            Ports          
---------------------------------------------------------------------------------
mongo           docker-entrypoint.sh mongod      Up      0.0.0.0:27017->27017/tcp
```

## Commands

---

> `mongo -u <username> -p <password>`:

```
docker-compose exec mongo mongo -u root -p secret
MongoDB shell version v4.2.1
connecting to: mongodb://127.0.0.1:27017/?compressors=disabled&gssapiServiceName=mongodb
Implicit session: session { "id" : UUID("87f8d652-3723-40c6-8540-13fc32a1e6b8") }
MongoDB server version: 4.2.1
Welcome to the MongoDB shell.
For interactive help, type "help".
For more comprehensive documentation, see
        http://docs.mongodb.org/
Questions? Try the support group
        http://groups.google.com/group/mongodb-user
Server has startup warnings: 
2019-12-12T23:02:47.146+0000 I  STORAGE  [initandlisten] 
2019-12-12T23:02:47.146+0000 I  STORAGE  [initandlisten] ** WARNING: Using the XFS filesystem is strongly recommended with the WiredTiger storage engine
2019-12-12T23:02:47.147+0000 I  STORAGE  [initandlisten] **          See http://dochub.mongodb.org/core/prodnotes-filesystem
---
Enable MongoDB's free cloud-based monitoring service, which will then receive and display
metrics about your deployment (disk utilization, CPU, operation statistics, etc).

The monitoring data will be available on a MongoDB website with a unique URL accessible to you
and anyone you share the URL with. MongoDB may use this information to make product
improvements and to suggest MongoDB products and deployment options to you.

To enable free monitoring, run the following command: db.enableFreeMonitoring()
To permanently disable this reminder, run the following command: db.disableFreeMonitoring()
---

> 
```

> `show dbs`:

```
> show dbs
admin   0.000GB
config  0.000GB
local   0.000GB
```

> `db.collection.save()`:

```
> db.people.save({ name: "Luiz Chaves", email: "luiz.chaves@ifpb.edu.br" })
WriteResult({ "nInserted" : 1 })
```

> `db.collection.find()`:

```
> db.people.find()
{ "_id" : ObjectId("5df2c8288b40815884ab3410"), "name" : "Luiz Chaves", "email" : "luiz.chaves@ifpb.edu.br" }
```

> `exit`:

```
> exit
```

## References

---

- Mongo
  - [Shell Quick Reference](https://docs.mongodb.com/manual/reference/mongo-shell/)
- Docker
  - [https://hub.docker.com/\_/mongo](https://hub.docker.com/_/mongo)
- Cheat Sheet
  - [bradtraversy/mongodb_cheat_sheet.md](https://gist.github.com/bradtraversy/f407d642bdc3b31681bc7e56d95485b6)
  - [SQL to MongoDB Mapping Chart](https://gist.github.com/aponxi/4380516)
- [10 Most Common Commands for MongoDB Beginners](https://dzone.com/articles/top-10-most-common-commands-for-beginners)
  