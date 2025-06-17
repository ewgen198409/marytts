ARG BUILD_FROM
FROM $BUILD_FROM

# Устанавливаем нужные пакеты
RUN apk add --no-cache openjdk8 unzip curl bash

# Устанавливаем MaryTTS
WORKDIR /opt
RUN curl -L -o marytts.zip https://github.com/marytts/marytts/archive/refs/tags/v5.2.1.zip && \
    unzip marytts.zip && \
    rm marytts.zip && \
    chmod +x /opt/marytts-5.2.1/marytts-server


EXPOSE 59125

