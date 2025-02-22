FROM node:14-slim

WORKDIR /app

COPY portfolio_vue/package*.json ./
RUN npm install

COPY portfolio_vue/ .

EXPOSE 8080

CMD ["npm", "run", "serve"]
