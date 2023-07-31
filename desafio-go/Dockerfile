FROM golang:alpine AS builder
WORKDIR /go/src/github/diogorochaa
COPY hello.go hello.go
RUN go build -o /go/bin/hello hello.go

FROM scratch
COPY --from=builder /go/bin/hello /go/bin/hello
ENTRYPOINT ["/go/bin/hello"]
