FROM golang:1.23-alpine AS builder

WORKDIR /app

COPY main.go .

RUN go build -o hello-world main.go

FROM alpine:latest

WORKDIR /app

COPY --from=builder /app/hello-world .

CMD ["./hello-world"]