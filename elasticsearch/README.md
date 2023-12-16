run ealstic alone

```
docker run -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" elasticsearch:7.12.0
```

add value via http

```
curl -H 'Content-Type: application/json' -XPOST -d '{"field":"value"}' http://localhost:9200/docker-masters/log/key1
```
