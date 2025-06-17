ARG BUILD_FROM
FROM $BUILD_FROM

# Устанавливаем нужные пакеты
RUN apk add --no-cache openjdk17-jre unzip curl bash

# Устанавливаем MaryTTS
WORKDIR /opt
RUN curl -L -o marytts.zip https://github.com/marytts/marytts/archive/refs/tags/v5.2.1.zip && \
    unzip marytts.zip && \
    rm marytts.zip && \
    
EXPOSE 59125

