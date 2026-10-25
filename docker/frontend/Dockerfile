FROM node:20-alpine
WORKDIR /app
RUN apk add --no-cache libc6-compat
COPY package.json yarn.lock* ./
RUN yarn install --immutable
COPY . .
RUN chmod +x ./scripts/start.sh
EXPOSE 3000
CMD ["./scripts/start.sh"]
