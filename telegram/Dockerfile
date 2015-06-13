FROM debian:jessie

RUN apt-get update && \
	apt-get install -y \
	libx11-6 \
	libx11-xcb1 \
	libglib2.0-0 \
	fontconfig \
	libappindicator1 \
	wget xz-utils \
	--no-install-recommends 

RUN rm /etc/fonts/conf.d/10-scale-bitmap-fonts.conf
RUN cd / && \
	wget --no-check-certificate -O telegram.tar.xz https://tdesktop.com/linux && \
	tar xvf telegram.tar.xz

CMD ["/Telegram/Telegram"]

