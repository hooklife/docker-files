FROM hyperf/hyperf:7.4-alpine-v3.11-cli-v4.5.2

RUN apk add --no-cache file git autoconf automake libtool gettext gettext-dev make g++ texinfo curl

ENV ROOT_HOME /root
ENV FSWATCH_BRANCH master

WORKDIR ${ROOT_HOME}
RUN git clone https://github.com/emcrisostomo/fswatch.git

WORKDIR ${ROOT_HOME}/fswatch
RUN git checkout ${FSWATCH_BRANCH}
RUN ./autogen.sh && ./configure && make -j
