FROM golang:1.17

WORKDIR /go/src/app

COPY *.go .

RUN go mod init dispatch && go get
RUN go install

COPY newrelic.yml /go/src/app

CMD dispatch
