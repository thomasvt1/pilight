FROM ubuntu

MAINTAINER Mark Kuipers <mmjgkuipers@gmail.com>

RUN echo "Hello!"

VOLUME /etc/pilight

RUN apt-get update && apt-get install -y --force-yes libunwind8 libpcap0.8 wget vim

RUN echo "deb http://apt.pilight.org/ stable main" > /etc/apt/sources.list.d/pilight.list

RUN wget -O - http://apt.pilight.org/pilight.key | apt-key add -

RUN apt-get update && apt-get install -y pilight pilight-firmware

COPY config.json /etc/pilight/config.json

RUN pilight-daemon

EXPOSE 5001


