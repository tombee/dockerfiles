FROM debian:jessie

RUN apt-get update && \
	apt-get install wget -y --no-install-recommends && \
	cd /root && \
	wget --no-check-certificate -O - "https://www.dropbox.com/download?plat=lnx.x86_64" | tar xzf -

CMD ["/root/.dropbox-dist/dropboxd"]
