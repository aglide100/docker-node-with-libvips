FROM node:16-buster

# RUN curl https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add - && \
#     curl https://storage.googleapis.com/download.dartlang.org/linux/debian/dart_stable.list > /etc/apt/sources.list.d/dart_stable.list && \
#     sed -i /etc/apt/sources.list.d/dart_stable.list -e 's/https:/http:/g'
    
RUN apt update && apt install -y wget libvips-dev libglib2.0-dev
RUN apt -y install glib2.0-dev expat gobject-introspection libgtk2.0-doc 
RUN wget https://github.com/libvips/libvips/releases/download/v8.12.2/vips-8.12.2.tar.gz
RUN tar xf vips-8.12.2.tar.gz

RUN cd vips-8.12.2 && ./configure && make && make install && rm -rf vips-8.12.2