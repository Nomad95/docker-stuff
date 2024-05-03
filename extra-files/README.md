# Unnecessary files left in the image

### git

Even that we are removing .git directory in the dockerfile with RUN. The .git directory is still a part of a image

To see files that are a part of image do either of those:

```
1. docker inspect -f '{{.GraphDriver.Data.LowerDir}}' c365 | tr ':' '\n'

2. docker save extra-files | tar xv -C ./image
2.1. Check manifest.json to check the order of layers

3. docker run --rm -it -v /var/run/docker.sock:/var/run/docker.sock  wagoodman/dive extra-files

```

To fix this, use .dockerignore
