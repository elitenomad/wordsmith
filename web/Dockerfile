FROM golang:alpine
WORKDIR /web
COPY dispatcher.go .
RUN go build dispatcher.go
FROM alpine
COPY --from=0 /web/dispatcher .
CMD ["./dispatcher"]