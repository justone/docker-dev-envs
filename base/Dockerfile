FROM ubuntu
MAINTAINER Nate Jones <nate@endot.org>

ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update && apt-get install vim-nox locales sudo tmux git openssh-server curl tree less aptitude man wget unzip libfile-slurp-perl -y

# Set up UTF-8
RUN echo "en_US.UTF-8 UTF-8" > /etc/locale.gen && locale-gen en_US.UTF-8
ENV LC_ALL en_US.utf8

# Add my user
RUN addgroup --gid 1000 nate
RUN adduser --uid 1000 --gid 1000 nate --gecos "" --disabled-password

# Ensure that color and time zone are correct
ENV TERM xterm-256color
ENV TZ /usr/share/zoneinfo/America/Los_Angeles

# Allow me to sudo
RUN echo "nate   ALL=NOPASSWD: ALL" >> /etc/sudoers

EXPOSE 22

RUN mkdir /var/run/sshd
CMD ["/usr/sbin/sshd", "-D"]
