FROM debian:jessie as build

RUN apt-get update && \
	apt-get install -y --no-install-recommends \
		curl \
		build-essential

WORKDIR /tmp
RUN curl -O http://download.joedog.org/siege/siege-4.0.4.tar.gz && \
	tar -xvf siege-4.0.4.tar.gz && \
	cd siege-4.0.4 && \
	./configure && \
	make && \
	make install

FROM alpine:3.6

RUN apk add --update openssl && \
	wget -O /etc/apk/keys/sgerrand.rsa.pub https://raw.githubusercontent.com/sgerrand/alpine-pkg-glibc/master/sgerrand.rsa.pub && \
	wget https://github.com/sgerrand/alpine-pkg-glibc/releases/download/2.25-r0/glibc-2.25-r0.apk && \
	apk add glibc-2.25-r0.apk

LABEL maintainer "Tom Barlow <tom.barlow@docker.com>"
COPY --from=build /usr/local/bin/siege /usr/local/bin/siege
COPY --from=build /usr/local/etc/siegerc /usr/local/etc/siegerc

ENTRYPOINT ["siege"]
