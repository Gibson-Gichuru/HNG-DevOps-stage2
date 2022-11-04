FROM node as build-step

WORKDIR /app

ENV PATH /app/node_modules/.bin:$PATH

COPY ./package.json ./


COPY ./src ./src

COPY ./public ./public

RUN npm install

RUN npm run build


FROM nginx:stable-alpine

COPY --from=build-step /app/build /usr/share/nginx/html
