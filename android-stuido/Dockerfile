FROM ubuntu:17.10
LABEL maintainer="jinhan13789@gmail.com"

ENV ANDROID_STUDIO_VERSION 3.1.2.0
ENV ANDROID_STUDIO_URL https://dl.google.com/dl/android/studio/ide-zips/${ANDROID_STUDIO_VERSION}/android-studio-ide-173.4720617-linux.zip
ENV ANDROID_STUDIO /opt/android-studio
ENV ANDROID_HOME /opt/android-sdk

RUN dpkg --add-architecture i386 && \
    apt-get update && \
    apt-get install -y libz1 libncurses5 libbz2-1.0:i386 libstdc++6 libbz2-1.0 lib32stdc++6 lib32z1 && \
    apt-get install -y default-jdk && \
    apt-get clean && \
    apt-get purge 

ADD $ANDROID_STUDIO_URL /tmp/studio.zip
RUN unzip -d /opt /tmp/studio.zip && rm /tmp/studio.zip


CMD ["/opt/android-studio/bin/studio.sh"]
