
FROM alpine:3.7

ENV HOST="0.0.0.0"
ENV PORT="8080"
ENV NAME="request"

RUN apk add --no-cache ca-certificates

WORKDIR /


RUN wget https://github.com/evildecay/etcdkeeper/releases/download/0.6.6/etcdkeeper3-v0.6.6-linux_x86_64.tar.gz \
    && tar xzvf etcdkeeper3-v0.6.6-linux_x86_64.tar.gz


EXPOSE ${PORT}

ENTRYPOINT ./etcdkeeper/etcdkeeper -h $HOST -p $PORT -n $NAME