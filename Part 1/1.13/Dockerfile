FROM golang:1.16
ENV PORT=8080
WORKDIR /usr/src/app

COPY go.mod go.sum ./
RUN go mod download && go mod verify

COPY . .
RUN go build 

EXPOSE $PORT

CMD ./server
