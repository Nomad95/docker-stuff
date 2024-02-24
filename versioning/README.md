Parameterize compose file

### Show result file

```
VERSION=1.19 docker-compose config
```

Can also read system env values

### Set variable to .env file

```
echo VERSION=1.18 > .env
```

Now compose will fill the values from .env file.
Value from command line has a priority

### Build from dockerfile with arguments

```
docker build --build-arg VERSION=1.19 .
```
