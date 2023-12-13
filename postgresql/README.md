Run specific service from compose file
Here CLI goes straight to the psql command line
Same for the "dump"

```
docker-compose -f docker-compose.yaml -f docker-compose-dev.yaml run cli
```

To run adminer

```
docker-compose -f docker-compose.yaml -f docker-compose-dev.yaml up -d adminer
```
