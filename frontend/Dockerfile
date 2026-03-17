FROM node:latest AS base

WORKDIR /app

COPY package.json .

RUN npm install

ARG VITE_BASE_API

COPY . .

RUN npm run build


FROM nginx:alpine 

COPY --FROM=base /app/dist /usr/share/nginx/html
