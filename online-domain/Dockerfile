FROM node:lts-alpine3.20 AS builder
WORKDIR /app
COPY ./package-lock.json .
COPY ./package.json .
RUN npm install
COPY . .
RUN npm run build

FROM nginx:latest AS runner
COPY --from=builder /app/dist /usr/share/nginx/html
COPY ./nginx.conf /etc/nginx/nginx.conf
EXPOSE 1-65535
CMD ["nginx", "-g", "daemon off;"]