FROM node:12-alpine

RUN apk update
RUN npm install -g yarn@^1

RUN mkdir /app
WORKDIR /app

COPY package.json *yarn* ./
RUN yarn install

COPY . .

EXPOSE 3000

# TODO: Only for development
CMD yarn nuxt -PORT=3000 -HOST=0.0.0.0
