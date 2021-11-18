### Run container
Spin up the docker container
```
docker-compose up -d
```

Test the connection of zookeeper and kafka respectively
```
nc -z localhost 22181
nc -z localhost 19092
```

#### Usage
Use [Conduktor](https://www.conduktor.io/) to send messages to topics