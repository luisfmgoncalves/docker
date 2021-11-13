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

#### GUI
You can make use of the [OffsetExplorer](https://kafkatool.com/download.html) to set up a GUI for your Kafka server.
After download and install the offsetExplorer, Add a new connection in the OffsetExplorer by setting localhost:29092 (kafka host and port) to `Advanced -> Bootstrap servers`.
