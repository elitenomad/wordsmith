FROM golang:alpine
WORKDIR /web
COPY dispatcher.go .
RUN go build dispatcher.go
CMD ["./dispatcher"]