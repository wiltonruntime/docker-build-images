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

# updated: 2021-02-16

FROM centos:8
RUN dnf update --exclude=filesystem -y  && \
    dnf install epel-release dnf-plugins-core -y && \
    dnf config-manager --set-enabled powertools -y && \
    dnf copr enable wilton/asio -y && \
    dnf update --exclude=filesystem -y  && \
    dnf install -y \
        git \
        openssh-clients \
        valgrind \
        gcc-c++ \
        make \
        cmake \
        pkg-config \
        zip \
        java-1.8.0-openjdk-devel \
        zlib-devel \
        jansson-devel \
        log4cplus-devel \
        openssl-devel \
        curl-devel \
        asio-devel \
        popt-devel \
        sqlite-devel \
        postgresql-devel \
        soci-devel \
        soci-sqlite3-devel \
        soci-postgresql-devel \
        libpng-devel \
        libharu-devel \
        systemd-devel \
        webkitgtk4-jsc-devel \
        glib2-devel \
        gtk3-devel \
        webkitgtk4-devel \
        libgit2-devel \
        systemd-devel \
        libjpeg-turbo-devel && \
    dnf clean all
