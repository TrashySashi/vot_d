FROM node:25-alpine AS builder

WORKDIR /app

COPY package*.json .

RUN npm ci

COPY . .

ENV NODE_ENV=production
ENV PORT=3000
ENV HOSTNAME=0.0.0.0

EXPOSE 3000

CMD ["node","index.js"]