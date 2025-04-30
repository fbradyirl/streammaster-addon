# https://developers.home-assistant.io/docs/add-ons/configuration#add-on-dockerfile
ARG BUILD_FROM
FROM $BUILD_FROM

# Set labels
LABEL maintainer="yourname@example.com"

# Pull the existing StreamMaster image content
COPY --from=ghcr.io/carlreid/streammaster:latest / / 

# Set working directory
WORKDIR /config

# Expose the web UI port
EXPOSE 7095

# Command to run
CMD [ "/init" ]