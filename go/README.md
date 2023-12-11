run app:

```
docker run --rm -it -v $(pwd):/app -w /app golang:1.16-buster go mod init hello # init go dependencies
docker build .
docker run -it --rm -p 8080:8080 ec6ddd44c800f1c1e31f81d253eb4c06fca3c11b4eb9ebcf3c28df88115e201e  # your image name
```

compose:

```
docker-compose -f docker-compose.yml -f docker-compose-dev.yml up -d --force-recreate
```
