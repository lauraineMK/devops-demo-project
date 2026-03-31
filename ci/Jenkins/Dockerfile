FROM jenkins/jenkins:lts-jdk17

USER root

# Install Maven
RUN apt-get update && apt-get install -y maven

# Install Docker
RUN apt-get install -y ca-certificates curl sudo && \
    curl -fsSL https://get.docker.com -o install-docker.sh && \
    sh install-docker.sh && \
    usermod -a -G docker jenkins

USER jenkins

EXPOSE 8080
