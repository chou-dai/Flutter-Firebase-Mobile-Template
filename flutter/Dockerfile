FROM --platform=linux/amd64 ubuntu:20.04

ENV TZ=Asia/Tokyo
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN apt-get update && apt-get install -y \
        autoconf \
        bash \
        bzip2 \
        curl \
        file \
        wget \
        unzip \
        gnupg \
        software-properties-common \
        vim \
        git \
        clang \
        cmake \
        ninja-build \
        pkg-config \
        libgtk-3-dev

#Flutter
RUN echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list \
    && wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add - \
    && add-apt-repository ppa:maarten-fonville/android-studio
RUN apt-get update && \
    apt-get -y -q install \
    xz-utils libglu1-mesa openjdk-8-jdk google-chrome-stable android-studio \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*	


# Dart
RUN sh -c 'curl https://storage.googleapis.com/download.dartlang.org/linux/debian/dart_stable.list > /etc/apt/sources.list.d/dart_stable.list'
RUN apt-get update && \
    apt-get -y -q install \
    dart \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Download Flutter SDK
RUN git clone https://github.com/flutter/flutter.git /usr/local/flutter
ENV PATH "$PATH:/usr/local/flutter/bin"

# Flutter Web
RUN flutter config --enable-web

# 作業ディレクトリの設定
RUN mkdir /flutter
WORKDIR /flutter

