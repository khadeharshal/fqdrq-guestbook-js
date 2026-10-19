FROM node:20-alpine

WORKDIR /app

COPY node_modules ./node_modules
COPY package*.json ./
COPY server.js ./
COPY public ./public/

RUN addgroup -S -g 1001 nodejs && \
    adduser -S -u 1001 -G nodejs nodeuser && \
    chown -R nodeuser:nodejs /app

USER nodeuser

EXPOSE 3000
CMD ["node", "server.js"]
