FROM node:0-wheezy

ENV DB mongodb://localhost/beyondpad

EXPOSE 8080

RUN apt-get update && apt-get install -y make g++ gcc build-essential libkrb5-dev python openssl && apt-get clean

RUN cd /root && \
git clone https://github.com/artursgirons/beyondpad.git && \
cd beyondpad && \
npm install

CMD ["node", "/root/beyondpad/server.js"]