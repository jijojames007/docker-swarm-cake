FROM nginx:alpine
WORKDIR /var/www/myapp
COPY cakephp .
RUN rm -rf /etc/nginx/conf.d/default.conf
COPY nginx.conf /etc/nginx/conf.d/default.conf
EXPOSE 80
