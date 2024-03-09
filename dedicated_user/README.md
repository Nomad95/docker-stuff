# Running images with dedicated user

### USER

User instruction sets the user name (or UID) and optionally the user group (GID) to use when running the image and for any RUN, CMD and ENTRYPOINT instructuins that follow it in the dockerfile.
Also execing to container will give us the given user

Following will run with user 31337

```
docker build -t user-go .
docker run -it --name user-go -d  user-go

```

Using USER sets the same user and group for following CMD and ENTRYPOINT instructions.
Both Docker run and docker exec accept -u 0 param which allows yo switch back to the root account

Tools like gosu or su-exec, can make docker run the container entrypoint as root which drops the privilege when it is no longer needed

This will run the 'ps aux' with www-data but as a child process of root

```
docker run --rm my-ubuntu sudo -u www-data ps aux
```

use gosu instead

```
docker run --rm my-ubuntu gosu www-data ps aux
```
