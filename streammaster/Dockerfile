# https://developers.home-assistant.io/docs/add-ons/configuration#add-on-dockerfile
ARG BUILD_FROM
FROM $BUILD_FROM

ENV POSTGRES_SET_PERMS=0
ENV POSTGRES_HOST="homeassistant.local"
ENV POSTGRES_DB="postgres"
ENV POSTGRES_USER="postgres"
ENV POSTGRES_PASSWORD="homeassistant"
ENV POSTGRES_IS_LOCAL=0
ENV STREAMMASTER_BASEHOSTURL=http://0.0.0.0:7095

# That should short-circuit any PGAdmin creation logic that expects working credentials.
ENV PGADMIN_SETUP_EMAIL=disabled
ENV PGADMIN_SETUP_PASSWORD=disabled

# This sets a hard heap limit on the .NET GC to ~1GB.
ENV DOTNET_GCHeapHardLimit=1048576000

# Set labels
LABEL maintainer="fbradyirl@github.com"

