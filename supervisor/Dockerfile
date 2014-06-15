FROM tkaarrela/ubuntu:docker-jdk8
RUN apt-get install -y curl lsb-release supervisor
ADD supervisord.conf /etc/supervisor/conf.d/supervisord.conf
#CMD ["/usr/bin/supervisord"]