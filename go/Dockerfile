FROM golang:1.16-buster AS build
WORKDIR /app
COPY . .
RUN go mod download && \
    go build -v -o app

#create multistage build as our docker image is too big

FROM debian:buster
CMD ["/app"]
EXPOSE 8080/tcp
#copy our built app to the /app in final debian image
COPY --from=build /app/app /app     