# Mongissimo

Mongissimo is a simple stack wich contains [MongoDB](https://www.mongodb.com) and [Mongo Express](https://github.com/mongo-express/mongo-express). It requires you have installed [Docker](https://www.docker.com). I highly recommend you [Docker Desktop](https://www.docker.com/products/docker-desktop).

## Up

The only thing you need to do is run one of the following two commands depending on if you prefer run it in the background or not:

```sh
docker compose -f docker-compose.yml up
```

### Running in the background
If you prefer to run it in the background:

```sh
docker compose -f docker-compose.yml up -d
```

### Customization

Probably you need to adapt this Stack to your specific case. With that in mind, I have several basic options as environment variables:

- MONGO_TAG (default: 3.6.23-xenial) - You can see all available versions in the [MongoDB's Docker Hub page](https://hub.docker.com/_/mongo).
- MONGO_ADMIN_USER (default: root)
- MONGO_ADMIN_PASS (default: secret)
- MONGO_PORT (default: 27017)
- MONGO_EXPRESS_PORT (default: 8081)

In order to use them, you must prepend the `key=value` pairs to the `up` command. For example:

```sh
MONGO_ADMIN_USER=admin MONGO_EXPRESS_PORT=8080 docker compose -f docker-compose.yml up -d
```

# Stop

In case you ran this stack on background or simply from another place, you may want to stop it. It is as simple as run the next command:

```sh
docker compose -f docker-compose.yml stop
```

### Remove

Maybe you prefer stop and remove it, in which case, you could run the next line:

```sh
docker compose -f docker-compose.yml down
```
