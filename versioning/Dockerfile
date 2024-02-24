ARG VERSION=default
# it is a build argument that has to be passed
FROM nginx:${VERSION}
# ARGs are deleted after FROM statement
ARG VERSION
# to see the version inside container env vars
ENV DOCKER_BUILD_VERSION=${VERSION}