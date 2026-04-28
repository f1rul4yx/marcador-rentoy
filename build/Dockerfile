FROM node:20-alpine

WORKDIR /app

COPY package.json ./
RUN npm install --production

COPY src/ ./src/
COPY public/ ./public/

COPY docker-entrypoint.sh /docker-entrypoint.sh
RUN chmod +x /docker-entrypoint.sh

EXPOSE 3000

ENV NODE_ENV=production
ENV PORT=3000
ENV TZ=Europe/Madrid

ENTRYPOINT ["/docker-entrypoint.sh"]
CMD ["node", "src/server.js"]
