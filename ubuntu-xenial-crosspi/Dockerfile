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

# updated: 2020-10-28

FROM ubuntu:xenial
RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y \
        git \
        build-essential \
        cmake \
        zip \
        wget \
        openjdk-8-jdk-headless \
        pkg-config && \
    apt-get autoremove -y && \
    wget https://github.com/Pro/raspi-toolchain/releases/download/v1.0.1/raspi-toolchain.tar.gz && \
    tar xfz raspi-toolchain.tar.gz --strip-components=1 -C /opt && \
    rm raspi-toolchain.tar.gz && \
    git clone https://github.com/wiltonruntime/crosspi-buster-sysroot.git /opt/cross-pi-gcc-sysroot && \
    ln -s /opt/cross-pi-gcc-sysroot/usr/bin/arm-linux-gnueabihf-pkg-config /opt/cross-pi-gcc/bin/arm-linux-gnueabihf-pkg-config


