FROM jenkins/jenkins:lts
USER root
ARG dockerGid=999
RUN apt-get update -y \
      && apt-get install -y sudo \
      && rm -rf /var/lib/apt/lists/*
#add user jenkins to docker group
RUN echo "docker:x:${dockerGid}:jenkins" >> /etc/group
USER jenkins
