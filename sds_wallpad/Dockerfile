ARG BUILD_FROM
FROM $BUILD_FROM

ENV LANG C.UTF-8

RUN apk add --no-cache jq npm make gcc g++ python3 linux-headers udev

COPY . /srv
RUN chmod a+x /srv/run_addon.sh

WORKDIR /share

CMD [ "/srv/run_addon.sh" ]
