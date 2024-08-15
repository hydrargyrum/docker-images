### BASE APPS
FROM debian:stable

# install syncthing relay server
# and ca-certificates for generating certs
RUN apt-get update && apt-get install -y \
    ca-certificates \
    syncthing-relaysrv

### PRIVILEGES
# the dedicated "strelay" user:
# - owns key files
# - runs the app
RUN useradd -g users strelay

### PRIVATE KEYS
# keys will be stored in /strelay
RUN mkdir /strelay
# strelay user needs access to that dir
RUN chown strelay /strelay
RUN chgrp users /strelay
# persist the private key by using a volume
VOLUME /strelay

### PRIVILEGES
# we do not need root anymore
USER strelay

### NETWORK
EXPOSE 22067/tcp 22070/tcp

### RUNNING
WORKDIR /strelay
CMD strelaysrv -keys=/strelay \
    -protocol=tcp4 \
    ${STRELAY_GLOBAL_RATE:+-global-rate=$STRELAY_GLOBAL_RATE} \
    ${STRELAY_SESSION_RATE:+-per-session-rate=$STRELAY_SESSION_RATE} \
    ${STRELAY_OWNER:+-provided-by=$STRELAY_OWNER}
