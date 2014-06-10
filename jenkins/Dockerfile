FROM ubuntu:jdk8
MAINTAINER Tero Kaarrela "tk"

RUN echo deb http://archive.ubuntu.com/ubuntu precise universe >> /etc/apt/sources.list
RUN apt-get update && apt-get clean
RUN apt-get install -q -y openjdk-7-jre-headless && apt-get clean
RUN apt-get install -q -y git-core && apt-get clean
RUN git config --global user.email "tero.kaarrela@gmail.com"
RUN git config --global user.name "Tero Kaarrela"
ADD http://mirrors.jenkins-ci.org/war/1.566/jenkins.war /opt/jenkins.war
RUN ln -sf /jenkins /root/.jenkins

ENTRYPOINT ["java", "-jar", "/opt/jenkins.war"]
EXPOSE 8080
VOLUME ["/jenkins"]
CMD [""]
