# Latest version of 
FROM ubuntu
MAINTAINER Johan Guldmyr <>
RUN \
  sed -i -e 's/^Defaults.*requiretty/Defaults    !requiretty/' -e 's/^%wheel.*ALL$/%wheel    ALL=(ALL)    NOPASSWD: ALL/' /etc/sudoers && \
  sed -i 's/# \(.*multiverse$\)/\1/g' /etc/apt/sources.list && \
  apt-get update && \
  apt-get -y upgrade && \
  apt-get install -y build-essential && \
  apt-get install -y software-properties-common && \
  apt-get install -y byobu curl git htop man unzip vim wget python-pip && \
  apt-get install -y libyaml-dev libyaml python-dev python-jinja2 python-httplib2 python-keyczar python-paramiko && \
  pip install pyrax pysphere boto passlib dnspython && \
  rm -rf /var/lib/apt/lists/*

RUN mkdir /etc/ansible/
RUN echo -e '[local]\nlocalhost' > /etc/ansible/hosts
RUN pip install ansible

CMD ["/bin/bash"]
