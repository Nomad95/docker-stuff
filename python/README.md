app needs to listen on all interfaces so the hostName must be 0.0.0.0

```
docker run --rm -it -v $(pwd):/app -w /app -p 8080:8080 python:3-buster python app.py
```

flask app

```
docker run --rm -it -p 8080:8080 52c9b8bbb10b6204d3dfe5c83018cf8cbecd2554423828e02d3380be4ad3742c //image name
```

run flask app with two docker composes files - that will merge the two docker-composes
with volumes in -dev.yml we can make changes to the file without restarting container

```
docker-compose -f docker-compose.yml -f docker-compose-dev.yml up -d
```
