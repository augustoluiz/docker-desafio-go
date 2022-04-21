from golang:alpine3.15 AS builder

WORKDIR /usr/src/app
COPY hello.go /usr/src/app

RUN go build hello.go

from hello-world:latest
WORKDIR /usr/src/app
COPY --from=builder /usr/src/app .

ENTRYPOINT ["./hello"]