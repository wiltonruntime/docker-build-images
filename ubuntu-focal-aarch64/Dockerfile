# Copyright 2020, alex at staticlibs.net
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

# updated: 2020-10-22

FROM ubuntu:focal
ADD openssl.cnf /opt/openssl.cnf
ADD sources.list /etc/apt/sources.list
RUN dpkg --add-architecture arm64 && \
    apt update && \
    apt upgrade -y && \
    apt-get install -y \
        git \
        cmake \
        zip \
        openjdk-8-jdk-headless \
        g++-aarch64-linux-gnu \
        pkg-config-aarch64-linux-gnu \
        dpkg-dev \
        qemu-user-static && \
    apt-get remove -y gcc g++ && \
    apt-get autoremove -y && \
    apt install -y \
        zlib1g-dev:arm64 \
        libjansson-dev:arm64 \
        liblog4cplus-dev:arm64 \
        libssl-dev:arm64 \
        libcurl4-openssl-dev:arm64 \
        libasio-dev:arm64 \
        libpopt-dev:arm64 \
        libsqlite3-dev:arm64 \
        libpq-dev:arm64 \
        libsoci-dev:arm64 \
        libpng-dev:arm64 \
        libhpdf-dev:arm64 \
        libglib2.0-dev:arm64 \
        libjavascriptcoregtk-4.0-dev:arm64 \
        libgtk-3-dev:arm64 \
        libwebkit2gtk-4.0-dev:arm64 \
        libssh2-1-dev:arm64 \
        libgit2-dev:arm64 \
        libsystemd-dev:arm64 \
        libjpeg-turbo8-dev:arm64 && \
    apt autoremove -y && \
    apt clean
