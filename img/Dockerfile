FROM alpine:3.20
RUN apk add --no-cache curl
RUN head -c 50000000 /dev/urandom > /blob && sha256sum /blob > /blob.sha
COPY hello.txt /hello.txt
