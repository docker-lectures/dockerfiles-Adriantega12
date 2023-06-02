FROM golang AS builder

COPY . .

RUN go build dispatcher.go

FROM alpine

COPY --from=builder /go/dispatcher .

CMD ["./dispatcher"]

EXPOSE 80