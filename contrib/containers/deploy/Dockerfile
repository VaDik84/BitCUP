FROM phusion/baseimage:focal-1.0.0
LABEL maintainer="BitCUP Developers <dev@bitcup.org>"
LABEL description="Dockerised BitCUP, built from Travis"

ARG USER_ID
ARG GROUP_ID

ENV HOME /home/bitcup

# add user with specified (or default) user/group ids
ENV USER_ID ${USER_ID:-1000}
ENV GROUP_ID ${GROUP_ID:-1000}
RUN groupadd -g ${GROUP_ID} bitcup && \
    useradd -u ${USER_ID} -g bitcup -s /bin/bash -m -d /home/bitcup bitcup && \
    mkdir /home/bitcup/.bitcup && \
    chown ${USER_ID}:${GROUP_ID} -R /home/bitcup

COPY bin/* /usr/local/bin/

RUN chmod a+x /usr/local/bin/*

USER bitcup

VOLUME ["/home/bitcup"]

EXPOSE 21973 9999 31973 31974

WORKDIR /home/bitcup
