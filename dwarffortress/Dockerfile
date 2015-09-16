FROM debian:jessie

RUN dpkg --add-architecture i386 && \
    apt-get update && \
    apt-get install -y --no-install-recommends \
        libsdl-image1.2:i386 \
        libsdl-ttf2.0-0:i386 \
        libgtk2.0-0:i386 \
        libjpeg62-turbo:i386 \
        libglu1-mesa:i386 \
        libopenal1:i386 \
        bzip2 \
        wget

RUN wget http://www.bay12games.com/dwarves/df_40_24_linux.tar.bz2 && \
    tar xvf df_40_24_linux.tar.bz2 && \
    rm df_40_24_linux.tar.bz2 && \
    rm -f /bin/sh && \
    ln -s /bin/bash /bin/sh

WORKDIR /df_linux

RUN ln -s /usr/lib/i386-linux-gnu/libopenal.so.1 ./libs/libopenal.so && \
    ln -s /usr/lib/i386-linux-gnu/libsndfile.so.1 ./libs/libsndfile.so


CMD ["./df"]
