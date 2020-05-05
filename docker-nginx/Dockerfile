# Base docker image. References:
#   - https://hub.docker.com/_/nginx
#   - https://github.com/docker-library/docs/blob/master/php/README.md#supported-tags-and-respective-dockerfile-links
#   - http://geekyplatypus.com/dockerise-your-php-application-with-nginx-and-php7-fpm/

# Nginx 1.17 under debian buster-slim
FROM nginx:1.17

# To be able to install other packages in this container
RUN apt-get update

# To be sure that other containers are visible to this one (dev only)
RUN apt-get install -y iputils-ping