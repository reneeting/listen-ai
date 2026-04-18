FROM golang:1.23-alpine AS builder
WORKDIR /app
COPY . .
RUN go build -o stat-service .

FROM alpine:latest
WORKDIR /app
COPY --from=builder /app/stat-service .

EXPOSE 8002

CMD ["./stat-service"]