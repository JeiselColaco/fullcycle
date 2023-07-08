FROM golang:1.20 AS builder

WORKDIR /usr/go/src
COPY . .
RUN go build main.go


FROM  scratch
WORKDIR /usr/go/app
COPY --from=builder /usr/go/src/main .
CMD ["./main"]