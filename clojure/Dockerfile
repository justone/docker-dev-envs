FROM nate/basedev

RUN apt-get install openjdk-7-jre-headless -y
RUN curl -s https://raw.githubusercontent.com/technomancy/leiningen/2.5.1/bin/lein > \
            /usr/local/bin/lein && \
            chmod 0755 /usr/local/bin/lein && \
            /usr/local/bin/lein
