FROM node:22-alpine

WORKDIR /app

# Adjust this line
COPY package*.json ./

ENV NODE_OPTIONS="--openssl-legacy-provider"

RUN npm install

COPY . .

EXPOSE 3000

CMD ["npm", "start"]