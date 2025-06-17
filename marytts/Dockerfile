ARG BUILD_FROM
FROM $BUILD_FROM

# Устанавливаем нужные пакеты
RUN apk add --no-cache openjdk8 unzip curl bash

# Устанавливаем MaryTTS
WORKDIR /opt
RUN curl -L -o marytts.zip https://github.com/marytts/marytts/releases/download/v5.2/marytts-5.2.1.zip && \
    unzip marytts.zip && \
    rm marytts.zip && \
    chmod +x /opt/marytts-5.2/marytts-server

# Копируем скрипт запуска
COPY run.sh /run.sh
RUN chmod a+x /run.sh

EXPOSE 59125

CMD [ "/run.sh" ]
