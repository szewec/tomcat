FROM tomcat:7.0-jre8

RUN apt-get update && \
    apt-get install -y libgtk2.0 libdbus-glib-1-2 libsm6 libglu1-mesa && \
    apt-get clean

ENV LIBREOFFICE_VERSION=5.3.7

RUN wget http://download.documentfoundation.org/libreoffice/stable/${LIBREOFFICE_VERSION}/deb/x86_64/LibreOffice_${LIBREOFFICE_VERSION}_Linux_x86-64_deb.tar.gz -O /tmp/LibreOffice_${LIBREOFFICE_VERSION}_Linux_x86-64_deb.tar.gz && \
    tar -xzvf /tmp/LibreOffice_5.3.7_Linux_x86-64_deb.tar.gz -C /tmp && \
    dpkg -i /tmp/LibreOffice_${LIBREOFFICE_VERSION}*_Linux_x86-64_deb/DEBS/*.deb && \
    rm -rf /tmp/LibreOffice_${LIBREOFFICE_VERSION}*
