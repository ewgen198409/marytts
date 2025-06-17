ARG BUILD_FROM
FROM $BUILD_FROM AS BUILD

FROM openjdk:8-jdk

WORKDIR /opt/marytts

# Копируем все необходимые файлы (допустим, ты положил дистрибутив в папку build)
COPY marytts-5.2.zip .
COPY run.sh /run.sh

RUN apt-get update && apt-get install -y unzip && \
    unzip marytts-5.2.zip && \
    chmod +x /run.sh

EXPOSE 59125

CMD ["/run.sh"]