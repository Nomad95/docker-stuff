FROM golang:1.16-buster AS build
CMD ["/app/app"]
EXPOSE 8080/tcp
WORKDIR /app
COPY . .
RUN go mod download && \
    go build -v -o app

FROM debian:buster
CMD ["gosu", "31337", "/app"]
EXPOSE 8080/tcp
RUN apt-get update && apt-get install -y gosu
COPY --from=build /app/app /app
