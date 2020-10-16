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

# updated: 2020-10-16

FROM debian:wheezy
ADD sources.list /etc/apt/sources.list
RUN echo 'Acquire::Check-Valid-Until "false";' >/etc/apt/apt.conf.d/90ignore-release-date && \
    apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y \
        git \
        curl \
        valgrind \
        build-essential \
        pkg-config \
        zip \
        unzip \
        zlib1g-dev \
        libjansson-dev \
        liblog4cplus-dev \
        libssl-dev \
        libcurl4-openssl-dev \
        libpopt-dev \
        libsqlite3-dev \
        libpq-dev \
        libpng12-dev \
        libglib2.0-dev \
        libjavascriptcoregtk-3.0-dev \
        libgtk-3-dev \
        libwebkitgtk-3.0-dev \
        libssh2-1-dev \
        libjpeg8-dev || true && \
    apt-get autoremove -y && \
    apt-get clean && \
    cd /opt/ && \
    curl -LO https://github.com/ojdkbuild/contrib_jdk8u-ci/releases/download/jdk8u265-b01/jdk-8u265-ojdkbuild-linux-x64.zip && \
    unzip -q jdk-8u265-ojdkbuild-linux-x64.zip && \
    rm jdk-8u265-ojdkbuild-linux-x64.zip && \
    mv jdk-8u265-ojdkbuild-linux-x64 jdk8

