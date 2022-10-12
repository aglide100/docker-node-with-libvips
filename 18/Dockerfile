FROM node:18-buster

RUN apt update && apt install -y wget libvips-dev libglib2.0-dev build-essential glib2.0-dev expat gobject-introspection libgtk2.0-doc 

RUN cd /usr/local/src/ && wget https://www.openssl.org/source/openssl-3.0.2.tar.gz && tar -xvf openssl-3.0.2.tar.gz

RUN cd /usr/local/src/openssl-3.0.2 && ./config && make && make install

ENV LD_LIBRARY_PATH /usr/local/lib/:/usr/local/lib64/

RUN wget https://github.com/libvips/libvips/releases/download/v8.12.2/vips-8.12.2.tar.gz

RUN tar xf vips-8.12.2.tar.gz

RUN cd vips-8.12.2 && ./configure && make && make install && rm -rf vips-8.12.2