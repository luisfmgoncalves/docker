## docker-compose.yml
Starts a single node elasticsearch cluster and a kibana instance
```
docker-compose up
```
______________________________________________

## docker-compose-xpack.yml
Starts a single node elasticsearch cluster, a kibana and a logstash instance with xpack feature enabled

### Generate passwords for default users (one time action)
Start the elasticsearch:
```
docker-compose -f docker-compose-xpack.yml up -d elasticsearch
```
Access the container:
```
docker-compose -f docker-compose-xpack.yml exec elasticsearch bash
```
Generate passwords for default users:
```
bin/elasticsearch-setup-passwords interactive
```

Start the kibana:
```
docker-compose -f docker-compose-xpack.yml up -d kibana
```

Start the logstash:
```
docker-compose -f docker-compose-xpack.yml up -d logstash
```
The logstash pipeline imports data from [CoinGecko](https://www.coingecko.com/en/api)

NOTE:  
The setup of the passwords for the default users just needs to be done once.
Once the passwords have been generated, you can run the entire stack with:
```
docker-compose -f docker-compose-xpack.yml up
```
______________________________________________