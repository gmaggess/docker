FROM jenkins:latest
COPY plugins.txt /usr/share/jenkins/plugins.txt
RUN /usr/local/bin/plugins.sh /usr/share/jenkins/plugins.txt

USER root
RUN apt-get update && apt-get install -y build-essential libssl-dev curl groovy
RUN curl -sL https://deb.nodesource.com/setup_6.x -o nodesource_setup.sh && bash nodesource_setup.sh && apt-get install -y nodejs

USER jenkins
