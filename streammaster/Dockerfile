# https://developers.home-assistant.io/docs/add-ons/configuration#add-on-dockerfile
ARG BUILD_FROM
FROM $BUILD_FROM

ENV POSTGRES_SET_PERMS=0
ENV POSTGRES_HOST="homeassistant.local"
ENV POSTGRES_DB="postgres"
ENV POSTGRES_USER="postgres"
ENV POSTGRES_PASSWORD="homeassistant"
ENV POSTGRES_IS_LOCAL=0
# ENV STREAMMASTER_BASEHOSTURL=http://0.0.0.0:7095
# ENV STREAMMASTER_BASEHOSTURL=http://0.0.0.0:7095/api/hassio_ingress/e517628b_streammaster
# ENV PATH_BASE=/api/hassio_ingress/e517628b_streammaster

# Set labels
LABEL maintainer="fbradyirl@github.com"

