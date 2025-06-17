ARG BUILD_FROM
FROM $BUILD_FROM AS BUILD


RUN apk add --no-cache openjdk17-jre unzip curl bash

ENV MARYTTS_VERSION 5.2
RUN wget -q --show-progress "https://github.com/marytts/marytts/releases/download/v${MARYTTS_VERSION}/marytts-${MARYTTS_VERSION}.zip" &&\
    unzip marytts-${MARYTTS_VERSION}.zip -d / && mv /marytts-${MARYTTS_VERSION} /app

FROM $BUILD_FROM AS RUNNING


#Used for the voice pack downloads
ENV MARYTTS_VERSION 5.2

COPY --from=BUILD /app /app

ENTRYPOINT [ "/init" ]
CMD []
COPY root /

