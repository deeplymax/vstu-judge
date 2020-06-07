FROM alpine:3.3

ENV GOPATH=/go PATH=/go/bin:$PATH

COPY . $GOPATH/src/github.com/deeplymax/vstu-judge-agent
WORKDIR $GOPATH/src/github.com/deeplymax/vstu-judge-agent

RUN apk add --no-cache git go && \
    go get -d                 && \
    apk del git               && \
    go install                && \
    apk del go                && \
    rm -rf "$GOPATH/pkg" "$GOPATH/src"

ONBUILD COPY vstu-judge-agent-configuration.json /agent/
WORKDIR /agent

CMD ["/go/bin/vstu-judge-agent"]
