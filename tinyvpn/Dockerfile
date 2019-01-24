FROM alpine
MAINTAINER turingking <jinhan13789@gmail.com>

COPY tinyvpn /tinyvpn/
WORKDIR /tinyvpn
RUN chmod +x tinyvpn
CMD ./tinyvpn -s -l0.0.0.0:4096 -f20:10 -k "passwd" --sub-net 10.22.22.0



