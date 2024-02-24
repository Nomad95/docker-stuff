# Resources

### add resource constraint

```
docker run --memory="2.5g" --cpus="1.5" <image>
docker update --memory="2.5g" --cpus="1.5" <container>
```

### Check container available memory

```
docker run --rm -m 1g -it  alpine:3 cat /sys/fs/cgroup/memory/memory.limit_in_bytes
```

### Smash some data into shared memory to see that we lack space

```
docker run --rm -m 1g -it  alpine:3 sh -c 'cat /dev/urandom > /dev/shm/abc'
```

Docker's OOM killer kills the container

### asign 0.5 cores to container

```
docker run --rm --cpus=0.5 -d  alpine:3 dd if=/dev/zero of=/dev/null
docker stats
```
