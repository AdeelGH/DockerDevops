FROM ubuntu:22.04

WORKDIR /usr/src/app

COPY script.sh .

RUN chmod +x script.sh

RUN apt-get update

RUN apt-get -y install curl

ENTRYPOINT ["./script.sh"]
