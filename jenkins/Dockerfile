FROM jenkins:latest
COPY plugins.txt /usr/share/jenkins/plugins.txt
RUN /usr/local/bin/plugins.sh /usr/share/jenkins/plugins.txt

USER root
RUN apt-get update
RUN apt-get install -y build-essential libssl-dev
RUN apt-get install curl
RUN curl -sL https://deb.nodesource.com/setup_6.x -o nodesource_setup.sh
RUN bash nodesource_setup.sh
RUN apt-get install -y nodejs

USER jenkins
