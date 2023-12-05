run hello world:

```
docker run --rm -it -v $(pwd):/app -w /app node:15-buster node simple.js
```

run app:

```
docker build .
docker run -it --rm -p 8080:8080 27ffdc3b720b690a03f4d248c3ffe702ef1b8e767011a1d3c00c72b01fac4723 # your image name
```

compose:

```
docker-compose -f docker-compose.yml -f docker-compose-dev.yml up -d --force-recreate
```
