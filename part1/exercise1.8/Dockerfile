FROM ubuntu:18.04

WORKDIR /usr/src/app

COPY read_website.sh .

RUN chmod +x read_website.sh

RUN apt update; apt install curl -y;

CMD ./read_website.sh
