FROM node:16

WORKDIR /usr/src
COPY . .

RUN npm install
RUN npm run build
RUN npm install -g serve

CMD ["serve", "-s", "-l", "5001", "build"]

EXPOSE 5001
