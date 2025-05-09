ARG BUILD_FROM
FROM $BUILD_FROM

RUN apk add icu-libs icu dotnet-sdk-7.0

WORKDIR /src
COPY FiatClient/ .

RUN dotnet publish -c Release -o /build

COPY run.sh /run.sh
RUN chmod +x /run.sh

CMD [ "/run.sh" ]
