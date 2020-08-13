FROM openjdk:8-jdk-alpine

RUN apk update && apk upgrade && apk add --no-cache curl

WORKDIR /app

ENV ST_VER=8.0

RUN curl -L https://bitbucket.org/art-uniroma2/semantic-turkey/downloads/semanticturkey-${ST_VER}_PATCHED.zip -o semanticturkey.zip \
    && curl -L https://raw.githubusercontent.com/niva83/onto-stack/master/it.uniroma2.art.semanticturkey.cfg -o it.uniroma2.art.semanticturkey.cfg \
    && unzip semanticturkey.zip -d /app \
    && rm semanticturkey.zip

COPY ./it.uniroma2.art.semanticturkey.cfg /app/semanticturkey-${ST_VER}/etc/it.uniroma2.art.semanticturkey.cfg

EXPOSE 1979

CMD sh /app/semanticturkey-${ST_VER}/bin/karaf server