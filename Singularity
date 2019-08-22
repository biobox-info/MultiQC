Bootstrap: docker
From: ubuntu:18.04

%environment
PATH=/usr/local/src/MultiQC:$PATH
export LC_ALL=C.UTF-8
export LANG=C.UTF-8

%post
apt-get update 
apt-get dist-upgrade -y 
apt-get install wget build-essential unzip git python3-setuptools python3 -y 
rm -rf /var/lib/apt/lists/*
mkdir -p /usr/local/src
cd /usr/local/src && \
git clone https://github.com/ewels/MultiQC.git && \
cd MultiQC && \
python3 setup.py install

%labels
MAINTAINER BioBox
Version v1.0
