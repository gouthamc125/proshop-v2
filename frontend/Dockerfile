FROM node:16-alpine

WORKDIR /app

COPY package.json package-lock.json ./

RUN npm install

RUN npx update-browserslist-db@latest

COPY . .

RUN npm run build

EXPOSE 3000

CMD [ "npm", "start" ]