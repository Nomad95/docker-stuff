```
docker run --rm -it -p 8080:8080 01056289375f3f6dce25ba47bf44b41950de484c16c17d01693d7fed76329edb #your image
```

run ruby app with two docker composes files - that will merge the two docker-composes. we need to restart container to see changes

```
docker-compose -f docker-compose.yml -f docker-compose-dev.yml up -d --force-recreate
```
