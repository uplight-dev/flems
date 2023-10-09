#FROM node:latest as build
#FROM nginx:alpine
FROM hoosin/alpine-nginx-nodejs:latest

RUN apk add git

WORKDIR /usr/src/flems

RUN git clone https://github.com/porsager/flems.git . && \
    npm install ;\
    npm run build

COPY . .

RUN cp -R /usr/src/flems/dist/* /usr/share/nginx/html && \
cp ./index.html /usr/share/nginx/html/
