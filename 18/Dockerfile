FROM node:18

RUN cd /etc/apt && sed -i 'deb http://security.ubuntu.com/ubuntu focal-security main' sources.list

RUN apt update && apt install -y wget libvips-dev libglib2.0-dev
RUN apt -y install glib2.0-dev expat gobject-introspection libgtk2.0-doc 
RUN wget https://github.com/libvips/libvips/releases/download/v8.12.2/vips-8.12.2.tar.gz
RUN tar xf vips-8.12.2.tar.gz

RUN cd vips-8.12.2 && ./configure && make && make install && rm -rf vips-8.12.2