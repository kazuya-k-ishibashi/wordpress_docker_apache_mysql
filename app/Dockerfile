FROM wordpress

ARG HOST_GID
ARG HOST_UID

RUN groupmod -g ${HOST_GID} www-data \
  && usermod -u ${HOST_UID} www-data \
  && chown -R www-data:www-data /usr/src/wordpress

