FROM golang:1.13 as builder

RUN go get -u google.golang.org/grpc/examples/helloworld/greeter_server

FROM debian

COPY --from=builder /go/bin/greeter_server /bin

ENTRYPOINT ["/bin/greeter_server"]