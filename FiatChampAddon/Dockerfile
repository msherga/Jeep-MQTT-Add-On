# BUILD IMAGE
ARG BUILD_FROM
FROM $BUILD_FROM

RUN apk add icu-libs
RUN apk add icu

COPY run.sh /run.sh
RUN chmod a+x /run.sh

COPY FiatClient/build/ /build/.
RUN chmod +x /build/FiatChamp

LABEL org.opencontainers.image.source https://github.com/wubbl0rz/FiatChamp

CMD [ "/run.sh" ]
