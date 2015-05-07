FROM nate/devpython

RUN apt-get update && apt-get install software-properties-common language-pack-en -y

# Set up repos for weechat and bitlbee
RUN add-apt-repository ppa:nesthib/weechat-stable -y
ADD bitlbee.key /tmp/bitlbee.key
RUN apt-key add /tmp/bitlbee.key
RUN echo "deb http://code.bitlbee.org/debian/devel/trusty/amd64/ ./" >> /etc/apt/sources.list.d/bitlbee.list

RUN apt-get update && apt-get install weechat=1.1.1~stable+20150128~trusty1 bitlbee bitlbee-plugin-otr perl -y
# required for the wee-slack plugin
RUN pip install websocket-client
RUN ln -sf /usr/share/zoneinfo/PST8PDT /etc/localtime

ADD bitlbee.conf /etc/bitlbee/bitlbee.conf
