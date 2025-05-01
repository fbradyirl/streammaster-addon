# https://developers.home-assistant.io/docs/add-ons/configuration#add-on-dockerfile
ARG BUILD_FROM
FROM $BUILD_FROM

ENV POSTGRES_SET_PERMS=0

# Set labels
LABEL maintainer="fbradyirl@github.com"

# Set working directory
WORKDIR /config

COPY run.sh /run.sh
RUN chmod +x /run.sh
CMD [ "/run.sh" ]