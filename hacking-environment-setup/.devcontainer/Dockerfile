FROM jetpackio/devbox:latest

# Installing your devbox project
WORKDIR /code
USER root:root

# Create TUN device
RUN mkdir -p /dev/net && mknod /dev/net/tun c 10 200

RUN mkdir -p /code && chown ${DEVBOX_USER}:${DEVBOX_USER} /code
USER ${DEVBOX_USER}:${DEVBOX_USER}
COPY --chown=${DEVBOX_USER}:${DEVBOX_USER} devbox.json devbox.json
# COPY --chown=${DEVBOX_USER}:${DEVBOX_USER} devbox.lock devbox.lock



RUN devbox run -- echo "Installed Packages."

RUN devbox shellenv --init-hook >> ~/.profile