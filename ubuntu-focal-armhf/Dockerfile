# Copyright 2018, alex at staticlibs.net
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
# http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

# updated: 2020-10-17

FROM ubuntu:focal
ADD openssl.cnf /opt/openssl.cnf
ADD sources.list /etc/apt/sources.list
RUN dpkg --add-architecture armhf && \
    apt update && \
    apt upgrade -y && \
    apt-get install -y \
        git \
        cmake \
        zip \
        openjdk-8-jdk-headless \
        g++-arm-linux-gnueabihf \
        pkg-config-arm-linux-gnueabihf \
        dpkg-dev \
        qemu-user-static && \
    apt-get remove -y gcc g++ && \
    apt-get autoremove -y && \
    apt install -y \
        zlib1g-dev:armhf \
        libjansson-dev:armhf \
        liblog4cplus-dev:armhf \
        libssl-dev:armhf \
        libcurl4-openssl-dev:armhf \
        libasio-dev:armhf \
        libpopt-dev:armhf \
        libsqlite3-dev:armhf \
        libpq-dev:armhf \
        libsoci-dev:armhf \
        libpng-dev:armhf \
        libhpdf-dev:armhf \
        libglib2.0-dev:armhf \
        libjavascriptcoregtk-4.0-dev:armhf \
        libgtk-3-dev:armhf \
        libwebkit2gtk-4.0-dev:armhf \
        libssh2-1-dev:armhf \
        libgit2-dev:armhf \
        libsystemd-dev:armhf \
        libjpeg-turbo8-dev:armhf && \
    apt autoremove -y && \
    apt clean
