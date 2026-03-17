FROM node:latest AS base

WORKDIR /app

COPY package.json .

RUN npm install

ARG VITE_BASE_API

COPY . .

CMD ["npm", "run", "dev"]
#RUN npm run build


#FROM nginx:alpine 

#COPY --from=base /app/dist /usr/share/nginx/html
