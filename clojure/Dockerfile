FROM nate/basedev

RUN apt-get install openjdk-7-jre-headless -y
RUN curl -s https://raw.githubusercontent.com/technomancy/leiningen/2.5.1/bin/lein > \
            /usr/local/bin/lein && \
            chmod 0755 /usr/local/bin/lein && \
            /usr/local/bin/lein

# Add user and allow sudo
ONBUILD ARG DEV_USER
ONBUILD ARG DEV_UID
ONBUILD ARG DEV_GID
ONBUILD ENV DEV_USER $DEV_USER
ONBUILD ENV DEV_UID $DEV_UID
ONBUILD ENV DEV_GID $DEV_GID
ONBUILD RUN addgroup --gid $DEV_GID $DEV_USER
ONBUILD RUN adduser --uid $DEV_UID --gid $DEV_GID $DEV_USER --gecos "" --disabled-password
ONBUILD RUN echo "$DEV_USER   ALL=NOPASSWD: ALL" >> /etc/sudoers
