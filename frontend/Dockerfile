FROM node:18.20.8-bullseye-slim
WORKDIR /app
COPY package.json yarn.lock ./
RUN corepack enable && yarn install --frozen-lockfile
COPY . .
ARG API_URL
ENV API_URL $API_URL
CMD ["yarn", "dev"]
