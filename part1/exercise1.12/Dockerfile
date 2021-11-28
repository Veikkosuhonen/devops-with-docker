FROM ubuntu

WORKDIR /usr/src/app

RUN apt-get update;apt-get install curl -y

RUN curl -sL https://deb.nodesource.com/setup_14.x | bash
RUN apt-get install -y nodejs

COPY . .

RUN npm install

RUN npm run build

RUN npm install serve

RUN npm install --global yarn

RUN yarn global add serve

EXPOSE 5000

CMD ["serve", "-s", "-l", "5000", "build"]
