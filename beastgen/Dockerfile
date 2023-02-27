FROM	ubuntu:18.04

RUN     apt-get update \
&&      apt-get install -y openjdk-8-jre openjdk-8-jdk python3\
&&      apt-get install -y wget unzip \
&&	    wget https://github.com/beast-dev/beast-mcmc/releases/download/v1.10.5pre_thorney/BEASTGen_v1.0.3pre_thorney.zip \
&&      unzip BEASTGen_v1.0.3pre_thorney.zip \
&&      rm -rf BEASTGen_v1.0.3pre_thorney.zip \
&&      apt-get autoremove -y wget unzip

ENV PATH="${PATH}:/BEASTGen_v1.0.3pre_thorney/bin"

LABEL	tool=beastgen version=1.0.3

WORKDIR /data