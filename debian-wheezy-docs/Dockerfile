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

FROM debian:wheezy
ADD sources.list /etc/apt/sources.list
RUN echo 'Acquire::Check-Valid-Until "false";' >/etc/apt/apt.conf.d/90ignore-release-date && \
    apt-get -qq update && \
    apt-get -qq upgrade -y && \
    apt-get -qq install -y \
        git \
        curl \
        vim \
        doxygen \
        make \
        mc && \
    apt-get -qq autoremove -y && \
    apt-get -qq clean && \
    cd /opt/ && \
    curl -LO https://github.com/ojdkbuild/contrib_jdk8u-ci/releases/download/jdk8u265-b01/jdk-8u265-ojdkbuild-linux-x64.zip && \
    unzip -q jdk-8u265-ojdkbuild-linux-x64.zip && \
    rm jdk-8u265-ojdkbuild-linux-x64.zip && \
    mv jdk-8u265-ojdkbuild-linux-x64 jdk8 && \
    git clone --quiet https://github.com/wiltonruntime/tools_linux_cmake.git cmake

