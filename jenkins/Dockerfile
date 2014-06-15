FROM tkaarrela/ubuntu:supervisor
MAINTAINER Tero Kaarrela "tk"

RUN apt-get update && apt-get clean
RUN apt-get install -qy git
ADD http://updates.jenkins-ci.org/latest/jenkins.war /opt/jenkins/jenkins.war
RUN ln -sf /jenkins /root/.jenkins
VOLUME ["/jenkins"]
RUN rm /etc/supervisor/conf.d/supervisord.conf
ADD supervisord.conf /etc/supervisor/conf.d/supervisord.conf
EXPOSE 8080