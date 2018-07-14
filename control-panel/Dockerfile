ARG BUILD_FROM=hassioaddons/base:2.0.1
# hadolint ignore=DL3006
FROM ${BUILD_FROM}

# Setup base
RUN \
    apk add --no-cache \
        nginx=1.14.0-r0

# Copy root filesystem
COPY rootfs /

# Build arugments
ARG BUILD_ARCH
ARG BUILD_DATE
ARG BUILD_REF
ARG BUILD_VERSION

# Labels
LABEL \
    io.hass.name="Home Assistant Control Panel" \
    io.hass.description="Simple to use control panel for the ultimate home automation setup" \
    io.hass.arch="${BUILD_ARCH}" \
    io.hass.type="addon" \
    io.hass.version=${BUILD_VERSION} \
    maintainer="Franck Nijhof <frenck@addons.community>" \
    org.label-schema.description="Simple to use control panel for the ultimate home automation setup" \
    org.label-schema.build-date=${BUILD_DATE} \
    org.label-schema.name="Home Assistant Control Panel" \
    org.label-schema.schema-version="1.0" \
    org.label-schema.url="https://community.home-assistant.io/t/community-hass-io-add-on-home-assistant-control-panel/49634?u=frenck" \
    org.label-schema.usage="https://github.com/hassio-addons/addon-control-panel/tree/master/README.md" \
    org.label-schema.vcs-ref=${BUILD_REF} \
    org.label-schema.vcs-url="https://github.com/hassio-addons/addon-control-panel" \
    org.label-schema.vendor="Community Hass.io Addons"
