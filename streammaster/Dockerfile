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

# This sets a hard heap limit on the .NET GC
ENV DOTNET_GCHeapHardLimit=734003200  # 700 MB

# This tells .NET to self-limit based on system memory and GC load.
ENV DOTNET_GCHeapHardLimitPercent=25
ENV DOTNET_GCTotalMemoryThreshold=700000000
# disabling server-mode GC, which allocates more memory for parallel collections:
ENV DOTNET_gcServer=false

USER root

RUN apt-get update && \
    apt-get install -y procps curl htop less && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Set labels
LABEL maintainer="fbradyirl@github.com"

