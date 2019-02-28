FROM jenkins/ssh-slave
LABEL maintainer "louis.davin@pumpkin-app.com"

# https://developer.android.com/studio/#downloads
ARG ANDROID_SDK_VERSION=4333796
RUN mkdir -p /opt/android-sdk && cd /opt/android-sdk && \
    wget -q https://dl.google.com/android/repository/sdk-tools-linux-${ANDROID_SDK_VERSION}.zip && \
    unzip *tools*linux*.zip && \
    rm *tools*linux*.zip
ENV ANDROID_HOME /opt/android-sdk
ENV PATH ${PATH}:${ANDROID_HOME}/tools:${ANDROID_HOME}/platform-tools:${ANDROID_HOME}/tools/bin

# accept the license agreements of the SDK components
ADD license_accepter.sh /opt/
RUN /opt/license_accepter.sh $ANDROID_HOME