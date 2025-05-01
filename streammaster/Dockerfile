# https://developers.home-assistant.io/docs/add-ons/configuration#add-on-dockerfile
ARG BUILD_FROM
FROM $BUILD_FROM

ENV POSTGRES_SET_PERMS=0
ENV POSTGRES_HOST="homeassistant.local:5432"
ENV POSTGRES_DB="postgres"
ENV POSTGRES_USER="postgres"
ENV POSTGRES_PASSWORD="homeassistant"
ENV POSTGRES_IS_LOCAL=0

# Set labels
LABEL maintainer="fbradyirl@github.com"

# Set working directory
WORKDIR /config

COPY run.sh /run.sh
RUN chmod +x /run.sh
CMD [ "/run.sh" ]