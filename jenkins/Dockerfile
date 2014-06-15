FROM tkaarrela/ubuntu:supervisor
MAINTAINER Tero Kaarrela "tk"

RUN echo deb http://archive.ubuntu.com/ubuntu precise universe >> /etc/apt/sources.list
RUN apt-get update && apt-get clean
RUN apt-get install -qy git
ADD http://updates.jenkins-ci.org/latest/jenkins.war /opt/jenkins.war
RUN ln -sf /jenkins /root/.jenkins
EXPOSE 8080
VOLUME ["/jenkins"]
CMD ["java", "-jar", "/opt/jenkins.war"]