FROM tkaarrela/ubuntu:jdk-docker
RUN apt-get install -y curl lsb-release supervisor
ADD supervisord.conf /etc/supervisor/conf.d/supervisord.conf
CMD ["/usr/bin/supervisord"]