FROM node:lts-alpine3.20 AS Builder
WORKDIR /app
COPY ./package-lock.json .
COPY ./package.json .
RUN npm install
COPY . .
RUN npm run build

FROM nginx:latest AS Runner
COPY --from=Builder /app/dist /usr/share/nginx/html
COPY ./nginx.conf /etc/nginx/nginx.conf
EXPOSE 85
CMD ["nginx", "g", "daemon off;"]