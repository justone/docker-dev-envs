FROM nate/devpython

RUN apt-get update && apt-get install libyaml-dev groff -y
RUN pip install awscli troposphere boto awacs requests ansible
RUN wget https://dl.bintray.com/mitchellh/packer/packer_0.7.5_linux_amd64.zip -O /tmp/packer.zip && unzip -d /usr/local/bin/ /tmp/packer.zip && rm /tmp/packer.zip
