FROM nginx:1.17-alpine

ARG user
ARG uid

# Copy nginx conf
COPY ./.docker/nginx/conf.d/app.conf /etc/nginx/conf.d/default.conf

# Add user
RUN adduser -G www-data -G root -u $uid -H -D $user

WORKDIR /var/www
RUN chown -R www:www-data /var/www
RUN chmod -R ug+rw /var/www 