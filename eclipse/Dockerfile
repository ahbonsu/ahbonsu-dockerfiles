FROM debian:stretch-slim

ENV NO_AT_BRIDGE=1

# update-alternatives needs this folder, otherwise config of openjdk-8-jdk does not run through
RUN mkdir -p /usr/share/man/man1

RUN apt-get update && apt-get install -y \
	wget \
	ca-cacert \
	libcanberra-gtk-module \
	libcanberra-gtk3-module \
	packagekit-gtk3-module \
	openjdk-8-jre-headless \
	openjdk-8-jdk \
	maven \
	--no-install-recommends

RUN wget http://ftp.fau.de/eclipse/technology/epp/downloads/release/2018-09/R/eclipse-jee-2018-09-linux-gtk-x86_64.tar.gz

RUN tar -xvf eclipse-jee-2018-09-linux-gtk-x86_64.tar.gz

ENTRYPOINT [ "bash" ]
