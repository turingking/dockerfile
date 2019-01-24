FROM alpine
MAINTAINER turingking <jinhan13789@gmail.com>

RUN set -ex \
    && if [ $(wget -qO- ipinfo.io/country) == CN ]; then echo "http://mirrors.aliyun.com/alpine/latest-stable/main/" > /etc/apk/repositories ;fi \
    && apk --update add --no-cache iptables
COPY udp2raw /udp2raw/
WORKDIR /udp2raw
RUN chmod +x udp2raw
ENTRYPOINT [ "./udp2raw" ]


