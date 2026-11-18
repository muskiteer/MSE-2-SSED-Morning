FROM node:22-alpine

WORKDIR /app

COPY package.json ./

RUN npm install --omit=dev && npm cache clean --force

COPY src/ ./src/
COPY db/ ./db/

ENV PORT=3000 \
    NODE_ENV=production

EXPOSE 3000

USER node

CMD ["node", "src/server.js"]
