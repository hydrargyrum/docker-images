# inspired from https://github.com/heichblatt/dockerfiles/blob/master/foldingathome/Dockerfile

FROM ubuntu:latest

ADD https://download.foldingathome.org/releases/public/fah-client/debian-10-64bit/release/latest.deb /tmp/fahclient.deb

# FIXME: Awful workaround until the DEBs are correctly packaged
RUN dpkg -i /tmp/fahclient.deb || true

VOLUME ["/var/lib/fahclient", "/etc/fahclient"]
CMD [ "/usr/bin/fah-client" ]
