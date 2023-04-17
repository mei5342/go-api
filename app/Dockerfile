FROM golang:1.20.3

ENV ROOT=/usr/src/app
ENV CGO_ENABLED 0
WORKDIR ${ROOT}

RUN apt-get update
COPY go.mod go.sum ./
RUN go mod download
EXPOSE 8080

CMD ["go", "run", "main.go"]