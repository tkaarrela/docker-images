FROM ubuntu:jdk8
RUN mkdir /opt/nexus
ADD http://www.sonatype.org/downloads/nexus-latest-bundle.tar.gz /tmp/nexus-latest-bundle.tar.gz
RUN tar -xzvf /tmp/nexus-latest-bundle.tar.gz -C /opt/nexus
RUN rm -rf /tmp/nexus-latest-bundle.tar.gz
RUN ln -s /opt/nexus/nexus-* /opt/nexus/nexus-latest
RUN ln -s /opt/nexus/nexus-latest/bin/nexus /etc/init.d/nexus

ENV RUN_AS_USER root

# declaring exposed ports. helpful for non Linux hosts. add "-P" flag to your "docker run" command to automatically expose them and "docker ps" to discover them.
# nexus
EXPOSE 8081
VOLUME ["/nexus"]
CMD /opt/nexus/nexus-latest/bin/nexus console
