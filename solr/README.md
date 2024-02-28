# Solr

### run solr and add core and example data

```
docker run -d -it --name solr -p 8983:8983 solr:8.9
docker exec -it -u solr solr bin/solr create_core -c masters
docker exec -it -u solr solr bin/post -c masters example/exampledocs/manufacturers.xml
```
