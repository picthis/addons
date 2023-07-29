#ARG BUILD_FROM="alpine:latest"
FROM python:3

ENV LANG C.UTF-8

# Copy data for add-on
COPY run.sh makeconf.sh rs485.py /

# Install requirements for add-on
RUN apk add --no-cache jq npm make gcc g++ python3 linux-headers udev

WORKDIR /
COPY package.json /
RUN npm install

RUN chmod a+x /makeconf.sh
RUN chmod a+x /run.sh

CMD [ "/run.sh" ]

