### Run container
Spin up the docker container
```
docker-compose up -d
```

#### GUI
Once the ActiveMQ container is running, the ActiveMQ broker manager is accessible at [http://localhost:8161/admin](http://localhost:8161/admin). Sign in with `admin:admin`.  

To publish a eventMessage to a specific topic, you can either use the manager or do the following post request which automatically creates a topic on ActiveMQ for which this application listens to:  
`
curl -X POST 'http://admin:admin@localhost:8161/api/eventMessage?destination=topic://<topic-name>' --header 'Content-Type: application/json' -d '{<message_body>}'
`
