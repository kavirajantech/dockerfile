FROM node:12.11.1 AS builder
MAINTAINER Kavirajan ST kavirajantech@gmail.com
WORKDIR /app
COPY . ./
RUN yarn
RUN yarn build

# For the production environment COPY to Nginx webserver document root
FROM nginx:alpine
COPY nginx.conf /etc/nginx/conf.d/default.conf
COPY --from=builder /app/build /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
